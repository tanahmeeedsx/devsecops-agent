# DevSecOps Agent — AI-Powered Container & Cloud Security Platform

<p align="center">
  <img src="https://img.shields.io/badge/AI-Powered-7C3AED?style=for-the-badge&logo=openai&logoColor=white" alt="AI Powered" />
  <img src="https://img.shields.io/badge/DevSecOps-Security%20Automation-176B87?style=for-the-badge" alt="DevSecOps" />
  <img src="https://img.shields.io/badge/Multi--Cloud-AWS%20%7C%20GCP%20%7C%20Azure-232F3E?style=for-the-badge&logo=icloud&logoColor=white" alt="Multi Cloud" />
</p>

<p align="center">
  An intelligent security operations dashboard for container inspection, vulnerability scanning, cloud infrastructure visibility, and AI-assisted remediation.
</p>

<p align="center">
  <a href="https://github.com/tanahmeeedsx/devsecops-agent">Repository</a> ·
  <a href="https://github.com/tanahmeeedsx/devsecops-agent/issues">Issues</a>
</p>

---

## Technology Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=python,javascript,css,docker,aws,git,github&theme=dark" alt="Python, JavaScript, CSS, Docker, AWS, Git and GitHub" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Trivy-Vulnerability%20Scanning-1904DA?style=flat-square" alt="Trivy" />
  <img src="https://img.shields.io/badge/Docker%20Compose-Container%20Orchestration-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker Compose" />
  <img src="https://img.shields.io/badge/GitHub%20Actions-CI%2FCD-2088FF?style=flat-square&logo=githubactions&logoColor=white" alt="GitHub Actions" />
  <img src="https://img.shields.io/badge/AWS%20SSM-Remote%20Operations-FF9900?style=flat-square&logo=amazonaws&logoColor=white" alt="AWS Systems Manager" />
</p>

## Overview

DevSecOps Agent brings container security, infrastructure inspection, and AI-assisted analysis into a centralized dashboard. It helps engineers investigate vulnerabilities, inspect runtime health, review cloud configurations, and understand potential security risks.

## Architecture

```mermaid
flowchart TB
    USER["DevOps / Security Engineer"]
    UI["Web Dashboard<br/>JavaScript · CSS"]
    API["Python Backend API"]

    subgraph CONTAINERS["Container Security"]
        DOCKER["Docker Engine"]
        INSPECT["Runtime Inspection<br/>Logs · Health · Resources"]
        TRIVY["Trivy<br/>Image Vulnerability Scanning"]
    end

    subgraph CLOUD["Cloud Infrastructure"]
        AWS["AWS APIs"]
        SSM["AWS Systems Manager"]
        EC2["EC2 Docker Containers"]
        ECS["ECS / ECR"]
        STORAGE["S3 · IAM · Security Groups"]
    end

    AI["AI Analysis"]
    REPORT["Findings & Remediation Reports"]

    USER --> UI
    UI <--> API
    API --> DOCKER
    DOCKER --> INSPECT
    API --> TRIVY
    API --> AWS
    API --> SSM
    SSM --> EC2
    AWS --> ECS
    AWS --> STORAGE
    INSPECT --> AI
    TRIVY --> AI
    API --> AI
    AI --> REPORT
    REPORT --> UI
```

## Core Features

- **Container Inspection** — View container status, logs, health checks, CPU and memory usage.
- **Vulnerability Scanning** — Scan container images with Trivy to identify known vulnerabilities.
- **Cloud Security** — Inspect supported AWS resources, including EC2, ECS, ECR, S3, IAM and security groups.
- **Remote EC2 Operations** — Inspect Docker containers on EC2 through AWS Systems Manager (SSM).
- **AI-Assisted Analysis** — Interpret findings and generate security insights and remediation reports.
- **Unified Dashboard** — Access container diagnostics and supported cloud security workflows from one interface.

## CI/CD & Deployment

The GitHub Actions workflow automates the application's build and deployment process.

1. Builds the backend and frontend Docker images.
2. Authenticates to AWS using GitHub Actions OIDC.
3. Sends a deployment command to EC2 through AWS Systems Manager.
4. Pulls the latest code and rebuilds services using Docker Compose.

## Repository Structure

```text
devsecops-agent/
├── .github/workflows/
│   └── deploy.yml
├── backend/
├── frontend/
├── docs/
├── prompts/
├── docker-compose.yml
├── .env.example
├── DOCKER-RUNBOOK.md
└── .gitignore
```

## Security Focus

- Container vulnerability detection
- Infrastructure and runtime visibility
- Cloud configuration inspection
- OIDC-based AWS authentication for CI/CD
- AI-assisted security analysis and remediation guidance

## Project Vision

To make infrastructure security more observable and actionable by combining container diagnostics, cloud security inspection, vulnerability intelligence, and AI-assisted remediation in one platform.

---

<p align="center">
  <a href="https://github.com/tanahmeeedsx">Tanjim Ahmed</a>
</p>

<p align="center">
  <sub>Secure Infrastructure · Intelligent Automation · Continuous Security</sub>
</p>
