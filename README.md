# Jenkins Docker CI/CD Pipeline Demo
This project demonstrates a basic Continuous Integration and Continuous Deployment (CI/CD) pipeline using **Jenkins**, **Docker**, and **GitHub** on an **AWS EC2** instance.
## 🚀 Objective
Automate the process of building and deploying a Dockerized Node.js application using Jenkins Pipeline on an EC2 instance.
---
## 🧰 Tech Stack
- **AWS EC2** (Ubuntu 22.04)
- **Jenkins**
- **Docker**
- **Git**
- **GitHub**
---
## 🏗️ Project Structure
```
jenkins-docker-demo/
│
├── Jenkinsfile          # Jenkins pipeline definition
├── Dockerfile           # Docker image build instructions
├── app.js               # Sample Node.js app
└── package.json         # Node.js dependencies
```
## ⚙️ Jenkins Pipeline Stages
1. **Checkout Code** – Pulls the latest code from GitHub.
2. **Build Docker Image** – Builds the application image using the Dockerfile.
3. **Run Docker Container** – Deploys the container locally on EC2.
## 🔐 Jenkins Setup Summary
- Installed Jenkins and Docker on EC2 instance.
- Configured Jenkins to run as a service.
- Added Jenkins user to the Docker group:
  sudo usermod -aG docker jenkins
- Created a Jenkins pipeline connected to GitHub via "Pipeline Script from SCM"
## 🔗 Live Jenkins URL (private
http://<your-ec2-public-ip>:8080
Make sure port **8080** is open in your EC2 **Security Group** settings.
## 👨‍💻 How to Use
# Clone the repo
git clone https://github.com/Santhoshreddy1818/jenkins-docker-demo.git
cd jenkins-docker-demo
# Build the Docker image manually (optional)
docker build -t jenkins-demo .
# Run the app manually (optional)
docker run -d -p 3000:3000 --name jenkins-demo jenkins-demo
## 📦 Sample Output
server running on http://localhost:3000
## ✍️ Author

**Santhosh Chada**  
[GitHub Profile](https://github.com/Santhoshreddy1818)
