## Deploying a Static Website on NGINX to AWS

This project focuses on deploying a static website using NGINX on an AWS EC2 instance running Amazon Linux 2. Below are the steps and configurations used to set up and deploy the website.

Prerequisites
AWS Account: Ensure you have an AWS account set up.
EC2 Instance: Launch an EC2 instance with Amazon Linux 2.
NGINX Installation: Install NGINX on the EC2 instance.
Domain Configuration: Configure your domain to point to the EC2 instance's public IP.

Steps to Deploy
1. Launch EC2 Instance
Launch an EC2 instance with Amazon Linux 2 AMI.
Ensure the security group allows HTTP (port 80) and HTTPS (port 443) inbound traffic.
2. Install NGINX
Connect to your EC2 instance using SSH.
Install NGINX:

sudo amazon-linux-extras install nginx1
sudo systemctl start nginx
sudo systemctl enable nginx

## Project Structure 

- **nginx.conf**: Main NGINX configuration file located at `/etc/nginx/nginx.conf`.
- **/etc/nginx/conf.d/**: Directory containing additional NGINX configuration files.
- **/var/log/nginx/**: NGINX log files directory.

### Installation

1. **SSH into your EC2 Instance**:
   
   ssh -i path/to/your/private-key.pem ec2-user@your-ec2-instance-public-ip
Update Package Repository:

sudo yum update

Install NGINX:

sudo yum install nginx
Configure NGINX:

Edit /etc/nginx/nginx.conf and other configuration files as needed.

Verify the configuration:

sudo nginx -t

Start NGINX:

sudo systemctl start nginx

Access NGINX Logs:

sudo tail -f /var/log/nginx/error.logNotes

Ensure appropriate security group rules are set to allow inbound traffic on ports 80 (HTTP) and/or 443 (HTTPS).

Monitor NGINX logs (/var/log/nginx/error.log) for troubleshooting.











