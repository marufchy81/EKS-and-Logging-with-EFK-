# Three-tier Application Deployment on AWS EKS with Logging using EFK Stack
Author: **Maruf Chowdhury**  
Date: **July 2025**
---
## 📌 Project Overview
This project demonstrates the deployment of a **Three-tier web application** on **Amazon EKS (Elastic Kubernetes Service)** following **DevOps best practices**. It includes secure infrastructure provisioning, container orchestration, and centralized logging using the **EFK stack (Elasticsearch, Fluentd, Kibana)**.
---
## 🧱 Architecture 
### 🔹 Tiered Structure:
- **Frontend**: React.js or Angular served via Nginx
- **Backend**: Node.js or Spring Boot API services
- **Database**: MySQL (deployed via Amazon RDS or Kubernetes StatefulSet)

### 🔹 Logging:
- **Elasticsearch**: Stores and indexes logs
- **Fluentd**: Collects and ships logs from pods
- **Kibana**: Visualizes logs for debugging and insights
### 🔹 Infrastructure:
- **EKS (managed Kubernetes)**
- **VPC with public/private subnets**
- **IAM roles for fine-grained access control**
- **Load Balancer Controller for ingress management**
---
## 🛠️ Tools & Technologies
| Category      | Tool/Service             |
|---------------|--------------------------|
| IaC           | Terraform / eksctl        |
| Container     | Docker                    |
| CI/CD         | Jenkins / GitHub Actions  |
| Orchestration | Kubernetes (EKS)          |
| Logging       | EFK Stack (Elastic, Fluentd, Kibana) |
| Monitoring    | Prometheus + Grafana (optional) |
| Security      | IAM, RBAC, TLS, Secrets   |
---
## 🚀 Deployment Steps
1. **Infrastructure Setup**
   - Provision EKS using Terraform or eksctl
   - Configure VPC, subnets, and node groups
   - Setup IAM roles for service accounts
2. **App Deployment**
   - Build & push Docker images to Amazon ECR
   - Apply Kubernetes manifests:
     - `frontend-deployment.yaml`
     - `backend-deployment.yaml`
     - `mysql-statefulset.yaml`
3. **Ingress Configuration**
   - Install AWS Load Balancer Controller
   - Setup Ingress with SSL and host-based routing
4. **EFK Logging Setup**
   - Deploy Elasticsearch via Helm
   - Configure Fluentd DaemonSet for log shipping
   - Deploy Kibana and expose via Ingress
---
## 📊 Visuals (Attach if needed)
- EKS Node and Pod Layout
- EFK Flow Diagram
- Kibana Dashboard Example
- CI/CD Pipeline Example
---
## ✅ Best Practices Followed
- Namespaces for isolation
- Backend autoscaling
- Secure Secrets via AWS Secrets Manager
- Centralized logging for all workloads
- Helm used for third-party deployments
- Proper RBAC and IAM configurations
--- 
## 📂 Repository Structure -EKS Infrastructure (IaC)
 ├── terraform/                 
├── kubernetes/
│   ├── frontend/
│   ├── backend/
│   ├── database/
│   └── ingress/
├── efk/
│ ├── elasticsearch/
│ ├── fluentd/
│ └── kibana/
├── ci-cd/ # Jenkins/GitHub Actions files
├── README.md
yamlCopyEdit---## 🤝 Author**Maruf Chowdhury**DevOps Engineer | Cloud Native Enthusiast📧 maruf.chowdhury@example.com🔗 [LinkedIn](https://www.linkedin.com/in/maruf-chowdhury)---## 🔭 Future Improvements- Add Prometheus + Grafana monitoring stack - Introduce Istio for service mesh - Enable autoscaling via KEDA - Add centralized tracing with Jaeger---
 
 
