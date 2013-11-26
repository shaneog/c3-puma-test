# c3-puma-test
Proof of concept app using Rails 4, Capistrano 3, and Puma

**Guide**

1. Create a new AWS instance. I used the AMI ID ami-0157f11c (m3.xlarge, EBS optimised). Ensure it has a public IP (so that you can SSH into it)
2. Login to machine using SSH
3. Run the following command to update the EC2 machine and set up Ruby 2.0.0-p353 and NodeJS v0.10.22
```
\curl -L https://gist.github.com/shaneog/7650901/raw/df80823ec123643a87f4d8df2eaf684a27799c19/aws.sh | bash -s stable
```
4. Clone this repository to your local machine `git clone https://github.com/shaneog/c3-puma-test.git`
5. Change into the repo directory and update the file `config/deploy/production.rb` with your EC2 instance public DNS name
6. Run `cap production deploy`
