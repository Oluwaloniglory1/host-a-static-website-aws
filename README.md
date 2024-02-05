# Project Title: Host a Static Website on AWS

## Overview
This project involves hosting a static HTML web app on AWS, utilizing various AWS resources and configurations for optimal performance, security, and reliability. The key components include a Virtual Private Cloud (VPC), public and private subnets across multiple Availability Zones, Internet Gateway, Security Groups, EC2 instances, Application Load Balancer, Auto Scaling Group, GitHub for version control, Certificate Manager for secure communication, Simple Notification Service (SNS) for alerting, and Route 53 for domain registration and DNS setup.

## Project Structure
- **VPC Configuration:**
  - Created a Virtual Private Cloud with public and private subnets across two Availability Zones.
  - Deployed an Internet Gateway to enable connectivity between VPC instances and the Internet.
  - Established Security Groups for network firewall mechanisms.

- **EC2 Instance Setup:**
  - Positioned web servers within private subnets for enhanced security.
  - Implemented EC2 Instance Connect Endpoint for secure connections.
  - Enabled instances in private subnets to access the Internet via NAT Gateway.

- **Web App Deployment:**
  - Hosted the static website on EC2 instances.
  - Utilized an Auto Scaling Group for managing instances to ensure availability, scalability, fault tolerance, and elasticity.
  - Employed an Application Load Balancer and a target group for even distribution of web traffic across multiple Availability Zones.

- **Version Control and Collaboration:**
  - Stored web files on GitHub for version control and collaboration.
  - Utilized a Bash script to automate deployment from the GitHub repository.

- **Security and Communication:**
  - Secured application communications using Certificate Manager.
  - Configured Simple Notification Service (SNS) to receive alerts about activities within the Auto Scaling Group.

- **Domain Registration and DNS Setup:**
  - Registered the domain name and set up a DNS record using Route 53.

## Deployment Script
The provided deployment script (`deploy.sh`) accomplishes the following tasks:
- Switches to the root user for administrative privileges.
- Updates all installed packages to their latest versions.
- Installs Apache HTTP Server and Git.
- Clones the project GitHub repository.
- Copies all files from the cloned repository to the Apache web root.
- Removes unnecessary files from the cloned repository.
- Enables the Apache HTTP Server to start automatically at system boot.
- Starts the Apache HTTP Server to serve web content.

## How to Use
1. Ensure that you have the necessary AWS credentials configured.
2. Run the provided deployment script (`deploy.sh`) on your EC2 instance.


