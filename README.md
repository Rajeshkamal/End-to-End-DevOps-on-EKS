Project Overview

This project demonstrates a complete DevOps lifecycle on AWS EKS, implemented using Infrastructure as Code (Terraform) and modern DevOps tools.
It covers CI/CD pipeline automation, artifact management, code quality analysis, container orchestration, and monitoring — making it a real-world, production-grade setup.

🛠️ Tools & Technologies Used

Infrastructure: Terraform, AWS EKS
CI/CD: Jenkins, GitHub Webhooks
Artifact Management: Nexus
Code Quality & Security: SonarQube, Trivy
Containerization: Docker, Kubernetes
Monitoring & Logging: Prometheus, Grafana
Database: MySQL with Backup & PVC
Ingress & Security: Nginx Ingress, SSL/TLS Certificates

📂 Project Architecture
<img width="5316" height="3619" alt="qqqqqq" src="https://github.com/user-attachments/assets/9cca72e8-0c2e-477e-a42f-2f239e232eeb" />

🔄 CI/CD Workflow
1️⃣ CI (Continuous Integration)

Code is pushed to GitHub → Webhook triggers Jenkins pipeline
Pre-Build Phase: Compile, Test, Quality Check (SonarQube)
Build Phase: Docker Image build, pushed to DockerHub, stored in Nexus
Post-Build Phase: Notifications (Email/Slack)

2️⃣ CD (Continuous Deployment)

Jenkins triggers deployment to EKS
Kubernetes manifests (Helm/Terraform) deploy app + MySQL DB
SSL enabled via Cert-Manager & Ingress
Continuous monitoring via Prometheus & Grafana

⭐ Key Highlights

End-to-End CI/CD: From code commit → to deployment on EKS
Complete Monitoring: Prometheus + Grafana dashboards
Security & Quality: Trivy scans + SonarQube checks
Scalable Architecture: Runs on AWS EKS with Terraform IaC
Production Ready: SSL, Ingress, Secrets, and Backups
