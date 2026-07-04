# ☸️ Kubernetes GitOps Infrastructure Lab

![Kubernetes](https://img.shields.io/badge/Kubernetes-v1.36-326CE5?logo=kubernetes&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-v1.15-7B42BC?logo=terraform&logoColor=white)
![Helm](https://img.shields.io/badge/Helm-v4-0F1689?logo=helm&logoColor=white)
![ArgoCD](https://img.shields.io/badge/ArgoCD-GitOps-EF7B4D?logo=argo&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-Monitoring-E6522C?logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-Dashboards-F46800?logo=grafana&logoColor=white)

> **Production-style Kubernetes platform demonstrating Infrastructure as Code, GitOps, Helm packaging, Kubernetes security, and observability.**

---

## 🚀 Skills at a Glance

- Kubernetes
- Terraform
- Docker
- Helm
- Argo CD
- GitOps
- Prometheus
- Grafana
- RBAC
- NetworkPolicy
- YAML
- Git & GitHub

---

## ⚡ 10-Second Summary

A production-style Kubernetes platform lab using **Terraform, Kubernetes, Helm, Argo CD, Prometheus, and Grafana**.

This project demonstrates end-to-end Kubernetes platform engineering through:

- Infrastructure as Code with Terraform
- Kubernetes application deployment
- GitOps continuous delivery with Argo CD
- Helm chart packaging
- RBAC and NetworkPolicy security controls
- Prometheus monitoring
- Grafana dashboards for live cluster observability

![Argo CD Application Synced](screenshots/phase4-argocd-application-synced.png)

---

## 📖 Project Overview

This lab simulates a real-world cloud-native infrastructure workflow. It starts with local Kubernetes infrastructure, deploys an NGINX workload, connects the application to Argo CD for GitOps-based delivery, converts the app into a Helm chart, adds Kubernetes security controls, and finishes with Prometheus and Grafana monitoring.

The goal of the project is to demonstrate hands-on ability with Kubernetes operations, GitOps workflows, Helm packaging, infrastructure troubleshooting, and observability.

---

## 🏗️ Architecture

```text
                 GitHub Repository
                        │
                        ▼
                   Argo CD (GitOps)
                        │
                        ▼
                Kubernetes Cluster
                        │
        ┌───────────────┼───────────────┐
        ▼               ▼               ▼
      Helm          NGINX App      RBAC & Network Policies
                        │
                        ▼
                  Prometheus
                        │
                        ▼
                     Grafana
```

---

## 🛠️ Technologies Used

| Category | Tools |
|---|---|
| Infrastructure as Code | Terraform |
| Container Platform | Docker, Kubernetes, KIND |
| Kubernetes Management | kubectl |
| GitOps | Argo CD |
| Packaging | Helm |
| Application | NGINX |
| Security | RBAC, NetworkPolicy |
| Monitoring | Prometheus |
| Visualization | Grafana |
| Version Control | Git, GitHub |

---

## ✨ Key Features

- Built a Kubernetes environment using KIND
- Created Kubernetes namespaces, deployments, services, and endpoints
- Deployed NGINX into a dedicated namespace
- Configured Argo CD for GitOps deployment from GitHub
- Enabled automated sync and self-healing
- Converted Kubernetes manifests into a Helm chart
- Validated Helm templates with `helm template` and dry-run testing
- Added RBAC using ServiceAccount, Role, and RoleBinding
- Added NetworkPolicy for pod traffic control
- Installed Prometheus and Grafana using Helm
- Verified live Kubernetes metrics in Grafana dashboards

---

## 📂 Repository Structure

```text
.
├── charts/
│   └── nginx/
│       ├── Chart.yaml
│       ├── values.yaml
│       └── templates/
│           ├── deployment.yaml
│           └── service.yaml
├── manifests/
│   ├── namespace/
│   │   └── namespace.yaml
│   ├── nginx/
│   │   ├── deployment.yaml
│   │   └── service.yaml
│   └── security/
│       ├── serviceaccount.yaml
│       ├── role.yaml
│       ├── rolebinding.yaml
│       └── networkpolicy.yaml
├── terraform/
├── screenshots/
└── README.md
```

---

## 🔄 Deployment Workflow

1. 🛠️ Verify local tooling: Docker, kubectl, Helm, Terraform, Argo CD CLI, and Trivy
2. 🌍 Initialize and apply Terraform configuration
3. ☸️ Create a KIND Kubernetes cluster
4. 🚀 Deploy namespace, NGINX deployment, and Kubernetes service
5. 🔍 Verify pods, deployments, services, and endpoints
6. 🔄 Install Argo CD
7. 🔗 Connect Argo CD to the GitHub repository
8. ⚙️ Configure automated GitOps synchronization
9. 🩹 Demonstrate drift detection and self-healing
10. 📦 Convert Kubernetes manifests into a Helm chart
11. ✅ Validate Helm chart rendering
12. 🔒 Add RBAC and NetworkPolicy security controls
13. 📊 Install Prometheus and Grafana
14. 📈 Verify live Kubernetes metrics in Grafana

---

# 📸 Screenshots

## 1️⃣ Tooling Verification

The project begins by verifying the required DevOps and Kubernetes tooling.

![Tool Verification](screenshots/phase1-tool-verification.png)

---

## 2️⃣ Terraform Infrastructure

Terraform was initialized and used to manage infrastructure configuration.

### Terraform Init

![Terraform Init](screenshots/phase2-terraform-init.png)

### Terraform Plan

![Terraform Plan](screenshots/phase2-terraform-plan.png)

### Terraform Apply

![Terraform Apply](screenshots/phase2-terraform-apply.png)

---

## 3️⃣ Kubernetes Cluster

A local KIND Kubernetes cluster was created and verified.

### KIND Cluster Created

![KIND Cluster Created](screenshots/phase3-kind-cluster-created.png)

### Cluster Info

![Cluster Info](screenshots/phase3-cluster-info.png)

### Cluster Health

![Cluster Health](screenshots/phase3-cluster-health.png)

### Kubernetes Nodes

![Kubernetes Nodes](screenshots/phase3-kubectl-get-nodes.png)

---

## 4️⃣ NGINX Kubernetes Workload

An NGINX application was deployed using Kubernetes manifests.

### Deployment Running

![NGINX Deployment Running](screenshots/phase3-deployment-running.png)

### Workloads Running

![Kubernetes Workloads Running](screenshots/phase3-workloads-running.png)

### Service Created

![Kubernetes Service Created](screenshots/phase3-kubernetes-service-created.png)

### Service Connectivity Test

![Service Connectivity Test](screenshots/phase3-service-connectivity-test.png)

### Service Endpoints Verified

![Service Endpoints Verified](screenshots/phase3-service-endpoints.png)

---

## 5️⃣ Argo CD GitOps

Argo CD was installed and used to continuously synchronize the cluster with the GitHub repository.

### Argo CD Login

![Argo CD Login Page](screenshots/phase4-argocd-login-page.png)

### Argo CD Pods Running

![Argo CD Pods Running](screenshots/phase4-argocd-pods-running.png)

### Application Synced and Healthy

![Argo CD Application Synced](screenshots/phase4-argocd-application-synced.png)

---

## 6️⃣ GitOps Auto-Sync and Self-Healing

The deployment was manually changed to create drift, then Argo CD restored the desired state from Git.

### Auto Sync Scaling to 4 Replicas

![Auto Sync Scale to 4](screenshots/phase5-auto-sync-scale-to-4.png)

### Manual Drift: Scale to 1 Replica

![Manual Scale to 1](screenshots/phase6-manual-scale-to-1.png)

### Argo CD Self-Healing Back to 4 Replicas

![Argo CD Self Heal](screenshots/phase6-argocd-self-heal.png)

---

## 7️⃣ Helm Chart

The NGINX workload was converted into a Helm chart with `Chart.yaml`, `values.yaml`, and Kubernetes templates.

### Helm Dry Run

![Helm Dry Run](screenshots/phase6-helm-dry-run-success.png)

### Helm Template Rendered

![Helm Template Rendered](screenshots/phase6-helm-template-rendered.png)

---

## 8️⃣ Kubernetes Security

RBAC and NetworkPolicy controls were added to the Kubernetes environment.

Security manifests included:

- `ServiceAccount`
- `Role`
- `RoleBinding`
- `NetworkPolicy`

![Security Resources Verified](screenshots/phase6-security-resources-verified.png)

---

## 9️⃣ Monitoring and Observability

Prometheus and Grafana were installed to monitor the Kubernetes cluster.

### Monitoring Pods Running

![Monitoring Pods Running](screenshots/phase6-monitoring-pods-running.png)

### Grafana Login Successful

![Grafana Dashboard](screenshots/phase7-grafana-dashboard.png)

### Prometheus Data Source Connected

![Prometheus Data Source Success](screenshots/phase7-prometheus-datasource-success.png)

### Live Kubernetes Metrics in Grafana

![Grafana Kubernetes Dashboard](screenshots/phase7-grafana-kubernetes-dashboard.png)

---

## 🎯 Skills Demonstrated

- Kubernetes cluster administration
- Kubernetes Deployments, Services, Endpoints, and Namespaces
- Helm chart creation and template rendering
- GitOps deployment with Argo CD
- Automated sync and self-healing
- RBAC security configuration
- Kubernetes NetworkPolicy configuration
- Prometheus monitoring
- Grafana dashboarding
- Terraform infrastructure workflow
- Git and GitHub version control
- YAML configuration management
- CLI-based troubleshooting
- Infrastructure documentation

---

## ⭐ Technical Highlights

- Built and managed a local Kubernetes cluster using KIND
- Provisioned and managed infrastructure configuration with Terraform
- Deployed and managed containerized workloads using Kubernetes Deployments and Services
- Implemented GitOps continuous delivery using Argo CD with automated synchronization and self-healing
- Packaged Kubernetes resources into reusable Helm charts and validated templates before deployment
- Configured Kubernetes security using Namespaces, RBAC, and NetworkPolicies
- Installed and configured Prometheus and Grafana for cluster monitoring and observability
- Verified application health, service connectivity, endpoints, and cluster resources using Kubernetes CLI
- Troubleshot Kubernetes workloads, networking, Helm templates, GitOps synchronization, and monitoring configuration
- Documented the complete deployment workflow with architecture diagrams, screenshots, and technical documentation

---

## 📚 What I Learned

Through this project, I practiced building and operating a Kubernetes-based platform using modern infrastructure and DevOps tooling. I learned how GitOps keeps a cluster synchronized with Git, how Helm improves repeatable application packaging, how Kubernetes security controls can limit access and traffic, and how Prometheus and Grafana provide visibility into cluster health.

This project also strengthened my troubleshooting skills by requiring me to debug image errors, Argo CD sync issues, Helm template problems, service connectivity, port-forwarding, and monitoring setup.

---

## 🚧 Future Improvements

- Add GitHub Actions CI/CD validation
- Add Trivy container and manifest scanning
- Add Ingress Controller
- Add Cert-Manager with Let's Encrypt
- Add External DNS
- Add Horizontal Pod Autoscaler
- Add Loki log aggregation
- Deploy to EKS, AKS, or GKE
- Add production-grade alerting rules

---

## ✅ Final Result

This project demonstrates an end-to-end Kubernetes platform built using modern cloud-native tooling and DevOps practices.

It showcases practical experience with Infrastructure as Code, Kubernetes administration, GitOps, Helm packaging, RBAC, NetworkPolicies, Prometheus, Grafana, and infrastructure troubleshooting while following workflows commonly used in production environments.