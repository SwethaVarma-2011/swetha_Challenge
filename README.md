1. Architecture Overview
AWS Services: Use Amazon S3 for hosting the static web page, Amazon CloudFront for CDN, AWS Certificate Manager (ACM) for SSL/TLS certificates, and AWS WAF for security.
Configuration Management Tool: Use Terraform for infrastructure as code (IaC) and Ansible for configuration management.

2. Steps to Implement

Step 1: Create and Deploy a Web Server
Terraform Configuration:
Define an S3 bucket to host the static website.
Configure CloudFront to serve the content from the S3 bucket.
Use ACM to create a self-signed certificate for HTTPS.
1.a Ansible Playbook:
Install and configure Nginx to serve the static page.
Redirect HTTP to HTTPS using Nginx configuration

Step 2: Secure the Application
Use AWS WAF to protect against common web exploits.
Ensure only ports 80 and 443 are open in the security group.

Step 3: Automated Tests
Use Ansible to run automated tests to validate the server configuration.

3. Monitoring and Scaling
Monitoring: Use AWS CloudWatch to monitor the health and performance of the application.
Scaling: Use AWS Auto Scaling to automatically scale the number of instances based on demand.
