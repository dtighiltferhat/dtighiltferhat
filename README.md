# Djamal Tighilt Ferhat — DevOps & Cloud Engineering Portfolio

**DevOps & Cloud Engineer | AWS Certified Solutions Architect | Kubernetes · Terraform · CI/CD · Observability**

📧 dtighiltferhat@gmail.com · 🔗 [LinkedIn](https://linkedin.com/in/djamal-tighilt-ferhat-983343110) · 📍 Sterling, VA · Open to Remote / Hybrid / On-site

---

## About This Portfolio

This portfolio documents hands-on DevOps and Cloud Engineering projects built across home lab environments. Each project reflects real tools, real architecture decisions, and real operational challenges — not tutorial exercises. All projects are available on GitHub at [github.com/dtighiltferhat](https://github.com/dtighiltferhat).

> **Note on professional experience:** I have 17 years of engineering experience across Charles Schwab, GEICO, Freddie Mac, and Wells Fargo. Professional project details are available upon request and described in my resume — they are not published here out of respect for client confidentiality and NDA obligations.

---

## Technical Stack

| Domain | Tools & Technologies |
|---|---|
| **Cloud** | AWS (EC2, VPC, IAM, RDS, S3, EKS, Lambda, DynamoDB, ALB, CloudWatch, CloudFormation) |
| **Containers** | Kubernetes · Docker · EKS · Helm |
| **IaC** | Terraform · CloudFormation · Ansible |
| **CI/CD** | Jenkins · GitHub Actions · Git · Maven |
| **Observability** | Prometheus · Grafana · AWS CloudWatch · Alertmanager |
| **Scripting** | Bash · Python |
| **AI & Emerging** | AI-assisted IaC validation · AI-powered anomaly detection · AWS AI Practitioner (in progress) |
| **Methodologies** | DevSecOps · SRE principles · Shift-left testing · Agile/Scrum |

---

## Projects

---

### 01 · Multi-Environment AWS Infrastructure — IaC Platform

> **Stack:** `Terraform` `AWS (EC2, VPC, RDS, S3, IAM, ALB)` `CloudFormation` `Git`
> **Repo:** [github.com/dtighiltferhat/aws-terraform-infra](https://github.com/dtighiltferhat/aws-terraform-infra)

Designed and deployed a fully modular, reusable Terraform-based AWS infrastructure spanning three isolated environments — DEV, STAGING, and PROD. The project simulates an enterprise-grade cloud platform with proper network segmentation, IAM role separation, state management via S3 with DynamoDB locking, and drift detection.

**Key highlights:**
- Modular Terraform structure with separate root modules per environment, enabling independent state management and environment promotion workflows
- VPC design with public/private subnets, NAT gateways, security groups, and NACLs — following AWS Well-Architected Framework principles
- IAM roles and policies enforcing least-privilege access across EC2, RDS, S3, and Lambda resources
- Remote state backend using S3 + DynamoDB locking to prevent concurrent state corruption
- Automated drift detection via scheduled Terraform plan runs integrated into CI/CD pipeline
- CloudFormation stack deployed in parallel to validate infrastructure parity between IaC tools

---

### 02 · Kubernetes Home Lab — Full Cluster Deployment & Operations

> **Stack:** `Kubernetes` `Docker` `Helm` `Prometheus` `Grafana` `Ansible`
> **Repo:** [github.com/dtighiltferhat/k8s-homelab](https://github.com/dtighiltferhat/k8s-homelab)

Built and operated a multi-node Kubernetes cluster from scratch, simulating a production-grade container orchestration environment. The lab covers the full lifecycle — cluster provisioning, workload deployment, scaling, observability, and failure recovery.

**Key highlights:**
- Provisioned a multi-node K8s cluster using kubeadm, with control plane and worker node separation
- Deployed containerized microservices applications using Kubernetes Deployments, Services, ConfigMaps, and Secrets
- Implemented Helm charts for repeatable, versioned application deployments across namespaces
- Set up cluster-wide observability using Prometheus and Grafana dashboards for real-time visualization of pod health, resource utilization, and node performance
- Configured Horizontal Pod Autoscaler (HPA) to simulate load-based scaling scenarios
- Used Ansible playbooks to automate cluster node configuration and kubeadm initialization — reducing setup time from hours to minutes
- Practiced failure recovery: simulated node failures, pod eviction, and cluster recovery procedures

---

### 03 · CI/CD Pipeline Automation — Jenkins & GitHub Actions

> **Stack:** `Jenkins` `GitHub Actions` `Docker` `Git` `Bash` `AWS S3`
> **Repo:** [github.com/dtighiltferhat/cicd-pipeline-lab](https://github.com/dtighiltferhat/cicd-pipeline-lab)

Built dual CI/CD pipelines — one using Jenkins and one using GitHub Actions — to automate build, test, and deployment workflows for a containerized application. Demonstrates end-to-end pipeline design including automated testing gates, Docker image build and push, and deployment to a target environment.

**Key highlights:**
- Jenkins pipeline with declarative Jenkinsfile stages: checkout → build → unit test → Docker build → push to registry → deploy
- GitHub Actions workflow with parallel jobs for linting, testing, and Docker image build — triggered on PR and main branch push
- Automated regression gate that blocks deployment if any test stage fails
- Docker image tagging strategy using Git commit SHA for traceability between code and deployed artifacts
- Secrets management using Jenkins credentials store and GitHub Actions encrypted secrets — no hardcoded credentials
- Deployment artifacts pushed to AWS S3 and versioned for rollback capability
- Webhook integration between GitHub and Jenkins for automatic pipeline triggering on code push

---

### 04 · Observability Stack — Prometheus, Grafana & CloudWatch

> **Stack:** `Prometheus` `Grafana` `AWS CloudWatch` `Alertmanager` `Docker Compose`
> **Repo:** [github.com/dtighiltferhat/observability-stack](https://github.com/dtighiltferhat/observability-stack)

Deployed a full observability stack combining Prometheus, Grafana, and AWS CloudWatch to monitor infrastructure health, application metrics, and log patterns. Built custom dashboards and alerting rules simulating real-world reliability monitoring.

**Key highlights:**
- Prometheus deployed via Docker Compose with custom scrape configurations targeting application endpoints, node exporters, and Kubernetes metrics
- Grafana dashboards built from scratch covering: CPU/memory utilization, request latency, error rates, pod health, and deployment status
- Alertmanager configured with alert routing rules — critical alerts route to email, warnings logged to Slack webhook
- AWS CloudWatch integration: custom metrics published via CloudWatch agent, log groups configured for application and infrastructure logs
- API health check monitoring with automatic alerting on endpoint failures or degraded response times
- Simulated a realistic on-call scenario: CPU spike → triggered alert → traced root cause through Grafana → resolved and documented

---

### 05 · Ansible Infrastructure Automation

> **Stack:** `Ansible` `Bash` `Python` `Linux` `AWS EC2`
> **Repo:** [github.com/dtighiltferhat/ansible-automation](https://github.com/dtighiltferhat/ansible-automation)

Developed a collection of Ansible playbooks for automated infrastructure configuration, environment setup, and application deployment across multiple Linux hosts — simulating enterprise DevOps configuration management workflows.

**Key highlights:**
- Playbooks for full server provisioning: package installation, user management, SSH key configuration, firewall rules, and service setup
- Role-based Ansible structure with reusable roles for web server, database, monitoring agent, and Docker installation
- Dynamic inventory configured against AWS EC2 instances using AWS tags for host grouping
- Idempotency testing — all playbooks verified to produce identical results on repeated runs
- Environment-specific variable files (dev/staging/prod) enabling safe targeting of different environments
- Integrated into CI/CD pipeline to trigger Ansible runs post-infrastructure provisioning via Terraform

---

## Certifications

| Certification | Issuer | Status |
|---|---|---|
| AWS Certified Solutions Architect – Associate | Amazon Web Services | ✅ Active |
| AWS Certified Cloud Practitioner | Amazon Web Services | 🔄 Renewal pending |
| AWS Certified AI Practitioner | Amazon Web Services | 🎯 In progress |

---

## Contact

- 📧 **Email:** dtighiltferhat@gmail.com
- 📞 **Phone:** (571) 314-7629
- 🔗 **LinkedIn:** [linkedin.com/in/djamal-tighilt-ferhat-983343110](https://linkedin.com/in/djamal-tighilt-ferhat-983343110)
- 💻 **GitHub:** [github.com/dtighiltferhat](https://github.com/dtighiltferhat)
- 📍 **Location:** Sterling, Virginia — Open to Remote · Hybrid · On-site

---

*Open to Senior DevOps Engineer, Cloud Engineer, SRE, and Platform Engineer roles across any industry where reliability and automation are taken seriously.*
