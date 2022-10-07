# Amazon EC2 Instance Isolation Challenge - Rescue a Compromised EC2 Instance Incident Run Book

## The Challenge Mission

## Challenge scenario
You have recently been hired as a cloud engineer for a gambling company. <br> The company heavily uses Amazon EC2 instances inside Elastic Load Balancing Auto Scaling Groups.

The company's cloud resources have been targeted by malicious actors in the past, and some resources were compromised.

As a part of your initial training, you have received instructions on what to do if a compromise is detected. <br> Below is the company's run book for dealing with a suspected compromised Amazon EC2 instance:

## Tasks

Tag any resources you create with the key **IncidentStatus** and the value **Isolated**.

1. Detach the instance from its auto scaling group and tag it
2. Create a new security group that disallows both inbound and outbound traffic (if one doesn't already exist)
3. Remove the instance's current security group and replace it with the group that blocks inbound and outbound traffic
4. Remove the IAM role from the instance (ensure no role is associated)
5. Snapshot the instance's root volume for later analysis
6. Create an AMI of the instance for later analysis

# Solutions
1. Detach an EC2 Instance from Scaling Group = https://docs.aws.amazon.com/autoscaling/ec2/userguide/detach-instance-asg.html
2. Create a new security group that disallows both inbound and outbound traffic (if one doesn't already exist) - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/working-with-security-groups.html
3. Attach Security Security Group to an Instance - https://stackoverflow.com/questions/52641395/can-we-remove-a-security-group-from-an-running-ec2-instance
4. Remove the IAM role from the instance (ensure no role is associated) - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/iam-roles-for-amazon-ec2.html
5. Snapshot the instance's root volume for later analysis - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-creating-snapshot.html
6. Create an AMI from an Amazon EC2 Instance - https://docs.aws.amazon.com/toolkit-for-visual-studio/latest/user-guide/tkv-create-ami-from-instance.html
