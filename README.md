# MERN Authentication API

- This is a simple MERN (MongoDB, Express, React, Node.js) project for user authentication, including registration, login, and a protected route with JWT-based authentication.

```bash
backend/
├── config/
│   └── db.js                 # MongoDB connection
├── middleware/
│   ├── authMiddleware.js     # JWT middleware for protected routes
│   └── errorMiddleware.js    # Error handling middleware
├── models/
│   └── User.js               # User schema
├── routes/
│   └── authRoutes.js         # Authentication API routes
├── .env                      # Environment variables
├── package.json              # Backend dependencies and scripts
└── server.js                 # Backend entry point

frontend/
├── public/                   # Static assets
├── src/                      # React components and application logic
│   ├── components/           # Reusable components
│   ├── pages/                # Application pages
│   ├── App.js                # Main React App
│   └── index.js              # React entry point
├── package.json              # Frontend dependencies and scripts
                     
```

# Features
- Register: Create a new user with name, email, and password.
- Login: Authenticate user and return a JWT.
- Protected Route: Access user profile information with a valid JWT.

# Setup Instructions
- Step 1: Initialize Backend
- Create a new directory for the backend and navigate into it

>- mkdir backend
>- cd backend

# Initialize a Node.js project:

>- npm init -y

# Install required backend dependencies:

>- npm install express mongoose dotenv bcryptjs jsonwebtoken body-parser cors


# Create the following folders and files:

```bash
backend/
├── config/
├── middleware/
├── models/
├── routes/
├── .env
├── server.js

```

# Initialize Frontend

- create a new directory for the frontend and navigate into it:

>- mkdir frontend
>- cd frontend

# Initialize a new React project

>- npx create-react-app frontend

# Install additional dependencies for the frontend:

>- npm install axios react-router-dom

# Create the following folders and files:

```bash
frontend/
├── public/
├── src/
│   ├── components/
│   ├── pages/
│   ├── App.js
│   └── index.js
├── .env
├── package.json

```

# Environment Variables

- Backend
- Create a .env file in the backend directory and add the following:

```bash
PORT=5000
MONGO_URI=<Your_MongoDB_Connection_String>
JWT_SECRET=<Your_JWT_Secret>
```

# Run the Application

- Backend
- Navigate to the backend folder:

>- cd backend

# Start the backend server:

>- node server.js


# Frontend
- Navigate to the frontend folder:

>-cd frontend

# Start the React development server:

>-npm start

# API Endpoints

## Authentication Endpoints

| Method | Endpoint                | Description                        | Protected |
|--------|-------------------------|------------------------------------|-----------|
| POST   | `/api/auth/register`     | Register a new user               | No        |
| POST   | `/api/auth/login`        | Login and get JWT token           | No        |
| GET    | `/api/auth/profile`      | Get user profile                  | Yes       |




