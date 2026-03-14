# Go Web Application – DevOps GitOps CI/CD Project

This project demonstrates a **production-style CI/CD pipeline** for a Go web application deployed on Kubernetes using **GitOps principles**.

The pipeline automatically builds, tests, containerizes, and deploys the application whenever new code is pushed.

---

## Architecture

Developer → GitHub → GitHub Actions → DockerHub → Helm → ArgoCD → Kubernetes (EKS)

---

## Tech Stack

* Golang (web application)
* Docker
* Kubernetes
* Helm
* ArgoCD (GitOps CD)
* GitHub Actions (CI)
* AWS EKS
* NGINX Ingress

---

## CI/CD Workflow

1. Developer pushes code to GitHub
2. GitHub Actions pipeline triggers
3. Application is built and tested
4. Docker image is built and pushed to DockerHub
5. Helm chart image tag is updated automatically
6. ArgoCD detects the change
7. Kubernetes cluster deploys the new version

---

## Repository Structure

```
go-web-app
├── main.go
├── Dockerfile
├── helm/
│   └── go-web-app-chart
├── k8s/
├── .github/workflows/
│   └── ci.yaml
```

---

## How to Run Locally

```
go run main.go
```

Application runs on:

```
http://localhost:8080/home
```

---

## Kubernetes Deployment

The application is deployed using **Helm charts** and managed by **ArgoCD GitOps**.

```
kubectl get pods
kubectl get svc
kubectl get ingress
```

---

## DevOps Features Implemented

* Automated CI pipeline
* Docker containerization
* Kubernetes deployment
* Helm packaging
* GitOps deployment with ArgoCD
* Automated image versioning
* Infrastructure automation ready for AWS EKS

---

## Future Improvements

* Multi-environment deployments (dev/staging/prod)
* Observability with Prometheus & Grafana
* Canary deployments
* Terraform infrastructure automation

---

## Author

Anushri Garg
DevOps / Cloud Enthusiast
