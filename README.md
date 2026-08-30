# End-to-End DevOps & SRE Deployment Pipeline

Production-ready microservices architecture deployment using AWS, Terraform, Docker, and Kubernetes (EKS).

---

## 🏗️ Architecture Overview
* **Infrastructure as Code:** Terraform for automated provisioning of VPC, EKS, and IAM.
* **Containerization:** Multi-stage Docker builds for microservices.
* **Orchestration:** Kubernetes (EKS) with Deployments, Services, and Ingress.
* **CI/CD:** Automated testing, container build, and deployment pipelines.
* **Monitoring:** Prometheus & Grafana for metrics; CloudWatch for centralized logging.

---

## 📂 Repository Structure
* \`src/\`: Microservices source code and Dockerfiles.
* \`terraform/\`: Terraform configurations for AWS infrastructure.
* \`k8s/\`: Kubernetes deployment manifests and service definitions.
* \`docs/\`: Architecture diagrams and deployment logs.

---

## 🚀 Getting Started

### Prerequisites
* AWS CLI configured with appropriate IAM permissions
* Terraform v1.5+
* Docker Engine
* kubectl

### Deployment Steps
1. **Provision Infrastructure:**
   \`\`\`bash
   cd terraform
   terraform init
   terraform plan
   terraform apply
   \`\`\`

2. **Build and Push Container Images:**
   \`\`\`bash
   docker build -t <your-repo>/recommendation:v1 src/recommendation/
   docker push <your-repo>/recommendation:v1
   \`\`\`

3. **Deploy to Kubernetes:**
   \`\`\`bash
   kubectl apply -f k8s/
   kubectl get pods -w
   \`\`\`

---

## 👤 Author
* **Avinash Ingle** - *SRE & DevOps Engineer*
