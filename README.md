# 🚀 DevOps Project: AWS Automation with Terraform & GitLab CI/CD

## 📌 Overview
Automating AWS infrastructure deployment using Terraform and GitLab CI/CD.



## 📂 Project Structure
- **VPC Module:** VPC, subnets, security groups
- **EC2 Module:** EC2 instance setup
- **Backend Configuration:** S3 & DynamoDB for Terraform state

## 🚀 GitLab CI/CD Pipeline
Stages: **Validate → Plan → Apply → Destroy**
```yaml
image: hashicorp/terraform:latest
stages: [validate, plan, apply, destroy]
validate: script: ["terraform init", "terraform validate"]
plan: script: ["terraform plan -out=planfile"]
apply: script: ["terraform apply planfile"] when: manual
destroy: script: ["terraform destroy -auto-approve"] when: manual
```

## 📌 Setup & Deployment
```bash
git init && git add . && git commit -m "Initial commit"
git push -u origin dev
terraform init && terraform apply -auto-approve
```

✅ **Automated AWS deployment with Terraform & GitLab CI/CD.**

