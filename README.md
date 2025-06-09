# 🚀 CI/CD Pipeline with GitHub Actions & Docker

This project demonstrates a complete **CI/CD pipeline** using **GitHub Actions** and **Docker** without relying on cloud platforms. It includes a simple Node.js web app, containerized with Docker, and automatically built and deployed using GitHub Actions.

---

## 📌 Project Features

- ✅ Simple Express.js app (returns "Hello, Docker!")
- 🐳 Docker containerization with `Dockerfile`
- ⚙️ CI/CD pipeline with GitHub Actions
- 📦 Docker image pushed to Docker Hub
- 🧪 Local deployment using Docker or Docker Compose

---

## 📁 Project Structure

```
ci-cd-node-docker-app/
├── .github/workflows/ci.yml       # GitHub Actions workflow
├── Dockerfile                     # Docker configuration
├── docker-compose.yml             # Local deployment script
├── app.js                         # Express.js server code
├── package.json                   # Project metadata
```

---

## 🚀 Quick Start

### 1. Clone the Repo
```bash
git clone https://github.com/your-username/ci-cd-node-docker-app.git
cd ci-cd-node-docker-app
```

### 2. Run Locally with Docker Compose
```bash
docker-compose up
```
Visit: [http://localhost:3000](http://localhost:3000)

---

## 🔧 GitHub Actions CI/CD Setup

### ➤ Step 1: Docker Hub Access Token
- Go to [Docker Hub Security Settings](https://hub.docker.com/settings/security)
- Generate a new **Access Token** with `Read & Write` permissions

### ➤ Step 2: Add Secrets in GitHub Repo
Go to: `GitHub Repo → Settings → Secrets and variables → Actions`  
Add the following secrets:
- `DOCKER_USERNAME` = your Docker Hub username
- `DOCKERHUB_TOKEN` = the token you copied

### ➤ Step 3: Push Code and Trigger CI
```bash
git add .
git commit -m "Initial CI/CD setup"
git push origin main
```

GitHub Actions will:
- Build the Docker image
- Push it to Docker Hub

---

## 🔍 Accessing the Docker Image

After a successful workflow run:
```bash
docker pull your-username/ci-cd-node-docker-app:latest
docker run -p 3000:3000 your-username/ci-cd-node-docker-app
```

Visit: [http://localhost:3000](http://localhost:3000)

---

## 📦 Docker Hub Repo
You can find the pushed image at:  
👉 `https://hub.docker.com/repository/docker/<your-username>/ci-cd-node-docker-app`

---

## 🧠 Learnings & Concepts Used

- CI/CD Pipeline Design
- GitHub Actions Workflow
- Docker & Docker Compose
- Docker Hub Authentication
- Automated Build and Deploy

---
## OUTPUTS
1. Local app running in browser
2. Terminal showing container logs
3. GitHub Actions success logs
4. Docker Hub image listing
---

## 🧾 License
This project is open-sourced under the [MIT License](LICENSE).

---

## 👤 Author
**KALKIESHWAR**  
Passionate about DevOps and Automation 🚀
