# ☁️ Cloud-DevOps: Scalable Infrastructure & Container Security
## Overview
This repository documents the transition from manual provisioning to automated, code-driven cloud environments. It covers the full DevOps lifecycle: from containerizing applications with Docker, to orchestrating them at scale with Kubernetes, and provisioning the underlying cloud fabric with Terraform. Every project is documented with a focus on Security & Observability, including incident runbooks and telemetry integration.

## 🛠️ Technical Stack
**Orchestration:** Kubernetes (Deployments, StatefulSets, DaemonSets, HPA)

**Containerization:** Docker (Multi-stage builds, Port Mapping, Layer Optimization)

**Infrastructure as Code (IaC):** Terraform (HCL, State Management, Azure Provider)

**Cloud Registries:** Google Artifact Registry, IBM Cloud Container Registry (ICR)

**Platforms:** Microsoft Azure, IBM Cloud, Google Cloud Platform (GCP)

## 🏗️ Infrastructure & Orchestration Modules
### 1. Infrastructure as Code (Terraform & Azure)
**Objective:** Automated the deployment of cloud resources to Microsoft Azure using Terraform.

**IaC Principles:** Used HashiCorp Configuration Language (HCL) to define resource groups and networking components.

**State Management:** Managed infrastructure consistency using terraform.tfstate to track resource lifecycles.

**Automation:** Transitioned from manual portal configurations to a Plan → Apply execution workflow.

### 2. Containerization Lifecycle (Docker)
**Objective:** Built and published custom Node.js application images to private cloud registries.

**Image Engineering:** Authored Dockerfiles using multi-stage builds to reduce attack surface and image size.

**Registry Management:** Authenticated and pushed images to IBM Cloud and Google Artifact Registry, managing versioning and tags.

**Portability:** Verified cross-environment consistency by pulling and running custom containers in fresh cloud shell environments.

### 3. Kubernetes Orchestration & Scaling
**Objective:** Deployed and managed production-grade workloads using Kubernetes (K8s).

**Workload Diversity:** Implemented Deployments for stateless apps, StatefulSets for persistent data, and DaemonSets for system-wide agents.

**Auto-Scaling:** Configured Horizontal Pod Autoscalers (HPA) to dynamically scale replicas based on CPU utilization thresholds (50%).

**Rolling Updates:** Managed application lifecycles by performing v1 to v2 rolling updates with the ability to rollback to previous revisions in seconds.

## 🛡️ The "DevSecOps" Edge
**Image Scanning:** Implemented CI checks to fail builds on high-severity vulnerabilities before registry ingestion.

**Pod Security:** Configured security contexts including non-root execution and read-only root filesystems to prevent container breakout.

**SOC Integration:** Mapped Kubernetes telemetry (Audit logs, Container logs, Syslogs) into Splunk and Falco for real-time threat detection.

**Incident Response:** Developed Tier-3 Runbooks specifically for containerized environments to handle pod crashes or unauthorized image execution.

## 🧠 Skills Demonstrated
**Cloud Architecture:** Designing modular, scalable systems across Azure, IBM, and GCP.

**Automation Engineering:** Reducing "Human-in-the-loop" errors through IaC and CI/CD logic.

**Cloud-Native Security:** Implementing runtime security and vulnerability management within the K8s ecosystem.

**Resource Efficiency:** Mastering HPA and Metrics-Server to optimize cloud spending and performance.
