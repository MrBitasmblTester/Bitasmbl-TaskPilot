# Bitasmbl-TaskPilot

Description
TaskPilot is a web-based task management application enabling users to register, authenticate via JWT, and manage tasks organized by projects with priority-based sorting. The front-end is built with React, while the back-end uses Node.js, Express, and MongoDB.

## Tech Stack
- Express.js
- MongoDB
- React
- Node.js

## Requirements
- Implement JWT-based authentication
- Design Mongoose schemas for User and Task
- Create RESTful API endpoints for CRUD operations
- Implement priority sorting on front-end
- Optional: Filter tasks by project category

## Installation
1. Clone the repository:
   bash
   git clone https://github.com/your-username/Bitasmbl-TaskPilot.git
   cd Bitasmbl-TaskPilot
   
2. Install server dependencies:
   bash
   cd server
   npm install
   
3. Install client dependencies:
   bash
   cd ../client
   npm install
   
4. Create a `.env` file in the `server` directory with the following variables:
   env
   MONGODB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   PORT=5000
   

## Usage
- Start the development servers:
  bash
  # In server folder
  npm run dev
  # In client folder
  npm start
  
- Server runs on `http://localhost:5000`, client runs on `http://localhost:3000`.
- Register a new user, authenticate, and start managing tasks by project.

## Implementation Steps
1. Initialize the Node.js project in `server/` and install Express, Mongoose, JSONWebToken, and other dependencies.
2. Set up the Express server (`server.js`), connect to MongoDB, and configure middleware (CORS, JSON parsing).
3. Create Mongoose schemas and models for `User` (with email, password hash) and `Task` (title, description, priority, project category, user reference).
4. Implement authentication routes for registration and login, issuing JWTs upon successful login.
5. Build protected CRUD API endpoints for tasks (`/api/tasks`) with middleware to verify JWTs.
6. Initialize the React app in `client/`, install Axios and React Router.
7. Create authentication context/hooks to handle login and token storage.
8. Develop components for listing, creating, editing, and deleting tasks, fetching data from the API.
9. Implement priority-based sorting and optional project filtering in the task list view.
10. Style the application and test end-to-end for both functionality and error handling.

## API Endpoints
- POST `/api/auth/register` — Register a new user
- POST `/api/auth/login` — Authenticate and receive a JWT
- GET `/api/tasks` — Get all tasks for the authenticated user
- POST `/api/tasks` — Create a new task
- GET `/api/tasks/:id` — Retrieve a specific task
- PUT `/api/tasks/:id` — Update a task
- DELETE `/api/tasks/:id` — Delete a task