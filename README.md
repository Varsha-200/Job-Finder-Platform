# 💼 Job Finder Platform

A full-stack web application designed to connect service seekers with service providers through job posting, searching, filtering, and booking functionality.

This project was developed as part of the **Intel Unnati Industrial Training Program**.

---

## 📌 Overview

The Job Finder Platform provides a centralized system where users can register, log in, post job opportunities, browse available jobs, filter listings, and book jobs.

The application combines a **Flask-based backend**, **SQLAlchemy ORM**, an **SQLite database**, and a responsive frontend built with **HTML, CSS, JavaScript, Bootstrap, and Jinja2 templates**.

The project focuses on practical full-stack development concepts such as authentication, session management, relational database design, CRUD-style operations, search and filtering, and backend–frontend integration.

---

## ✨ Features

### 👤 User Management
- User registration
- Secure login and logout
- Password hashing using Werkzeug
- Session-based authentication
- User profile information including degree and skills

### 💼 Job Management
- Post new job opportunities
- Store job title, description, location, and salary
- Display available jobs
- Associate posted jobs with registered users

### 🔎 Search, Filtering & Sorting
Users can search and filter jobs using:

- Job title
- Minimum salary
- Maximum salary
- Location

Jobs can also be sorted by:

- Job title
- Salary
- Location

### 🤝 Job Booking
- Registered users can book available jobs
- Booking information is stored in the database
- Jobs that have already been booked are excluded from the available-job query

### 📧 Email Integration
- Flask-Mail configuration for email-related functionality

### 📱 Responsive Interface
- Bootstrap-based responsive design
- Jinja2 template inheritance
- Flash messages for user feedback

---

## 🛠️ Tech Stack

### Backend
- Python
- Flask
- Flask-SQLAlchemy
- Flask-Mail
- Werkzeug

### Frontend
- HTML5
- CSS
- JavaScript
- Bootstrap
- Jinja2

### Database
- SQLite
- SQLAlchemy ORM

### Core Concepts
- Full-Stack Web Development
- User Authentication
- Password Hashing
- Session Management
- Relational Database Design
- CRUD Operations
- Search and Filtering
- Backend–Frontend Integration

---

## 🏗️ Application Architecture

```text
                ┌──────────────────────┐
                │        User          │
                └──────────┬───────────┘
                           │
                           ▼
                ┌──────────────────────┐
                │  HTML / Bootstrap    │
                │  Jinja2 Templates    │
                └──────────┬───────────┘
                           │
                           ▼
                ┌──────────────────────┐
                │    Flask Backend     │
                │                      │
                │ • Authentication     │
                │ • Job Management     │
                │ • Search & Filter    │
                │ • Booking Logic      │
                └──────────┬───────────┘
                           │
                           ▼
                ┌──────────────────────┐
                │   SQLAlchemy ORM     │
                └──────────┬───────────┘
                           │
                           ▼
                ┌──────────────────────┐
                │       SQLite         │
                │                      │
                │  Users │ Jobs        │
                └──────────────────────┘
```

---

## 🔄 Application Workflow

```text
Register
   ↓
Login
   ↓
Dashboard
   ↓
Browse Available Jobs
   ↓
Search / Filter / Sort
   ↓
View Job
   ↓
Book Job
```

Users can also create new listings:

```text
Login → Post Job → Store in Database → Display to Other Users
```

---

## 🗄️ Database Design

The application primarily uses two SQLAlchemy models.

### User

Stores:

- User ID
- Username
- Email
- Password
- Degree
- Skills
- Posted jobs
- Booked jobs

### Job

Stores:

- Job ID
- Title
- Description
- Location
- Salary
- Poster ID
- Booker ID

The relationships between these models allow the application to identify both the user who posted a job and the user who booked it.

---

## 🔐 Authentication & Security

User passwords are hashed using Werkzeug rather than stored directly as plain text.

The application uses:

```python
generate_password_hash()
check_password_hash()
```

Flask sessions are used to maintain authenticated users and restrict access to protected routes such as the dashboard, job posting, and job booking.

---

## 📸 Application Screenshots

### 🔐 Login Page

Users can securely sign in using their registered credentials.

![Login Page](login-page.png)

### 💼 Job Dashboard

The dashboard displays available jobs and allows users to interact with listings.

![Job Dashboard](job-dashboard.png)

### 🔎 Job Search & Filtering

Users can filter available jobs based on criteria such as job title, salary, and location.

![Job Filtering](job-filtering.png)

### 🤝 Job Booking

Users can select and book available jobs through the platform.

![Job Booking](job-booking.png)

---

## 📂 Project Structure

```text
Job-Finder-Platform/
│
├── app.py
├── requirements.txt
├── README.md
├── Intel-Unnati-Project-Report.pdf
│
├── templates/
│   ├── base.html
│   ├── index.html
│   ├── login.html
│   ├── register.html
│   ├── dashboard.html
│   ├── post_job.html
│   └── book_job.html
│
└── screenshots/
    ├── login-page.png
    ├── job-dashboard.png
    ├── job-filtering.png
    └── job-booking.png
```

---

## 🚀 Running the Project Locally

### 1. Clone the repository

```bash
git clone https://github.com/Varsha-200/Job-Finder-Platform.git
cd Job-Finder-Platform
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

### 3. Activate the virtual environment

#### Windows

```bash
venv\Scripts\activate
```

#### macOS / Linux

```bash
source venv/bin/activate
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

### 5. Run the application

```bash
python app.py
```

Open the local Flask address shown in the terminal.

---

## 📖 Project Report

The complete project report contains additional details about the methodology, implementation, results, and development process.

[View Project Report](Intel-Unnati-Project-Report.pdf)

---

## 🎓 Intel Unnati Program

This project was developed as part of the **Intel Unnati Industrial Training Program**.

The goal was to build an integrated platform that simplifies access to job and service opportunities by connecting service seekers and service providers through a web application.

---

## 👥 Team

- **Varsha S Panicker**
- Sreya Elizabeth Shibu
- Jijo Sebastian
- Geethanjali P.

**Project Mentor:** Dr. Anju Pratap  
**Institution:** Saintgits College of Engineering and Technology

---

## 💡 Key Learnings

Through this project, I gained practical experience in:

- Building full-stack web applications with Flask
- Designing relational models using SQLAlchemy
- Connecting frontend templates with backend logic
- Implementing registration and authentication
- Secure password handling
- Session management
- Job posting and booking workflows
- Search, filtering, and sorting functionality
- Working with relational data
- Creating responsive interfaces with Bootstrap
- Collaborating in a team-based software project

---

## 🔮 Future Improvements

Potential enhancements include:

- Separate service-provider and service-seeker roles
- Advanced skill-based matching
- Improved email notification functionality
- User profile editing
- Booking and job history
- Employer and worker ratings
- REST API endpoints
- Stronger form validation
- Automated testing
- Improved UI/UX
- Cloud deployment
- Recommendation-based job matching

---

## 📄 Disclaimer

This project was developed for educational and training purposes as part of the Intel Unnati program.
