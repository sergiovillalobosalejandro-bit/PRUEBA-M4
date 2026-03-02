# 🏥 Database API Simulation

REST API built with Node.js, Express, and PostgreSQL following a layered architecture (Controller → Service → Repository).

------------------------------------------------------------------------

## 🚀 Technologies used

- Node.js
- Express
- PostgreSQL
- pg (node-postgres)
-Nodemon
- ES Modules

------------------------------------------------------------------------

## 📁 Project structure

    src/
    │
    ├── config/
    │ ├── env.js
    │ ├── postgres.js
    │ └── mongo.js
    │
    ├── modules/
    │ └── patients/
    │ ├── patient.routes.js
    │ ├── patient.controller.js
    │ ├── patient.service.js

│ └── patient.repository.js

│
├── app.js

└── server.js

------------------------------------------------------------------------

## 🧠 Architecture

Route → Controller → Service → Repository → Database

------------------------------------------------------------------------

## ⚙️ Installation

### 1️⃣ Clone the repository

git clone <REPO_URL>

cd Simulacro-database

### 2️⃣ Install dependencies

npm install

### 3️⃣ Configure environment variables

Create the `.env` file:

PORT=8000

DATABASE_URL=postgresql://username:password@localhost:5432/your_database

### 4️⃣ Create a table in PostgreSQL

CREATE TABLE patients (
id SERIAL PRIMARY KEY,
name VARCHAR(100) NOT NULL,
age INTEGER NOT NULL

);

### 5️⃣ Run the server

npm run dev

Server at:

http://localhost:8000

------------------------------------------------------------------------

## 📌 Endpoints

### GET /patients

Retrieves all patients.

### POST /patients

Body JSON:

{
"name": "Sergio",
"age": 23

}

------------------------------------------------------------------------

## 🧪 Try with curl

curl -X POST http://localhost:8000/patients -H "Content-Type: application/json" -d '{"name":"Sergio","age":23}'

------------------------------------------------------------------------

## 👨‍💻 Author

Project developed as a backend architecture exercise with Node.js and PostgreSQL.
