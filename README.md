# Mindify - Mental Health Tracking Application

A comprehensive mental health and mood tracking application that helps users monitor their emotional well-being, track daily moods, and maintain gratitude journals.

## 🌟 Features

- **User Authentication**: Secure registration and login system with JWT tokens
- **Mood Tracking**: Log daily moods with emojis and personalized labels
- **Health Status Monitoring**: Track physical and mental health indicators
- **Gratitude Journal**: Daily gratitude entries to promote positive thinking
- **MCQ Assessments**: Mental health questionnaires for self-evaluation
- **Mood History**: Visual representation of mood patterns over time
- **User Profiles**: Customizable profiles with emoji and descriptions
- **Responsive Design**: Works seamlessly on desktop and mobile devices

## 🛠️ Tech Stack

### Frontend
- **Next.js 15.3.2** with TypeScript
- **React** for UI components
- **Tailwind CSS** for styling
- **Axios** for API communication
- **Context API** for state management

### Backend
- **Node.js** with Express.js
- **MySQL** database
- **Sequelize ORM** for database management
- **JWT** for authentication
- **bcryptjs** for password hashing
- **CORS** enabled for cross-origin requests

## 📋 Prerequisites

Before running this application, ensure you have:

- Node.js (v18 or higher)
- MySQL Server (v8.0 or higher)
- npm or yarn package manager
- Git

## 🚀 Installation

### 1. Clone the repository

```bash
git clone https://github.com/Meghana-sh/Mindify.git
cd Mindify
```

### 2. Backend Setup

```bash
cd backend

# Install dependencies
npm install

# Configure environment variables
# Update .env file with your MySQL credentials:
# DB_HOST="localhost"
# DB_PORT=3306
# DB_USER="root"
# DB_PASSWORD="your_mysql_password"
# DB_NAME="mindcareapp"
# JWT_SECRET="your-secret-key"

# Start the backend server
npm run dev
```

The backend server will run on `http://localhost:5000`

### 3. Frontend Setup

```bash
cd medapp

# Install dependencies
npm install

# Start the development server
npm run dev
```

The frontend application will run on `http://localhost:3000`

##  API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user
- `GET /api/auth/profile/:id` - Get user profile

### Mood Tracking
- `POST /api/mood` - Add mood entry
- `GET /api/mood/user/:userId` - Get user mood history
- `GET /api/mood/stats` - Get mood statistics

## 🎯 Usage

1. **Sign Up**: Create a new account with your email and password
2. **Login**: Access your dashboard using your credentials
3. **Track Mood**: Log your daily mood with emojis and descriptions
4. **Add Gratitude**: Write daily gratitude entries
5. **View History**: Check your mood patterns and trends over time
6. **Update Profile**: Customize your profile with emoji and description

## 🔒 Security Features

- Password hashing with bcryptjs
- JWT-based authentication
- Protected routes and middleware
- Secure API endpoints
- CORS configuration for trusted origins

## 🗄️ Database Schema

### Users Table
- id (UUID, Primary Key)
- name
- email (Unique)
- password_hash
- emoji
- description
- createdAt
- updatedAt

### Moods Table
- id (UUID, Primary Key)
- user_id (Foreign Key)
- label
- emoji
- healthStatus
- gratitudeText
- mcqAnswers (JSON)
- entry_date
- createdAt
- updatedAt

---

Made with ❤️ for better mental health awareness