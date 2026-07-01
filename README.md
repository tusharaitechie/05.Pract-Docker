# 🐳 Dockerizing an Application: From Code to Container

## 📌 Project Overview

This repository demonstrates the practical implementation of **Docker containerization** using a real-world project example.

The objective of this project is to understand how an application can be packaged, containerized, and deployed consistently across different environments using Docker.

This project covers the complete Docker workflow:

- Creating a Dockerfile
- Building Docker images
- Running applications inside containers
- Managing containers and images
- Tagging Docker images
- Publishing images to Docker Hub

---

# 🚀 Why Docker?

In traditional application deployment, developers often face issues like:

- "It works on my machine but not on another system"
- Dependency conflicts
- Environment configuration problems

Docker solves these problems by packaging:

- Application code
- Runtime environment
- Dependencies
- Configuration

into a portable container.

---

# 🏗️ Project Architecture

```
Developer Code
      |
      |
   Dockerfile
      |
      |
 Docker Build
      |
      |
 Docker Image
      |
      |
 Docker Container
      |
      |
 Application Running
```

---

# 📂 Repository Structure

```
05.Pract-Docker
│
├── Dockerfile
├── requirements.txt
├── app.py
└── README.md
```

---

# ⚙️ Prerequisites

Before running this project, install Docker:

Check Docker installation:

```bash
docker --version
```

Example:

```
Docker version 27.x.x
```

---

# 🐳 Docker Implementation Steps

## 1. Clone Repository

```bash
git clone https://github.com/tusharaitechie/05.Pract-Docker.git
```

Navigate into project:

```bash
cd 05.Pract-Docker
```

---

# 2. Build Docker Image

Create Docker image using Dockerfile:

```bash
docker build -t mlops-docker-demo .
```

### Explanation:

| Command | Purpose |
|---|---|
| docker build | Creates Docker image |
| -t | Assigns image name/tag |
| mlops-docker-demo | Image name |
| . | Current directory as build context |

---

# 3. Verify Docker Image

Check available images:

```bash
docker images
```

Output:

```
REPOSITORY              TAG
mlops-docker-demo       latest
```

---

# 4. Run Docker Container

Start container:

```bash
docker run mlops-docker-demo
```

If application exposes a port:

```bash
docker run -p 8000:8000 mlops-docker-demo
```

---

# 5. Check Running Containers

Running containers:

```bash
docker ps
```

All containers:

```bash
docker ps -a
```

---

# 6. Stop Container

```bash
docker stop <container_id>
```

Example:

```bash
docker stop abc123
```

---

# 7. Remove Container

```bash
docker rm <container_id>
```

---

# 8. Remove Docker Image

```bash
docker rmi mlops-docker-demo
```

---

# ☁️ Push Docker Image to Docker Hub

## Step 1: Login Docker Hub

```bash
docker login
```

Enter Docker Hub credentials.

---

## Step 2: Tag Docker Image

Docker Hub Username:

```
tnlabs
```

Tag image:

```bash
docker tag mlops-docker-demo tnlabs/mlops-docker-demo:latest
```

Verify:

```bash
docker images
```

Expected:

```
tnlabs/mlops-docker-demo   latest
```

---

## Step 3: Push Image

Upload image:

```bash
docker push tnlabs/mlops-docker-demo:latest
```

Now the Docker image is available on Docker Hub.

---

# 📥 Pull Image From Docker Hub

Anyone can download the image:

```bash
docker pull tnlabs/mlops-docker-demo:latest
```

Run:

```bash
docker run tnlabs/mlops-docker-demo:latest
```

---

# 🧰 Frequently Used Docker Commands

### Check Docker Version

```bash
docker --version
```

### List Images

```bash
docker images
```

### List Running Containers

```bash
docker ps
```

### View All Containers

```bash
docker ps -a
```

### Remove Unused Docker Resources

```bash
docker system prune
```

---

# 📚 Key Learnings

Through this project, I learned:

✅ Docker fundamentals  
✅ Containerization workflow  
✅ Dockerfile creation  
✅ Image building process  
✅ Container lifecycle management  
✅ Docker Hub integration  
✅ Deployment-ready application packaging  

---

# 🐳 Docker Hub Repository

Docker Image:

```
tnlabs/mlops-docker-demo:latest
```

---

# 👨‍💻 Author

**Tushar**

GitHub:
https://github.com/tusharaitechie

---

# ⭐ Conclusion

This project represents my hands-on learning of Docker and containerization concepts, focusing on creating reproducible and portable application environments.

Docker is a fundamental skill for modern software development, DevOps, and MLOps workflows.