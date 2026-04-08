# DevOps Capstone Project

A fully automated infrastructure pipeline combining Terraform, Ansible, Docker and Flask.

## What it does
1. Terraform provisions a real EC2 server on AWS
2. Ansible SSHes into the server, installs Docker and deploys the Flask app
3. Flask app runs inside a Docker container on the live server
4. App is accessible from anywhere in the world

## Stack
- Terraform — infrastructure provisioning
- Ansible — server configuration and app deployment
- Docker — application containerization
- Flask — web application
- AWS EC2 — cloud server

## How to use

### 1. Provision the server
cd terraform
terraform init
terraform apply

### 2. Update the server IP in ansible/inventory.ini

### 3. Deploy the app
ansible-playbook -i ansible/inventory.ini ansible/playbook.yml

### 4. Access the app
http://<your-server-ip>:5000

### 5. Destroy when done
cd terraform
terraform destroy# devops-capstone
