# 🚀 Dockerized Node.js + MongoDB Student Signup App

A beginner-friendly full-stack application built using **Node.js**, **Express.js**, **MongoDB**, and **Docker**.

This project was created to learn:
- Docker fundamentals
- Docker commands
- Docker Compose
- MongoDB containers
- Docker volumes
- Docker networking
- Containerizing Node.js applications

---

# 📌 Project Overview

This is a simple student signup application for XYZ University.

Users can:
- Open the signup page
- Enter email, username, and password
- Submit the form
- Store user data in MongoDB database

The entire application runs using Docker containers.

---

# 🛠️ Technologies Used

- Node.js
- Express.js
- MongoDB
- Mongo Express
- Docker
- Docker Compose
- HTML
- CSS

---

# 📂 Project Structure

```bash
project-folder/
│
├── public/
│   ├── index.html
│   └── style.css
│
├── server.js
├── Dockerfile
├── mongodb.yaml
├── package.json
└── README.md
```

---

# 🎨 Frontend Explanation

The frontend is created using HTML and CSS.

## Features
- Student signup form
- Input fields:
  - Email
  - Username
  - Password
- Submit button
- Simple responsive styling

The form sends data to:

```bash
POST /addUser
```

using Express backend.

---

# ⚙️ Backend Explanation

The backend is built using Node.js and Express.js.

## Backend Features
- Serves static frontend files
- Handles form submission
- Connects with MongoDB
- Stores user data
- Fetches all users from database

## API Routes

| Route | Method | Purpose |
|---|---|---|
| `/addUser` | POST | Add new user |
| `/getUsers` | GET | Fetch all users |

---

# 🐳 Docker Setup

This project uses 3 containers:

| Container | Purpose |
|---|---|
| Node.js App | Backend server |
| MongoDB | Database |
| Mongo Express | Database dashboard |

---

# 🐳 Dockerfile Explanation

The Dockerfile is used to create a Docker image for the Node.js application.

## Dockerfile Instructions Used

| Instruction | Purpose |
|---|---|
| FROM | Base image |
| ENV | Environment variables |
| COPY | Copy project files |
| RUN | Execute commands |
| CMD | Start application |

---

# 🗄️ MongoDB Setup

MongoDB runs inside Docker container.

Mongo Express is used to manage database visually.

## Mongo Express URL

```bash
http://localhost:8081
```

---

# 💾 Docker Volumes

Docker volumes are used for persistent MongoDB storage.

Purpose:
- Prevent data loss
- Keep database safe after container deletion

Example:

```yaml
volumes:
- /c/Users/AdminName/Desktop/data:/data/db
```

---

# 🌐 Docker Networking

Docker Compose automatically creates a shared network.

Containers communicate using service names.

Example:

✅ Correct:
```bash
mongodb://adminName:password@mongo:27017
```

❌ Wrong:
```bash
mongodb://adminName:password@localhost:27017
```

---

# ▶️ How to Run Project

## Step 1: Build Docker Image

```bash
docker build -t docker-testapp:1.0 .
```

---

## Step 2: Run MongoDB Services

```bash
docker compose -f mongodb.yaml up -d
```

---

## Step 3: Run Node.js Application

```bash
docker run -p 5050:5050 docker-testapp:1.0
```

---

# 🌍 Application URLs

## Node.js App

```bash
http://localhost:5050
```

## Mongo Express

```bash
http://localhost:8081
```

---

# 📚 Docker Commands Learned

---

## 🔹 Basic Docker Commands

| Command | Purpose |
|---|---|
| `docker` | Show Docker commands |
| `docker images` | Show all images |
| `docker ps` | Show running containers |
| `docker ps -a` | Show all containers |
| `docker pull hello-world` | Download image |
| `docker run hello-world` | Run container |
| `docker run -it hello-world` | Run interactive container |
| `docker start CONTAINER_ID` | Start container |
| `docker stop CONTAINER_ID` | Stop container |
| `docker rm CONTAINER_ID` | Remove container |
| `docker rmi IMAGE_ID` | Remove image |

---

## 🔹 Running Containers

| Command | Purpose |
|---|---|
| `docker run -d IMAGE_NAME` | Run container in background |
| `docker run --name mycontainer -d IMAGE_NAME` | Run container with custom name |
| `docker run -p8080:3306 IMAGE_NAME` | Port mapping |

---

## 🔹 Troubleshooting Commands

| Command | Purpose |
|---|---|
| `docker logs CONTAINER_ID` | View container logs |
| `docker exec -it CONTAINER_ID /bin/bash` | Open bash terminal |
| `docker exec -it CONTAINER_ID /bin/sh` | Open shell terminal |
| `docker network ls` | View Docker networks |

---

## 🔹 Docker Compose Commands

| Command | Purpose |
|---|---|
| `docker compose` | Docker Compose commands |
| `docker compose -f mongodb.yaml up -d` | Start containers |

---

## 🔹 Docker Build Commands

| Command | Purpose |
|---|---|
| `docker build -t docker-testapp:1.0 .` | Build Docker image |

---

## 🔹 DockerHub Commands

| Command | Purpose |
|---|---|
| `docker login` | Login to DockerHub |
| `docker push punit011/testappdocker` | Push image to DockerHub |

---

# 💾 Docker Volumes Learned

| Command | Purpose |
|---|---|
| `docker volume ls` | List volumes |
| `docker volume create VOL_NAME` | Create volume |
| `docker volume rm VOL_NAME` | Remove volume |
| `docker volume prune` | Remove unused volumes |

---

# 📁 Types of Docker Volumes Learned

## 1️⃣ Named Volumes

```bash
docker run -v VOL_NAME:/CONT_DIR
```

Purpose:
- Docker manages storage

---

## 2️⃣ Anonymous Volumes

```bash
docker run -v /MOUNT_PATH
```

Purpose:
- Temporary storage

---

## 3️⃣ Bind Mounts

```bash
docker run -v HOST_DIR:CONT_DIR
```

Windows Example:

```bash
docker run -it -v "C:\Users\AdminName\Desktop\data:/test/data" ubuntu
```

Purpose:
- Connect local folder with container folder

---

# 🌐 Docker Networks Learned

| Network Type | Purpose |
|---|---|
| Bridge | Default Docker network |
| Host | Uses host network |
| Null | No network access |

---

# 🧠 What I Learned

Through this project I learned:

- Docker basics
- Docker commands
- Docker images and containers
- Docker Compose
- MongoDB container setup
- Docker networking
- Docker volumes
- Bind mounts
- Persistent storage
- Node.js containerization
- Multi-container applications
- Connecting backend with MongoDB
- Using Mongo Express
- Uploading images to DockerHub
