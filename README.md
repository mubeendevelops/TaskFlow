# TaskFlow - Task Management System

A modern task management web application with JWT authentication, built with Node.js, Express, and Turso database.

## Project Structure

```
Task Management/
├── backend/              # Backend server files
│   ├── server.js        # Express server and API routes
│   ├── package.json     # Backend dependencies
│   ├── .env             # Environment variables (DATABASE_URL, DATABASE_AUTH_TOKEN, JWT_SECRET)
│   └── db/
│       └── schema.sql   # Database schema
│
├── frontend/            # Frontend files
│   ├── index.html       # Landing page
│   ├── login.html       # Login page
│   ├── register.html    # Registration page
│   ├── dashboard.html   # Main task management dashboard
│   ├── app.js           # Frontend JavaScript
│   └── style.css        # Stylesheet
│
└── package.json         # Root package.json with convenience scripts
```

## Setup Instructions

1. **Install Dependencies**

   ```bash
   npm run install-deps
   ```

   Or manually:

   ```bash
   cd backend
   npm install
   ```

2. **Configure Environment Variables**

   Edit `backend/.env` and fill in your values:

   ```
   DATABASE_URL=your_turso_database_url
   DATABASE_AUTH_TOKEN=your_turso_auth_token
   JWT_SECRET=your_jwt_secret_key
   ```

3. **Set Up Database**

   Execute the SQL schema in `backend/db/schema.sql` on your Turso database.

4. **Start the Server**

   ```bash
   npm start
   ```

   Or manually:

   ```bash
   cd backend
   node server.js
   ```

   The server will run on `http://localhost:3000` (or the port specified in your environment).

## Features

- User authentication with JWT
- Task CRUD operations
- Priority-based task sorting (High → Medium → Low)
- Due date tracking with visual indicators
- Task filtering (All, Active, Completed)
- Multiple sorting options (Priority, Date, Created)
- Delete all tasks functionality
- Modern, responsive UI

## Technology Stack

- **Backend**: Node.js, Express.js
- **Database**: Turso (libSQL)
- **Authentication**: JWT (jsonwebtoken)
- **Frontend**: Vanilla HTML, CSS, JavaScript
- **Password Hashing**: bcryptjs
