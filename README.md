# StudyNotion - EdTech Platform

[Live Demo](https://studynotionfe-a5mm69uz1-omptl164703s-projects-89586688.vercel.app/contact)

![Main Page](https://i.ibb.co/TpsCbLS/Screenshot-2025-07-16-024945.png)

StudyNotion is a full-featured EdTech platform that enables users to create, consume, and rate educational content. Built with the MERN stack (MongoDB, Express.js, React.js, Node.js), it supports both students and instructors with a modern, scalable, and interactive learning experience.

---

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [System Architecture](#system-architecture)
  - [Frontend](#frontend)
  - [Backend](#backend)
  - [Database](#database)
  - [Architecture Diagram](#architecture-diagram)
- [API Design](#api-design)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Environment Variables](#environment-variables)
- [Tech Stack](#tech-stack)
- [Contributing](#contributing)
- [License](#license)

---

## Introduction

StudyNotion aims to provide a seamless and interactive learning experience for students, making education more accessible and engaging. It also empowers instructors to showcase their expertise and connect with learners globally.

---

## Features

### For Students

- Browse and search for courses
- Add courses to wishlist and cart
- Purchase and enroll in courses (Razorpay integration)
- View course content (videos, documents)
- Track progress and rate courses
- Edit profile and manage account

### For Instructors

- Instructor dashboard with insights and analytics
- Create, update, and manage courses and content
- Manage course pricing and media
- View and respond to student feedback
- Edit profile and manage account

### General

- Secure authentication (JWT, OTP, password reset)
- Responsive UI with React and Tailwind CSS
- Cloud-based media management (Cloudinary)
- Email notifications (Nodemailer)
- RESTful API design

---

## System Architecture

The platform follows a client-server architecture:

### Frontend

- **Framework:** React.js
- **State Management:** Redux Toolkit
- **Styling:** Tailwind CSS
- **Routing:** React Router
- **Pages:** Home, About, Contact, Catalog, Course Details, Dashboard, Auth, etc.

### Backend

- **Framework:** Node.js with Express.js
- **Database:** MongoDB (via Mongoose ODM)
- **Authentication:** JWT, OTP, bcrypt
- **Payments:** Razorpay
- **Media:** Cloudinary
- **Email:** Nodemailer

### Database

- **MongoDB** stores users, courses, categories, progress, reviews, etc.
- Flexible schemas for students, instructors, courses, and more.
---

## API Design

- RESTful API with clear separation of concerns
- Endpoints for authentication, user management, courses, payments, etc.
- JSON for data exchange
- Standard HTTP methods (GET, POST, PUT, DELETE)

---

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/OrcasXCode/study-notion-v2.0mern.git
cd Study-Notion
```

### 2. Install dependencies

#### For the frontend

```bash
npm install
```

#### For the backend

```bash
cd server
npm install
```

---

## Configuration

### 1. Set up MongoDB

- Create a MongoDB database (local or cloud, e.g., MongoDB Atlas).

### 2. Create a `.env` file in `server/` with the following variables:

```env
# MongoDB
MONGODB_URL=your-mongodb-connection-url

# JWT
JWT_SECRET=your-jwt-secret-key

# Cloudinary
CLOUD_NAME=your-cloudinary-cloud-name
API_KEY=your-cloudinary-api-key
API_SECRET=your-cloudinary-api-secret
FOLDER_NAME=your-cloudinary-folder-name

# Razorpay
RAZORPAY_KEY_ID=your-razorpay-key-id
RAZORPAY_KEY_SECRET=your-razorpay-key-secret
RAZORPAY_SECRET=your-razorpay-webhook-secret

# Email (Nodemailer)
MAIL_HOST=your-mail-host
MAIL_USER=your-mail-username
MAIL_PASS=your-mail-password

# (Optional) Server Port
PORT=4000
```

> **Note:** Never commit your `.env` file or secrets to version control.

---

## Usage

### 1. Start the backend server

```bash
cd server
npm run start
```

### 2. Start the frontend development server

```bash
cd ..
npm run start
```

- The frontend will run at [http://localhost:3000](http://localhost:3000)
- The backend will run at [http://localhost:4000](http://localhost:4000)

---

## Environment Variables

| Variable             | Description                        | Required | Example                |
|----------------------|------------------------------------|----------|------------------------|
| MONGODB_URL          | MongoDB connection string          | Yes      | mongodb+srv://...      |
| JWT_SECRET           | JWT secret for authentication      | Yes      | mysecretkey            |
| CLOUD_NAME           | Cloudinary cloud name              | Yes      | mycloud                |
| API_KEY              | Cloudinary API key                 | Yes      | 1234567890             |
| API_SECRET           | Cloudinary API secret              | Yes      | abcdefghijklmnop       |
| FOLDER_NAME          | Cloudinary folder for uploads      | Yes      | studynotion            |
| RAZORPAY_KEY_ID      | Razorpay key ID                    | Yes      | rzp_test_...           |
| RAZORPAY_KEY_SECRET  | Razorpay key secret                | Yes      | 1234567890abcdef       |
| RAZORPAY_SECRET      | Razorpay webhook secret            | Yes      | 1234567890abcdef       |
| MAIL_HOST            | SMTP host for Nodemailer           | Yes      | smtp.gmail.com         |
| MAIL_USER            | SMTP username                      | Yes      | user@gmail.com         |
| MAIL_PASS            | SMTP password                      | Yes      | yourpassword           |
| PORT                 | Backend server port                | No       | 4000                   |

---

## Tech Stack

- **Frontend:** React.js, Redux Toolkit, Tailwind CSS, React Router, Axios, Chart.js, Swiper, etc.
- **Backend:** Node.js, Express.js, MongoDB, Mongoose, JWT, bcrypt, Razorpay, Cloudinary, Nodemailer, dotenv, etc.

---

## Contributing

Contributions are welcome! Please open issues and submit pull requests for improvements or bug fixes.
