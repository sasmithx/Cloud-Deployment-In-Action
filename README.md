
# Cloud Enabled Deployment In Action with AWS, GCP

🚀 This project demonstrates a cloud-enabled ☁️ microservices-based deployment using Spring Boot 🍃, React ⚛️, AWS 🟨, GCP 🔵, and Docker 🐳.
It showcases how to build 🛠️, containerize 📦, and deploy 🚢 backend services and a frontend application with cloud-managed 🌐 and self-hosted 🖥️ databases.

This repository contains four projects:

- course-service (Spring Boot + MySQL)
- student-service (Spring Boot + MongoDB)
- media-service (Spring Boot + Local file storage, can be extended to S3/MinIO)
- frontend-app (React + TypeScript)

## Backend Services

### 1. course-service
- Entity: Course(id, name, duration)
- Endpoints:
    - GET /courses
    - GET /courses/{id}
    - POST /courses
    - DELETE /courses/{id}
- Default port: 8081
- Configure MySQL settings

### 2. student-service
- Document: Student(registrationNumber, fullName, address, contact, email)
- Endpoints:
    - GET /students
    - GET /students/{id}
    - POST /students
    - DELETE /students/{id}
- Default port: 8082
- Configure MongoDB settings

### 3. media-service
- Resource: files
- Endpoints:
    - POST /files (multipart/form-data: file)
    - GET /files (list)
    - GET /files/{id} (fetch)
    - DELETE /files/{id} (delete)
- Default port: 8083
- Uses local disk storage at `./data/media` by default (override with env var `MEDIA_STORAGE_DIR`).

## Frontend (frontend-app)
- React + TypeScript + MUI + Axios + Vite app with 3 sections: Courses, Students, Media
- Scripts:
    - npm run dev (Vite dev server)
    - npm run build (TypeScript build + Vite build)
    - npm run preview (Preview built app)

## Build

- Backend: run `mvn -q -e -DskipTests package` at repo root to build services.
- Frontend: run `npm install` then `npm run dev` inside `frontend-app`.

---  

## ⚙️ Development Environment

In **development mode**:

* **MySQL** and **MongoDB** run inside Docker containers with persistent volumes.
* Backend services are started using the `dev` profile.

### Start MySQL (with volume)

```bash

docker run -d --name mysql -v mysql-data:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=mysql -p 15000:3306 mysql:lts
```

### Start MongoDB (with volume)

```bash

docker run --name mongo -v mongo-data:/data/db -e MONGO_INITDB_ROOT_USERNAME=root -e MONGO_INITDB_ROOT_PASSWORD=mongo -p 16000:27017 -d mongo:latest
```

Both containers will persist data in their respective Docker volumes (`mysql-data`, `mongo-data`).

---

## 📌 Built With

![Springboot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
[![React.js](https://img.shields.io/badge/React-000000?style=for-the-badge&logo=react&logoColor=61DAFB)](https://react.dev/)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
![NPM](https://img.shields.io/badge/NPM-%23000000.svg?style=for-the-badge&logo=npm&logoColor=white)
![MySQL](	https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)

## 📌 Deploy And Containerize

![AWS](https://img.shields.io/badge/AWS-000000?style=for-the-badge&logo=amazonaws&logoColor=FF9900)
![Google Cloud](https://img.shields.io/badge/Google_Cloud-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white)

---

##  <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Travel%20and%20places/High%20Voltage.png" style="width: 50px; height: 50px;" alt="">Demo Video

- [Watch Demo](https://drive.google.com/file/d/10DJfSJDkzuR5-c9kWxQ5wTiJiTg0Em9-/view?usp=sharing)

##  <img src="https://user-images.githubusercontent.com/74038190/216122003-1c7d9078-357a-47f5-81c7-1c4f2552e143.png" style="width: 50px; height: 50px;" alt="">Connecting Database Instances in AWS and GCP

- [View AWS, GCP Configurations](https://www.notion.so/Cloud-Deployment-In-Action-2631c3d19714802d8acde6264a28dad2?source=copy_link)

## Clone Project


```bash
  https://github.com/sasmithx/Cloud-Deployment-In-Action.git
```
## <img src="https://user-images.githubusercontent.com/74038190/216122069-5b8169d7-1d8e-4a13-b245-a8e4176c99f8.png" style="width: 50px; height: 50px;" alt="">License
This project is licensed under the MIT License - see the [MIT License](LICENSE) file for details.

<br>

<div align="center">
  <img src="https://img.shields.io/badge/AWS-000000?style=for-the-badge&logo=amazonaws&logoColor=FF9900" />
  <img src="https://img.shields.io/badge/Google_Cloud-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white" />
</div> <br>
