# First-file
This is second file for testing purpose
<BR>
Author:- Utkarsh Dubey


New Project and Descriptions 

1. Dockerized Node.js App on AWS EC2 with Terraform

Goal: Deploy a simple Node.js app (in Docker) on AWS using Terraform, with CI/CD via GitHub Actions.

Stack:

App: Node.js REST API (Hello World / ToDo API).

Containerization: Dockerfile (multi-stage build).

Infra: Terraform → AWS EC2 + Security Group.

Deployment: GitHub Actions → Build & push Docker image to DockerHub/ECR → Deploy on EC2.

Steps:

Write a Node.js app with Dockerfile.

Use Terraform to create EC2 + Security Group.

Configure EC2 UserData script → install Docker & run container.

Add GitHub Actions pipeline:

On commit → build Docker image → push to DockerHub/ECR → SSH into EC2 → pull & run container.

Practice Areas:
✅ Docker build, push, run
✅ Terraform provisioning
✅ GitHub CI/CD pipeline

2. Static Website on AWS S3 + CloudFront with Terraform

Goal: Host a React app (or static HTML) on S3, exposed via CloudFront, all managed by Terraform.

Stack:

App: ReactJS (or plain HTML).

Infra: Terraform → S3 bucket + CloudFront + IAM policy.

CI/CD: GitHub Actions → Deploy static site to S3 on every push.

Steps:

Create React app (npm run build → static files).

Write Terraform code for:

S3 bucket (static hosting enabled).

CloudFront distribution.

IAM bucket policy.

Add GitHub Actions workflow → Sync build files to S3 (aws s3 sync build/ s3://bucket-name).

Practice Areas:
✅ Terraform S3/CloudFront/IAM
✅ GitHub → AWS S3 Deployment
✅ AWS static hosting best practices

3. Multi-Service App on AWS ECS (Fargate) with Terraform

Goal: Deploy microservices (Node.js + MongoDB) in Docker containers on ECS Fargate.

Stack:

App: Node.js (API) + MongoDB (container).

Infra: Terraform → ECS Cluster, Task Definition, Fargate Service.

Storage: AWS RDS or MongoDB Atlas (optional).

CI/CD: GitHub Actions → Push images to ECR → Trigger ECS deploy.

Steps:

Write Dockerfiles for Node.js + MongoDB.

Push images to ECR.

Use Terraform for ECS Cluster + Fargate Task + ALB.

Add GitHub Actions for CI/CD → On commit → build & push image → update ECS Service.

Practice Areas:
✅ Docker multi-service apps
✅ Terraform ECS, ECR, IAM, ALB
✅ GitHub → ECS Deployments

4. Kubernetes on AWS EKS with Terraform

Goal: Deploy a microservices app to EKS using Terraform for infra & GitHub Actions for CI/CD.

Stack:

App: Python/Node.js API + frontend (React).

Infra: Terraform → EKS Cluster, Node Groups, IAM roles.

Deployment: Kubernetes manifests (YAML) applied via GitHub Actions.

Steps:

Write Dockerfiles for frontend & backend.

Push to DockerHub/ECR.

Write Terraform code → create EKS cluster.

Deploy app via K8s manifests (Deployment, Service, Ingress).

Use GitHub Actions:

Build & push images.

Apply manifests with kubectl.

Practice Areas:
✅ Docker + Kubernetes
✅ Terraform EKS
✅ GitHub CI/CD to Kubernetes

5. Monitoring Stack on AWS (Prometheus + Grafana in Docker)

Goal: Deploy a monitoring stack with Docker Compose on AWS EC2 via Terraform.

Stack:

Infra: Terraform → EC2 instance with security groups.

Monitoring: Docker Compose → Prometheus + Grafana containers.

CI/CD: GitHub Actions → Build Docker images → Deploy to EC2.

Steps:

Write a docker-compose.yml with Prometheus + Grafana.

Use Terraform to provision EC2.

GitHub Actions → SCP docker-compose.yml → SSH → docker-compose up -d.

Practice Areas:
✅ Infra automation with Terraform
✅ Monitoring setup in Docker
✅ GitHub CI/CD → remote deploy
