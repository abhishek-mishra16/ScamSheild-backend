# 🛡️ ScamShield Backend

Backend API for the **ScamShield** hackathon project.

ScamShield provides secure user authentication and account management using **Node.js, Express.js, PostgreSQL, Prisma, and JWT**.

## 🚀 Tech Stack

* **Node.js**
* **Express.js**
* **PostgreSQL**
* **Prisma ORM**
* **JWT**
* **bcrypt**

## ✨ Features

* User Signup
* User Login
* JWT Authentication
* Protected User Profile
* User Logout
* Input Validation
* PostgreSQL Database Integration
* Secure Password Hashing

## 📡 API Endpoints

### Authentication

| Method | Endpoint           | Description               | Auth |
| ------ | ------------------ | ------------------------- | ---- |
| `POST` | `/api/auth/signup` | Create a new user account | No   |
| `POST` | `/api/auth/login`  | Login and receive JWT     | No   |
| `GET`  | `/api/auth/me`     | Get authenticated user    | Yes  |
| `POST` | `/api/auth/logout` | Logout authenticated user | Yes  |

### Health Check

```http
GET /api/health
```

Expected response:

```json
{
  "success": true,
  "message": "ScamShield backend is running"
}
```

## 📁 Project Structure

```text
server/
├── prisma/
│   ├── migrations/
│   └── schema.prisma
│
├── src/
│   ├── config/
│   │   └── prisma.js
│   ├── controllers/
│   │   └── auth.controller.js
│   ├── middleware/
│   │   ├── auth.middleware.js
│   │   └── error.middleware.js
│   ├── routes/
│   │   └── auth.routes.js
│   ├── services/
│   │   └── auth.service.js
│   ├── utils/
│   │   ├── jwt.js
│   │   └── password.js
│   ├── validators/
│   │   └── auth.validator.js
│   ├── app.js
│   └── server.js
│
├── .env.example
├── .gitignore
├── package.json
├── package-lock.json
└── prisma.config.ts
```

## ⚙️ Setup

### 1. Clone the repository

```bash
git clone https://github.com/abhishek-mishra16/ScamSheild-backend.git
cd ScamSheild-backend
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

Create a `.env` file in the project root:

```env
DATABASE_URL="postgresql://USERNAME:PASSWORD@localhost:5432/scamshield"
JWT_SECRET="your_jwt_secret_here"
JWT_EXPIRES_IN="7d"
PORT=5000
FRONTEND_URL="http://localhost:3000"
```

### 4. Run database migrations

```bash
npx prisma migrate dev
```

### 5. Generate Prisma Client

```bash
npx prisma generate
```

### 6. Start the development server

```bash
npm run dev
```

The backend will run at:

```text
http://localhost:5000
```

## 🔐 Authentication

Protected endpoints require a valid JWT token.

Include the token in the request header:

```http
Authorization: Bearer <token>
```

## 🔒 Security

* Passwords are securely hashed using **bcrypt**.
* Authentication is handled using **JWT**.
* Environment secrets are stored in `.env`.
* `.env` is excluded from Git using `.gitignore`.
* `.env.example` contains only placeholder values.

## 🛠️ Development

Start the development server with:

```bash
npm run dev
```
Build For Hackathon Project
---


