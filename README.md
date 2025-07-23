# 📝 TaskFlow
TaskFlow is a full-stack task management application built with ASP.NET Core (.NET 9) and AngularJS, designed to showcase clean architecture, authentication, and role-based access control.

It supports:
[ ] User registration and login with email verification
[ ] Public and secured API endpoints
[ ] Role-based access control
[ ] Dockerized deployment

## 🚀 Features
🗂 Project & Task Management API

🔒 JWT Authentication with email verification

👥 Role-based authorization

🖥 AngularJS frontend with public and secured pages

🐳 Dockerized for easy local development

## 🛠 Tech Stack
Backend: ASP.NET Core (.NET 9), Entity Framework Core, SQLite (PostgreSQL-ready), CQRS, MediatR

Frontend: AngularJS 1.x, Bootstrap, JWT token management

DevOps: Docker, Docker Compose

## 📦 Getting Started
### ⚙️ Prerequisites
.NET 9 SDK

Node.js (v14+)

Docker

### 🖥 Run Locally
#### Clone the repository:
git clone https://github.com/<your-username>/taskflow.git

cd taskflow

#### Run with Docker:
docker-compose up --build

Backend: http://localhost:5000

Frontend: http://localhost:4200

## 🔑 Authentication & Roles
New users must verify their email before logging in (see console for link).

Predefined roles:

Admin – Full access to application but not data

Manager - Full access to data but not application

User – Limited access (can manage own tasks)

Guest – Read-only

## 🌐 API Endpoints
| Method | Endpoint | Description | Auth Required |
| ------ | -------- | ----------- | ------------- |
| POST | /api/auth/register | Register a new user |	❌ |
| POST | /api/auth/login | Login & get JWT token | ❌ |
| GET | /api/public/projects | Get public projects | ❌ |
| GET | /api/projects | Get projects for logged-in user | ✅ |
| POST | /api/projects | Create new project | ✅ |

## 🐳 Docker Setup
Build & Run

docker-compose up --build

Visit:
API: http://localhost:5000/swagger

Frontend: http://localhost:4200

## 👥 Contributing
Want to extend TaskFlow? Fork this repository and submit a pull request.

## 📜 License
This project is licensed under the MIT License.
