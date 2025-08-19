# QR Maker – Django with CI/CD (Docker + Kubernetes)

A simple yet powerful **QR Code Generator Web Application** built with Django, containerized with Docker, and production-ready with Kubernetes.  
This project demonstrates how to build, deploy, and scale a Python-based web application with modern DevOps practices.

---

## 🚀 Features

### 🖥️ Application (QR Maker)
- Generate QR codes for text, URLs, or any custom input.
- Download QR codes as PNG.
- History of generated QR codes (per user session).
- Django-based web UI with Bootstrap.

### ⚙️ DevOps / CI-CD
- **Dockerized** Django app for consistent local & production environments.
- **Docker Compose** for easy multi-service setup (app + database + nginx).
- **Kubernetes deployment** YAMLs for scalable production deployment.
- **CI/CD pipeline (GitHub Actions / Jenkins / CircleCI)** to automate build & deploy.
- **SSL-ready Nginx reverse proxy** for HTTPS production setup.

---

## 📂 Project Structure

qrmaker-django/
│── exampleapp/ # Django QR maker application
│── req/ # Python requirements
│── config/ # Nginx config files
│── ssl/ # SSL certificates
│── docker-compose.yml # Local dev orchestration
│── Dockerfile # App container
│── k8s/ # Kubernetes manifests
└── README.md


---

## 🔧 Quick Start (Local Development)

### 1. Clone the repository
```bash
git clone https://github.com/rajat1644/Qrmaker-django-docker-cicd-this.git
cd Qrmaker-django-docker-cicd-this
2. Build & Run with Docker
bash
Copy
Edit
docker build -t qrmaker:latest .
docker run -it -p 8000:8000 qrmaker:latest
Visit 👉 http://localhost:8000 to start generating QR codes.

🌐 Deploy with Docker Compose
bash
Copy
Edit
docker-compose up -d
☸️ Deploy with Kubernetes
bash
Copy
Edit
kubectl apply -f k8s/django-deployment.yml
kubectl apply -f k8s/django-volume.yml
Access your app at https://<your-domain> once ingress & SSL are configured.

🔄 CI/CD Setup
GitHub Actions / Jenkins pipeline runs on every commit:

Build Docker image

Push to DockerHub / GHCR

Deploy to Kubernetes cluster

Update pipeline files with your own DockerHub credentials and repo name.

🛠️ Tech Stack
Backend: Django, Python

Frontend: HTML, Bootstrap

Database: PostgreSQL (default: SQLite for dev)

Containerization: Docker, Docker Compose

Orchestration: Kubernetes

CI/CD: GitHub Actions / Jenkins

📸 Screenshots


🤝 Contributing
Contributions, issues, and feature requests are welcome!
Feel free to fork this repo and submit a PR.

📧 Contact
Author: rajat1644

Email: rajatbir1644@gmail.com

⭐ Support
If you like this project, give it a ⭐ on GitHub — it helps a lot!



---

👉 Want me to also prepare a **ready-to-use `.github/workflows/ci.yml` GitHub Actions file** so your
