# demo-spring-boot-aws-codedeploy
### Description 
* Demonstrate the deployment of a spring-boot application using AWS CodeBuild,
AWS CodeDeploy and AWS CodePipeline.
### User-data for EC2
```shell
#!/bin/bash
sudo yum update
sudo yum install -y ruby
sudo yum install -y wget
CODEDEPLOY_BIN="/opt/codedeploy-agent/bin/codedeploy-agent"
$CODEDEPLOY_BIN stop
yum erase codedeploy-agent -y
cd /home/ec2-user
wget https://aws-codedeploy-ap-south-1.s3.ap-south-1.amazonaws.com/latest/install
chmod +x ./install
sudo ./install auto
sudo yum install -y python-pip
sudo pip install awscli
sudo yum install -y java-17-amazon-corretto
```
