# The-Server-Commander

📌 Project Overview

A startup is launching a new dynamic application and requires a dedicated server environment with full OS control to install custom software and security patches.

As a System Administrator, this project demonstrates how to:

-Provision a Virtual Machine (AWS EC2 / Azure VM)

-Connect securely using SSH

-Install and configure a Web Server (Apache/Nginx)

-Host a custom webpage: "Welcome to DecodeLabs"


🏗️ Architecture

Client (Browser)
⬇
Internet
⬇
EC2 / Virtual Machine (Ubuntu / Amazon Linux)
⬇
Apache / Nginx Web Server
⬇
Custom HTML Page


🛠️ Tools & Technologies

☁️ AWS EC2 / Azure Virtual Machine

🐧 Ubuntu / Amazon Linux

🔐 SSH (Secure Shell)

🌐 Apache / Nginx Web Server

💻 Linux Terminal


⚙️ Step 1: Launch Virtual Machine (AWS EC2)

1.Login to AWS Console

2.Go to EC2 → Launch Instance

3.Choose:

-AMI: Ubuntu / Amazon Linux

-Instance Type: t2.micro (Free Tier)

4.Create or Select Key Pair

5.Configure Security Group:

-Allow SSH (Port 22)

-Allow HTTP (Port 80)

6.Launch Instance


🔐 Step 2: Connect to Server via SSH

For Amazon Linux:

ssh -i key.pem ec2-user@your-public-ip


Install Apache (Amazon Linux)
sudo yum update -y
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd

📄 Step 4: Create Custom Web Page

Navigate to web root directory:

Amazon Linux:

cd /var/www/html

Create index.html:

sudo nano index.html


Add the following content:

<!DOCTYPE html>
<html>
<head>
    <title>DecodeLabs</title>
</head>
<body>
    <h1>Welcome to DecodeLabs</h1>
    <p>Server is successfully configured!</p>
</body>
</html>

Save and exit.


🌍 Step 5: Access Website

Open browser and visit:

http://54.88.48.105

You should see:

🎉 Welcome to DecodeLabs


🔒 Security Configuration

Only required ports opened (22, 80)

SSH secured using Key Pair

Web server enabled on boot


✅ Project Outcome

✔ Successfully provisioned a Virtual Machine
✔ Connected securely via SSH
✔ Installed and configured Apache Web Server
✔ Hosted a custom webpage
