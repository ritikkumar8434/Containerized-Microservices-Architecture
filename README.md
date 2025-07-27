# 🐳 Containerized Microservices Architecture with Flask, Docker Compose, PostgreSQL, and Redis

This project demonstrates a microservices-based backend architecture using:

- 🔹 **Flask** for REST API development
- 🟠 **PostgreSQL** for persistent data storage
- 🔵 **Redis** for in-memory caching
- 🐳 **Docker Compose** for container orchestration

Each component runs in its own container, and services communicate over a shared Docker network. [cite_start]This project was developed by Ritik Kumar Sahu.

---

<pre> ## 🗂️ Project Structure . ├── user-service/ # Handles user registration │ ├── app.py │ ├── Dockerfile │ └── requirements.txt ├── data-service/ # Fetches user data with Redis caching │ ├── app.py │ ├── Dockerfile │ └── requirements.txt ├── docker-compose.yml # Orchestrates all services ├── init.sql # Initializes the PostgreSQL database └── README.md </pre>
---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone [https://github.com/ritikkumar8434/Containerized-Microservices-Architecture.git](https://github.com/ritikkumar8434/Containerized-Microservices-Architecture.git)
cd microservices-docker-app
```
### 2. Build and Run All Services
 ```bash
 docker-compose up --build
 ```
## 🔗 Service Endpoints

# 🔗 Service Endpoints

| **Service**     | **Endpoint**                                   | **Description**                          |
|-----------------|------------------------------------------------|------------------------------------------|
| User Service    | `http://127.0.0.1:5000/register`               | Register a new user                      |
| Data Service    | `http://127.0.0.1:5001/user/<name>`            | Retrieve user info (cached with Redis)  |

---

## 🧪 How to Use

### ✅ Insert User into Database (via User Service)

```bash
curl -X POST -H "Content-type: application/json" \
http://127.0.0.1:5000/register \
-d '{"name": "ritik", "email": "ritikkumar3g@gmail.com"}'
```

### 🔍 Fetch User Data (via Data Service)
```bash
curl http://127.0.0.1:5001/user/ritik

```
## ⚙️ Environment Details

- **Python:** 3.9+
- **Framework:** Flask
- **Database:** PostgreSQL 13
- **Cache:** Redis (Alpine)
- **Containerization:** Docker & Docker Compose

---

## 📈 Future Enhancements

- Add **JWT-based authentication**
- Integrate **CI/CD** using GitHub Actions or Jenkins
- Add **monitoring** with Prometheus + Grafana
- Prepare for **cloud deployment** (AWS/GCP)

---

## 🙏 Credits

Special thanks to my mentor:

**Vimal Daga Sir**  
For his guidance and constant support during this project journey.

---

## 📎 License

This project is open-source and available under the **MIT License**.

---

## 📬 Connect with Me

**Ritik Kumar Sahu**

- 📧 **Email:** ritikkumar3g@gmail.com  
- 💼 **LinkedIn:** [https://linkedin.com/in/ritikumarsahu/]  
- 🌐 **Portfolio:** [https://ritik-personal-portfolio.netlify.app/]
