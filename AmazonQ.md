# Wanderlust CICD Project Documentation

This document provides an overview of the CI/CD implementation for the Wanderlust travel blog application.

## Project Overview

Wanderlust is a MERN stack travel blog application with a complete CI/CD pipeline implemented using:

- GitHub (Version Control)
- Docker (Containerization)
- Jenkins (CI)
- OWASP (Dependency check)
- SonarQube (Code Quality)
- Trivy (Filesystem Scan)
- ArgoCD (CD)
- Redis (Caching)
- AWS EKS (Kubernetes)
- Helm (Monitoring with Grafana and Prometheus)

## CI/CD Pipeline Flow

1. **CI Pipeline**: Builds and pushes Docker images to registry
2. **CD Pipeline**: Updates application versions in the deployment repository
3. **ArgoCD**: Automatically deploys updated applications to EKS cluster

## Infrastructure Setup

The project uses AWS EKS for Kubernetes orchestration with the following components:
- Jenkins Master and Worker nodes
- SonarQube for code quality analysis
- ArgoCD for GitOps-based deployments
- Prometheus and Grafana for monitoring

## Monitoring

The EKS cluster is monitored using Prometheus and Grafana, providing visibility into:
- Kubernetes component health
- Pod resource utilization
- Application performance metrics

## Security Measures

The pipeline includes several security checks:
- OWASP dependency scanning
- SonarQube code quality analysis
- Trivy container scanning

## Deployment Access

The application is accessible via NodePort services:
- Frontend: `<worker-node-ip>:31000`
- Backend: `<worker-node-ip>:31100`

## Maintenance

Regular updates and monitoring are required to ensure the application remains secure and performant.
