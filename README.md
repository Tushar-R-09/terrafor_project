# 🌐 Multi-Region Web Hosting with Terraform on AWS

This project demonstrates how to deploy a **highly available web infrastructure** on AWS using **Terraform**. It provisions a **VPC**, **two subnets**, **EC2 instances hosting sample webpages**, and an **Application Load Balancer (ALB)** to distribute traffic between them.

---

## 🏗️ Project Overview

- **VPC** – Creates an isolated virtual network.  
- **Subnets** – Two subnets in different availability zones (`us-east-1a` & `us-east-1b`) for redundancy.  
- **Internet Gateway & Route Tables** – Enable internet connectivity for public subnets.  
- **Security Group** – Allows HTTP (80) and SSH (22) access from anywhere.  
- **EC2 Instances** – Hosts a sample webpage using `userdata.sh` and `userdata1.sh`.  
- **S3 Bucket** – Example bucket for storage (`hmlaprojectbucket2024`).  
- **Application Load Balancer (ALB)** – Distributes incoming traffic across the two web servers.  
- **Target Group & Listener** – Routes HTTP traffic to the EC2 instances.  
- **Output** – Displays the ALB DNS for accessing the web application.

---

## 🛠️ Terraform Resources Used

- `aws_vpc`, `aws_subnet`  
- `aws_internet_gateway`, `aws_route_table`, `aws_route_table_association`  
- `aws_security_group`  
- `aws_instance`  
- `aws_s3_bucket`  
- `aws_lb`, `aws_lb_target_group`, `aws_lb_target_group_attachment`, `aws_lb_listener`  

---

## 🚀 Getting Started

### **Prerequisites**
- Terraform installed ([Terraform Download](https://developer.hashicorp.com/terraform/downloads))  
- AWS CLI configured with credentials (`aws configure`)  
- Basic knowledge of AWS services like VPC, EC2, and Load Balancers  

### **Setup Instructions**
1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/multi-region-terraform.git
   cd multi-region-terraform
