# Namuy Learning — Full-Stack Learning Platform

An earlier full-stack implementation of **Namuy Learning**, developed as a custom web application using **React, Flask, and PostgreSQL**.

The project explores the architecture of an online learning platform with user authentication, student profiles, course-related interfaces, multilingual support, account management, two-factor authentication, and other learning-platform functionality.

> **Project status:** Legacy / paused development
>
> This repository represents an earlier custom-built version of Namuy Learning.  
> The current production platform has since evolved to a WordPress-based architecture.

🌐 **Current Namuy Learning website:**  
https://namuylearning.com/

---

## Overview

This project was created to explore how Namuy Learning could operate as a custom full-stack web application rather than relying on a CMS.

The application separates the platform into multiple layers:

- A React single-page application
- A Python/Flask REST API
- PostgreSQL persistence
- JWT-based authentication
- Email-based two-factor authentication
- User profile and account management
- Multilingual user interfaces
- An experimental Node.js / Socket.IO real-time server

The repository reflects a practical attempt to build the different layers of an educational platform and connect frontend, backend, authentication, database, and user-management functionality.

---

## Tech Stack

### Frontend

- **React 18**
- **JavaScript**
- **React Router**
- **Axios**
- **React Bootstrap**
- **Bootstrap 5**
- **CSS Modules**
- **i18next**
- **react-i18next**
- **Framer Motion**
- **Swiper**
- **Font Awesome**
- **React Icons**

### Backend

- **Python**
- **Flask**
- **Flask-CORS**
- **Flask-SQLAlchemy**
- **Flask-Migrate**
- **Flask-Mail**
- **PyJWT**
- **bcrypt**

### Database

- **PostgreSQL**
- **SQLAlchemy**
- **pg8000**
- **psycopg2**

### Real-Time / Experimental Services

- **Node.js**
- **Express**
- **Socket.IO**
- **JSON Web Tokens**

### Development

- **Git**
- **GitHub**
- **npm / Yarn**
- **Create React App**

---

## Architecture

```text
                         Namuy Learning
                               │
              ┌────────────────┴────────────────┐
              │                                 │
              ▼                                 ▼
      React Frontend                      Flask Backend
      localhost:3000                     localhost:3001
              │                                 │
              │ Axios / REST API                │
              └──────────────►──────────────────┤
                                                │
                                   ┌────────────┴────────────┐
                                   │                         │
                                   ▼                         ▼
                              PostgreSQL                Email Services
                                                          / 2FA

              React Frontend
                     │
                     │ Socket.IO
                     ▼
            Experimental Node.js
             Real-Time Server
              localhost:4000
