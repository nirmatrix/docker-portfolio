# 🚀 Portfolio CI/CD with Docker + GitHub Actions

A simple portfolio website built with HTML, CSS, and JavaScript, containerized using Docker, and automated through a GitHub Actions CI/CD pipeline.

This project demonstrates a complete DevOps workflow from source code management to container image delivery.

---

## 📌 Project Overview

The application is a static portfolio website served through Nginx inside a Docker container.

The CI/CD pipeline automatically builds and publishes a Docker image whenever changes are pushed to the repository.

---

## 🧠 Tech Stack

- HTML5
- CSS3
- JavaScript (Vanilla)
- Docker
- Nginx
- GitHub Actions
- Docker Hub

---

## ✨ Features

- Responsive portfolio website
- Multi-page navigation
  - Home
  - About
  - Projects
  - Contact
- Dockerized application using Nginx
- Automated CI/CD workflow
- Docker image build and push to Docker Hub
- Version-controlled source code using GitHub

---

## 📂 Project Structure

```text
.
├── index.html
├── about.html
├── projects.html
├── contact.html
├── css/
├── js/
├── images/
├── Dockerfile
├── .github/
│   └── workflows/
│       └── ci-cd.yml
└── README.md
```

---

## 🐳 Docker Setup

### Build the Docker Image

```bash
docker build -t portfolio-app .
```

### Run the Container

```bash
docker run -d -p 8081:80 portfolio-app
```

### Access the Application

```text
http://localhost:8081
```

---

## 🔁 CI/CD Pipeline

The GitHub Actions workflow performs the following steps:

1. Trigger on push to the main branch
2. Checkout source code
3. Build Docker image
4. Login to Docker Hub
5. Push image to Docker Hub

### Pipeline Flow

```text
Developer Push
      │
      ▼
GitHub Repository
      │
      ▼
GitHub Actions
      │
      ▼
Docker Image Build
      │
      ▼
Docker Hub Login
      │
      ▼
Docker Image Push
      │
      ▼
Ready for Deployment
```

---

## ⚙️ GitHub Actions Workflow

The workflow is located in:

```text
.github/workflows/
```

It automates the Docker image build and publishing process, enabling continuous integration and delivery.

---

## 🔐 Required Secrets

The following GitHub repository secrets are required:

| Secret          | Description		    |
|-----------------|-------------------------|
| DOCKER_USERNAME | Docker Hub username     |
| DOCKER_PASSWORD | Docker Hub access token |

---

## 🎯 Learning Objectives

This project was created to practice and demonstrate:

- Docker containerization
- Nginx web hosting
- CI/CD automation
- GitHub Actions workflows
- Docker Hub integration
- DevOps fundamentals

---

## 🚀 Future Improvements

- Deploy to AWS EC2
- Deploy using Kubernetes
- Configure HTTPS with Nginx
- Add automated testing
- Add image versioning and tagging
- Implement Infrastructure as Code (Terraform)

---

## 📥 Clone Repository

Clone the repository to your local machine:

```bash
git clone https://github.com/nirmatrix/docker-portfolio.git
```
```bash
cd docker-portfolio
```

## 👨‍💻 Author

Developed as a DevOps practice project to demonstrate containerization and CI/CD automation using Docker and GitHub Actions.

---

## ⭐ Acknowledgement

This project showcases a simple but practical implementation of modern DevOps practices by automating the build and delivery process of a containerized web application.
