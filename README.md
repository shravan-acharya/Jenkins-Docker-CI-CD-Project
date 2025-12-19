# Jenkins Docker CI/CD Automation Project

A complete **CI/CD automation project** built using **Jenkins** and **Docker**, demonstrating real-world DevOps practices such as automated build, test, image publishing, and remote deployment. The project follows a multi-stage pipeline approach with job chaining and zero manual intervention.

---

## 🚀 Features

* End-to-end CI/CD pipeline using Jenkins
* Automated Docker image build and testing
* Docker image versioning and publishing to Docker Hub
* Remote deployment using SSH
* Job chaining for build → test → push → deploy
* Clean rollback by stopping and removing old containers

---

## 🛠️ Tech Stack

* **CI/CD Tool:** Jenkins
* **Containerization:** Docker
* **Programming Language:** Node.js (Express)
* **Testing:** Mocha, Supertest
* **Version Control:** Git, GitHub
* **Cloud/Servers:** Linux (AWS EC2 / Ubuntu)
* **Registry:** Docker Hub
* **Remote Access:** SSH

---

## ⚙️ CI/CD Pipeline Flow
GitHub Commit
>
docker-build
>
docker-test
>
docker-push
>
docker-deploy
>
Application Live on Remote Server



---

## 🔁 Jenkins Jobs Overview

### docker-build
* Pulls latest source code from GitHub
* Builds Docker image using Dockerfile
* Verifies image creation

### docker-test
* Runs container from the built image
* Ensures application starts successfully
* Cleans up old containers if present

### docker-push
* Tags the Docker image with version
* Pushes image to Docker Hub registry

### docker-deploy
* Connects to a remote server via SSH
* Pulls latest Docker image
* Stops and removes old container
* Deploys new container on the server

---

## 🧪 Testing

* Automated testing using **Mocha** and **Supertest**
* Tests executed before pushing Docker image
* Ensures only stable builds move to deployment

---

## 🔒 Security & Best Practices

* Jenkins user configured with Docker permissions
* Credentials managed via Jenkins Credentials Manager
* SSH-based secure remote deployment
* Separate CI server and deployment server
* Old containers cleaned before deployment

---

## 📊 Deployment Workflow

1. Developer pushes code to GitHub
2. Jenkins triggers the pipeline automatically
3. Docker image is built and tested
4. Image is pushed to Docker Hub
5. Remote server pulls and runs latest image
6. Application becomes live

---

## 🌟 Future Enhancements

* Convert freestyle jobs to Jenkinsfile (Pipeline as Code)
* Add email or Slack notifications
* Integrate Docker image scanning
* Deploy using Kubernetes (EKS)
* Add blue-green or canary deployment strategy

---

## Diagram 

![1_CH2R5552IjZCTqhgaBpXHw](https://github.com/user-attachments/assets/0b8c2a84-54d6-4254-9b14-43cfc876d34b)


## 📜 License

This project is licensed under the MIT License.

