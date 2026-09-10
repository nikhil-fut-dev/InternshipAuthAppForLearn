# 👨‍💻 NIKHIL

### Full-Stack Web Developer & Project Creator

> **Internship Auth** — A production-oriented, secure authentication system built with modern full-stack technologies.

<p align="center">

**🔐 Secure Authentication • 🛡️ Production Security • ⚡ REST API • 🎯 Role-Based Access**

</p>

---

## 🚀 Internship Auth

A professional full-stack authentication system designed with **real-world security practices**, scalable architecture, and clean API development.

Built by **NIKHIL** with a focus on understanding not only *how* authentication works, but also **why each security layer is necessary**.

---

### 👨‍💻 Created & Developed By

**NIKHIL**  
*Full-Stack Web Developer*

**Role:** Project Architect & Developer  
**Focus:** React • Node.js • Express • MongoDB • Authentication • Web Security

---

# 🔐 Internship Auth App Pro

> **A production-oriented full-stack authentication system built with React, Node.js, Express, MongoDB and JWT — focused on secure authentication, authorization, API protection and modern web security practices.**

![React](https://img.shields.io/badge/Frontend-React%20%2B%20Vite-61DAFB?logo=react&logoColor=black)
![Node](https://img.shields.io/badge/Backend-Node.js-339933?logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/API-Express-000000?logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/Database-MongoDB-47A248?logo=mongodb&logoColor=white)
![JWT](https://img.shields.io/badge/Auth-JWT-000000?logo=jsonwebtokens&logoColor=white)
![Security](https://img.shields.io/badge/Security-Production--Oriented-red)
![Deployment](https://img.shields.io/badge/Deployment-Vercel%20%2B%20Render-black)

---

## 📌 Table of Contents

- [Overview](#-overview)
- [Project Goals](#-project-goals)
- [Tech Stack](#-tech-stack)
- [Architecture](#-architecture)
- [Project Structure](#-project-structure)
- [Authentication Flow](#-authentication-flow)
- [Security Level](#-security-level)
- [Security Features](#-security-features)
- [Registration Flow](#-registration-flow)
- [Login Flow](#-login-flow)
- [JWT Authentication](#-jwt-authentication)
- [HttpOnly Cookie Authentication](#-httponly-cookie-authentication)
- [Protected Routes](#-protected-routes)
- [Role-Based Authorization](#-role-based-authorization)
- [Input Validation](#-input-validation)
- [Password Security](#-password-security)
- [CSRF Protection](#-csrf-protection)
- [Rate Limiting](#-rate-limiting)
- [Security Headers](#-security-headers)
- [CORS](#-cors)
- [Logout](#-logout)
- [Database Security](#-database-security)
- [Frontend Security](#-frontend-security)
- [Environment Variables](#-environment-variables)
- [API Endpoints](#-api-endpoints)
- [HTTP Status Codes](#-http-status-codes)
- [Local Development](#-local-development)
- [Production Deployment](#-production-deployment)
- [Testing Checklist](#-testing-checklist)
- [Security Architecture](#-security-architecture)
- [Current Security Assessment](#-current-security-assessment)
- [Future Improvements](#-future-improvements)
- [Learning Outcomes](#-learning-outcomes)
- [Author](#-author)

---

# 🚀 Overview

**Internship Auth App Pro** is a full-stack authentication and authorization application designed to demonstrate how a modern web application's authentication system can be built with security as a core requirement.

The project implements:

- User registration
- User login
- User logout
- JWT authentication
- HttpOnly cookie-based authentication
- Protected API routes
- Role-based authorization
- Admin access control
- Password hashing
- Strong request validation
- CSRF protection
- Login rate limiting
- Registration rate limiting
- Security headers
- CORS protection
- MongoDB persistence
- Production environment configuration
- React frontend
- REST API architecture
- Vercel frontend deployment
- Render backend deployment
- MongoDB Atlas database

The project is designed not only to work, but also to demonstrate **why each security layer exists and how different layers work together.**

---

# 🎯 Project Goals

The main goal of this project is to build authentication using an approach closer to real-world production applications instead of using a simple:

```text
Login → localStorage → JWT
```

approach.

The application follows a layered security model:

```text
                    ┌─────────────────────┐
                    │      Frontend       │
                    │    React + Vite     │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │        CORS         │
                    │   Origin Control    │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │  Security Headers  │
                    │      Helmet         │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    Rate Limiting    │
                    │ Brute-force Control │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Joi Validation    │
                    │ Input Sanitization  │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Authentication      │
                    │ JWT + HttpOnly      │
                    │ Cookie              │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Authorization       │
                    │ User / Admin        │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │      MongoDB        │
                    │     Mongoose        │
                    └─────────────────────┘
```

---

# 🛠️ Tech Stack

## Frontend

| Technology | Purpose |
|---|---|
| React | UI development |
| Vite | Frontend development/build tool |
| React Router | Client-side routing |
| Axios | API communication |
| React Icons | UI icons |
| React Hot Toast | Notifications |

## Backend

| Technology | Purpose |
|---|---|
| Node.js | JavaScript runtime |
| Express.js | REST API framework |
| MongoDB | Database |
| Mongoose | MongoDB ODM |
| bcryptjs | Password hashing |
| JSON Web Token | Authentication |
| cookie-parser | Cookie handling |
| Joi | Request validation |
| Helmet | Security headers |
| express-rate-limit | Rate limiting |
| csrf-csrf | CSRF protection |
| Nodemailer | Email infrastructure |

## Deployment

| Service | Purpose |
|---|---|
| GitHub | Source code |
| Render | Backend deployment |
| Vercel | Frontend deployment |
| MongoDB Atlas | Cloud database |
| Gmail SMTP | Email service infrastructure |

---

# 📁 Project Structure

```text
internship-auth-app/
│
├── backend/
│   │
│   ├── config/
│   │   └── db.js
│   │
│   ├── controllers/
│   │   └── authController.js
│   │
│   ├── middleware/
│   │   ├── authMiddleware.js
│   │   ├── roleMiddleware.js
│   │   ├── validateMiddleware.js
│   │   ├── csrfMiddleware.js
│   │   └── rateLimitMiddleware.js
│   │
│   ├── models/
│   │   └── User.js
│   │
│   ├── routes/
│   │   ├── authRoutes.js
│   │   └── adminRoutes.js
│   │
│   ├── validations/
│   │   └── authValidation.js
│   │
│   ├── utils/
│   │
│   ├── .env
│   ├── .env.example
│   ├── package.json
│   └── server.js
│
├── frontend/
│   │
│   ├── src/
│   │   ├── api/
│   │   │   └── axios.js
│   │   │
│   │   ├── components/
│   │   │   └── ProtectedRoute.jsx
│   │   │
│   │   ├── pages/
│   │   │   ├── Register.jsx
│   │   │   ├── Login.jsx
│   │   │   └── Dashboard.jsx
│   │   │
│   │   ├── services/
│   │   │   └── authService.js
│   │   │
│   │   ├── App.jsx
│   │   ├── main.jsx
│   │   └── index.css
│   │
│   ├── .env
│   ├── .env.example
│   ├── package.json
│   └── vite.config.js
│
├── .gitignore
└── README.md
```

---

# 🔄 Authentication Flow

The overall authentication process works like this:

```text
                    REGISTER
                       │
                       ▼
                Joi Validation
                       │
                       ▼
              Check Existing User
                       │
                       ▼
              bcrypt Password Hash
                       │
                       ▼
                 MongoDB Save
                       │
                       ▼
              Registration Success


                     LOGIN
                       │
                       ▼
                Joi Validation
                       │
                       ▼
                Find User
                       │
                       ▼
              Check Account Status
                       │
                       ▼
             bcrypt.compare()
                       │
                       ▼
                  Create JWT
                       │
                       ▼
             HttpOnly Cookie
                       │
                       ▼
                Login Success
                       │
                       ▼
                 Protected API
                       │
                       ▼
               JWT Verification
                       │
                       ▼
                  req.user
```

---

# 📝 Registration Flow

When a user registers:

```text
POST /api/v1/auth/register
```

The request passes through:

```text
Rate Limiter
      ↓
Joi Validation
      ↓
Controller
      ↓
Existing User Check
      ↓
Password Hashing
      ↓
MongoDB
      ↓
Success Response
```

### Example request

```json
{
  "fullName": "Nikhil",
  "email": "nikhil@example.com",
  "password": "Strong@123"
}
```

The backend validates:

- Full name
- Email format
- Password strength
- Unknown fields

The password is never stored as plain text.

---

# 🔑 Login Flow

Login endpoint:

```text
POST /api/v1/auth/login
```

Flow:

```text
Client
  ↓
Rate Limiter
  ↓
Joi Validation
  ↓
Find User
  ↓
Check Active Status
  ↓
Compare Password
  ↓
Generate JWT
  ↓
Set HttpOnly Cookie
  ↓
Return User Data
```

The access token is **not stored in localStorage**.

Instead:

```text
JWT
 ↓
HttpOnly Cookie
```

This significantly reduces exposure of the authentication token to client-side JavaScript.

---

# 🔐 JWT Authentication

JWT is used to represent an authenticated user's identity.

The token contains information such as:

```json
{
  "userId": "USER_ID",
  "role": "user"
}
```

The JWT is signed using:

```text
JWT_SECRET
```

The secret is stored in environment variables and should never be committed to GitHub.

---

# 🍪 HttpOnly Cookie Authentication

Instead of:

```text
localStorage
   ↓
accessToken
```

the application uses:

```text
Browser
   ↓
HttpOnly Cookie
   ↓
accessToken
```

The cookie configuration in production uses:

```text
HttpOnly: true
Secure: true
SameSite: None
```

### Why HttpOnly?

JavaScript cannot directly read an HttpOnly cookie.

Therefore, code such as:

```js
document.cookie
```

cannot access the authentication token.

This provides an important layer of protection against token theft through client-side JavaScript.

---

# 🛡️ Protected Routes

Protected backend routes use authentication middleware.

Example:

```text
GET /api/v1/auth/me
```

Flow:

```text
Request
   ↓
Read accessToken cookie
   ↓
Verify JWT
   ↓
Find User
   ↓
Check Account Status
   ↓
req.user
   ↓
Controller
```

If authentication fails:

```text
401 Unauthorized
```

is returned.

---

# 👑 Role-Based Authorization

The application supports:

```text
user
admin
```

roles.

Authentication and authorization are treated as two different concepts.

### Authentication

> "Who are you?"

### Authorization

> "What are you allowed to do?"

Example:

```text
User
 ↓
Authenticated
 ↓
Role = user
 ↓
Admin endpoint
 ↓
403 Forbidden
```

Admin:

```text
Admin
 ↓
Authenticated
 ↓
Role = admin
 ↓
Admin endpoint
 ↓
200 OK
```

The backend performs the actual authorization check.

Frontend role-based UI hiding is **not considered a security boundary**.

---

# 🧹 Input Validation

The application uses **Joi** for request validation.

Validation happens before controller logic.

Example password requirements:

```text
Minimum 8 characters
Maximum 72 characters
At least one uppercase letter
At least one lowercase letter
At least one number
At least one special character
```

Example:

```text
Strong@123
```

is valid.

Unknown fields are stripped using:

```js
stripUnknown: true
```

This prevents users from attempting to inject unexpected fields such as:

```json
{
  "fullName": "John",
  "email": "john@example.com",
  "password": "Strong@123",
  "role": "admin"
}
```

The unwanted `role` field from the registration request is removed before controller processing.

---

# 🔒 Password Security

Passwords are hashed using:

```text
bcryptjs
```

Example concept:

```text
Plain Password
      ↓
bcrypt
      ↓
Password Hash
      ↓
MongoDB
```

MongoDB stores the hash rather than the original password.

During login:

```text
Entered Password
      ↓
bcrypt.compare()
      ↓
Stored Hash
      ↓
Match / No Match
```

The backend never needs to decrypt a password because bcrypt is designed as a one-way password hashing mechanism.

---

# 🛡️ CSRF Protection

The application implements **Double Submit Cookie-style CSRF protection** using `csrf-csrf`.

The system generates a CSRF token and stores it in a cookie:

```text
csrfToken
```

For protected state-changing requests, the frontend sends:

```http
X-CSRF-Token: <token>
```

The backend verifies the token before processing the request.

### Protected methods

The CSRF middleware ignores:

```text
GET
HEAD
OPTIONS
```

and protects state-changing methods such as:

```text
POST
PUT
PATCH
DELETE
```

The authentication cookie is HttpOnly, while the CSRF token cookie is intentionally accessible to frontend JavaScript so Axios can send the token in the request header.

---

# 🚦 Rate Limiting

The application uses `express-rate-limit`.

## Login Rate Limit

```text
Window: 15 minutes
Maximum: 5 requests
```

After excessive login attempts:

```text
Too many login attempts.
Please try again after 15 minutes.
```

This helps reduce:

- Brute-force attacks
- Password guessing
- Automated login abuse

## Registration Rate Limit

```text
Window: 15 minutes
Maximum: 10 requests
```

This helps reduce automated account creation and registration abuse.

---

# 🪖 Security Headers — Helmet

The backend uses:

```text
Helmet
```

Helmet adds commonly recommended HTTP security headers.

In production, HSTS is enabled:

```text
Strict-Transport-Security
```

with HTTPS-oriented configuration.

This helps browsers enforce secure HTTPS communication.

---

# 🌐 CORS Protection

The API does not allow arbitrary origins.

The backend uses an explicit frontend origin:

```env
FRONTEND_URL=https://your-frontend.vercel.app
```

CORS is configured with:

```text
credentials: true
```

This is required because authentication depends on cookies.

The production architecture is therefore:

```text
Vercel Frontend
       │
       │ HTTPS + Credentials
       ▼
Render Backend
       │
       ▼
MongoDB Atlas
```

---

# 🚪 Logout

Logout endpoint:

```text
POST /api/v1/auth/logout
```

The backend clears the authentication cookie.

Flow:

```text
Logout Request
      ↓
CSRF Verification
      ↓
Clear accessToken Cookie
      ↓
Logout Success
```

After logout, the previous authentication cookie is removed.

---

# 🗄️ Database Security

MongoDB is hosted using:

```text
MongoDB Atlas
```

The connection string is stored in:

```text
MONGODB_URI
```

and is never hardcoded into the source code.

The application uses Mongoose models to control the structure of user data.

Example user data:

```text
fullName
email
password
role
isActive
createdAt
updatedAt
```

The password field contains a hash rather than a plaintext password.

---

# 💻 Frontend Security

The frontend follows several security practices:

### No JWT in localStorage

The authentication token is not stored in:

```text
localStorage
```

Instead, authentication is handled using an HttpOnly cookie.

### Axios credentials

Axios uses:

```js
withCredentials: true
```

so cookies can participate in cross-origin requests when the backend CORS policy allows them.

### CSRF Header

Axios automatically reads the CSRF cookie and adds:

```http
X-CSRF-Token
```

to state-changing requests.

### Protected UI Routes

React Router uses a protected route component to prevent unauthenticated users from accessing protected pages through the normal UI.

However, the backend remains the actual security boundary.

---

# 🔑 Environment Variables

Sensitive configuration is stored in `.env`.

Example:

```env
NODE_ENV=production

PORT=10000

MONGODB_URI=

JWT_SECRET=
JWT_EXPIRES_IN=7d

CSRF_SECRET=

EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USER=
EMAIL_PASSWORD=

FRONTEND_URL=https://your-frontend.vercel.app
```

Frontend:

```env
VITE_API_URL=https://your-backend.onrender.com
```

### Important

Never commit:

```text
.env
```

to GitHub.

The repository contains:

```text
.env.example
```

instead.

---

# 🔌 API Endpoints

Base URL:

```text
/api/v1
```

## Authentication

| Method | Endpoint | Authentication | Purpose |
|---|---|---|---|
| GET | `/auth/csrf-token` | No | Generate CSRF token |
| POST | `/auth/register` | No | Register user |
| POST | `/auth/login` | No | Login user |
| POST | `/auth/logout` | CSRF | Logout |
| GET | `/auth/me` | JWT | Get current user |

## Admin

| Method | Endpoint | Required Role | Purpose |
|---|---|---|---|
| GET | `/admin/dashboard` | admin | Admin dashboard |

---

# 📊 HTTP Status Codes

The API follows meaningful HTTP status codes.

| Status | Meaning |
|---|---|
| `200` | Successful request |
| `201` | Resource created |
| `400` | Bad request / validation failure |
| `401` | Authentication required / invalid authentication |
| `403` | Forbidden / insufficient permission / CSRF rejection |
| `404` | Resource not found |
| `429` | Rate limit exceeded |
| `500` | Internal server error |

---

# 🧪 Local Development

## 1. Clone Repository

```bash
git clone https://github.com/YOUR_USERNAME/internship-auth-app.git
cd internship-auth-app
```

---

## 2. Backend Setup

```bash
cd backend
npm install
```

Create:

```text
.env
```

Example:

```env
PORT=5000
NODE_ENV=development

MONGODB_URI=your_mongodb_connection_string

JWT_SECRET=your_jwt_secret
JWT_EXPIRES_IN=7d

CSRF_SECRET=your_csrf_secret

FRONTEND_URL=http://localhost:5173
```

Start backend:

```bash
npm run dev
```

Backend:

```text
http://localhost:5000
```

---

# ⚛️ Frontend Setup

Open another terminal:

```bash
cd frontend
npm install
```

Create:

```text
.env
```

Add:

```env
VITE_API_URL=http://localhost:5000
```

Start frontend:

```bash
npm run dev
```

Frontend:

```text
http://localhost:5173
```

---

# 🚀 Production Deployment

The application is deployed using:

```text
                    GitHub
                   /      \
                  /        \
                 ▼          ▼
             Vercel       Render
           Frontend       Backend
                            │
                            ▼
                       MongoDB Atlas
```

## Frontend

```text
React + Vite
      ↓
GitHub
      ↓
Vercel
```

## Backend

```text
Node.js + Express
      ↓
GitHub
      ↓
Render
```

## Database

```text
MongoDB
   ↓
MongoDB Atlas
```

---

# 🔄 Production Environment Flow

Production frontend:

```text
https://your-frontend.vercel.app
```

Production backend:

```text
https://your-backend.onrender.com
```

Frontend environment:

```env
VITE_API_URL=https://your-backend.onrender.com
```

Backend environment:

```env
FRONTEND_URL=https://your-frontend.vercel.app
```

This ensures that:

- Frontend calls the correct backend
- Backend accepts the correct frontend origin
- Verification/cross-origin URL configuration can use the deployed frontend origin where applicable
- Secure cookies work over HTTPS

---

# 🧪 Testing Checklist

## Registration

- [x] Valid registration
- [x] Duplicate email handling
- [x] Invalid email validation
- [x] Weak password rejection
- [x] Missing field validation
- [x] Unknown field stripping
- [x] Password hashing

## Login

- [x] Valid login
- [x] Invalid email/password
- [x] Inactive account protection
- [x] JWT generation
- [x] HttpOnly authentication cookie
- [x] Login rate limiting

## Authentication

- [x] Protected `/me` route
- [x] JWT verification
- [x] Invalid token rejection
- [x] Expired token rejection
- [x] Non-existing user rejection

## Authorization

- [x] User role
- [x] Admin role
- [x] Admin-only endpoint
- [x] `403 Forbidden` for unauthorized role

## CSRF

- [x] CSRF token generation
- [x] CSRF cookie
- [x] CSRF request header
- [x] CSRF validation on protected state-changing route

## Security

- [x] Helmet
- [x] Rate limiting
- [x] Joi validation
- [x] bcrypt password hashing
- [x] HttpOnly cookie
- [x] Secure production cookie
- [x] SameSite configuration
- [x] CORS origin restriction
- [x] Environment variables
- [x] `.env` excluded from Git

---

# 🛡️ Security Architecture

The project follows a **defense-in-depth** approach.

Instead of relying on a single security mechanism, multiple independent layers protect the application.

```text
┌────────────────────────────────────────────┐
│                 Browser                    │
└─────────────────────┬──────────────────────┘
                      │
                      ▼
              ┌───────────────┐
              │     HTTPS     │
              └───────┬───────┘
                      │
                      ▼
              ┌───────────────┐
              │     CORS      │
              └───────┬───────┘
                      │
                      ▼
              ┌───────────────┐
              │    Helmet     │
              └───────┬───────┘
                      │
                      ▼
              ┌───────────────┐
              │ Rate Limiting │
              └───────┬───────┘
                      │
                      ▼
              ┌───────────────┐
              │     Joi       │
              │  Validation   │
              └───────┬───────┘
                      │
                      ▼
              ┌───────────────┐
              │     CSRF      │
              │  Protection   │
              └───────┬───────┘
                      │
                      ▼
              ┌───────────────┐
              │ JWT + Cookie  │
              │Authentication │
              └───────┬───────┘
                      │
                      ▼
              ┌───────────────┐
              │ Role-Based    │
              │ Authorization │
              └───────┬───────┘
                      │
                      ▼
              ┌───────────────┐
              │   MongoDB     │
              │   + Mongoose  │
              └───────────────┘
```

---

# 📈 Current Security Assessment

## 🟢 Strongly Implemented

The project currently has a **good security foundation for an internship/fresher-level authentication project**.

Implemented layers include:

```text
✅ JWT Authentication
✅ HttpOnly Authentication Cookie
✅ Secure Production Cookie
✅ SameSite Cookie Configuration
✅ bcrypt Password Hashing
✅ Joi Input Validation
✅ Unknown Field Stripping
✅ Login Rate Limiting
✅ Registration Rate Limiting
✅ CSRF Protection
✅ Helmet Security Headers
✅ CORS Origin Restriction
✅ Role-Based Authorization
✅ Protected Backend Routes
✅ Environment-Based Secrets
✅ MongoDB Atlas
```

---

## 🟡 Production Considerations

The project is production-oriented, but security is never "100% complete".

Before handling sensitive real-world production traffic, additional hardening should be considered.

Examples:

- Centralized error handling
- Better structured logging
- Monitoring and alerting
- Refresh-token/session architecture
- Account lockout/risk-based authentication
- Password reset hardening
- Email delivery through a dedicated transactional provider
- SPF/DKIM/DMARC for custom-domain email
- CSRF session-binding strategy review
- More comprehensive automated security tests
- Dependency vulnerability scanning
- Content Security Policy tuning
- Reverse-proxy/trusted-proxy configuration review
- Secrets management through deployment infrastructure

---

# 🔮 Future Improvements

Possible future upgrades:

### Authentication

- Refresh tokens
- Token rotation
- Session management
- Device/session logout
- Password reset
- Change password
- Two-factor authentication
- OAuth / Google login

### Security

- Account lockout
- Suspicious login detection
- IP/device monitoring
- Content Security Policy
- Security audit logging
- Automated dependency scanning
- Automated penetration testing

### User Management

- Profile update
- Avatar upload
- Account deletion
- Admin user management
- User activation/deactivation
- Permission management

### Infrastructure

- Docker
- CI/CD
- Automated tests
- Production logging
- Monitoring
- Error tracking

---

# 🎓 Learning Outcomes

This project demonstrates practical understanding of:

### Frontend

- React component architecture
- React Router
- Protected routes
- Axios
- API integration
- Environment variables
- Authentication state handling

### Backend

- Express.js
- REST API design
- Middleware architecture
- Controllers
- Routes
- MongoDB
- Mongoose
- Authentication
- Authorization

### Security

- JWT
- HttpOnly cookies
- Password hashing
- CSRF protection
- Rate limiting
- CORS
- Helmet
- Input validation
- Role-based access control
- Secure environment variables

### Deployment

- Git/GitHub
- MongoDB Atlas
- Render
- Vercel
- Production environment variables
- HTTPS
- Cross-origin cookie authentication

---

# 💡 Key Security Concepts Demonstrated

This project intentionally demonstrates the difference between:

```text
Authentication ≠ Authorization
```

and:

```text
Password Hashing ≠ Encryption
```

and:

```text
Frontend Protection ≠ Backend Security
```

and:

```text
JWT Storage ≠ JWT Security
```

The backend is treated as the final security boundary.

---

# 🏆 Project Highlights

> 🔐 **Secure Authentication**  
> JWT-based authentication using HttpOnly cookies.

> 🛡️ **Defense in Depth**  
> Multiple independent security layers instead of relying on a single mechanism.

> 🚦 **Brute-Force Protection**  
> Login and registration rate limiting.

> 🧹 **Strong Validation**  
> Joi schema validation with unknown-field stripping.

> 👑 **Role-Based Access**  
> Separate permissions for users and administrators.

> 🍪 **Secure Cookies**  
> HttpOnly + Secure + SameSite configuration for production.

> 🛡️ **CSRF Protection**  
> CSRF token validation for protected state-changing requests.

> 🌐 **Production CORS**  
> Explicit frontend origin with credentials support.

> 🪖 **Security Headers**  
> Helmet-based HTTP security headers.

> ☁️ **Cloud Deployment**  
> Vercel + Render + MongoDB Atlas architecture.

---

# 📌 Important Security Note

No web application can honestly be described as completely secure.

This project should be considered:

```text
                SECURITY LEVEL

        ┌──────────────────────────┐
        │   Basic Authentication    │
        └────────────┬─────────────┘
                     │
                     ▼
        ┌──────────────────────────┐
        │   Intermediate Security  │
        └────────────┬─────────────┘
                     │
                     ▼
        ┌──────────────────────────┐
        │ ⭐ This Project ⭐        │
        │ Production-Oriented      │
        │ Authentication Foundation│
        └────────────┬─────────────┘
                     │
                     ▼
        ┌──────────────────────────┐
        │ Enterprise Security      │
        │ + Monitoring + MFA +     │
        │ Advanced Threat Defense  │
        └──────────────────────────┘
```

The project provides a **strong foundation for an internship/fresher portfolio project**, while clearly leaving room for enterprise-level hardening.

---

# 👨‍💻 Author

**Nikhil**

Full-Stack Web Developer

### Technologies

```text
HTML
CSS
JavaScript
React
Node.js
Express.js
MongoDB
JWT
REST API
Web Security
```

---

# ⭐ Final Note

This project was built with an emphasis on understanding **how authentication works internally**, rather than simply installing an authentication package.

The goal is to understand:

```text
How users register
       ↓
How passwords are protected
       ↓
How users authenticate
       ↓
How JWT works
       ↓
How cookies protect authentication tokens
       ↓
How protected APIs verify users
       ↓
How roles control permissions
       ↓
How CSRF attacks are mitigated
       ↓
How brute-force attacks are limited
       ↓
How HTTP security headers help
       ↓
How frontend and backend communicate securely
       ↓
How the complete application is deployed
```

**Built to learn. Built to understand. Built with security in mind. 🔐**

# 🎤 Interview Questions & Answers

This section contains commonly asked interview questions related to this project.

The answers are written according to the actual architecture and security practices used in this project.

---

## 🟢 Level 1 — Basic Project Questions

### 1. What is this project?

**Answer:**

This is a full-stack authentication and authorization application built using React, Node.js, Express.js and MongoDB.

It provides secure user registration, login, logout, JWT-based authentication, protected routes, role-based authorization, password hashing, CSRF protection, rate limiting, CORS protection and security headers.

---

### 2. Why did you build this project?

**Answer:**

I built this project to understand how authentication works in a real-world full-stack application.

Instead of simply storing a JWT in localStorage, I implemented a more security-oriented architecture using HttpOnly cookies, CSRF protection, rate limiting, input validation and role-based authorization.

---

### 3. What technologies did you use?

**Answer:**

Frontend:

- React
- Vite
- React Router
- Axios
- React Icons
- React Hot Toast

Backend:

- Node.js
- Express.js
- MongoDB
- Mongoose
- JWT
- bcryptjs
- Joi
- Helmet
- express-rate-limit
- csrf-csrf
- Nodemailer

Deployment:

- GitHub
- Vercel
- Render
- MongoDB Atlas

---

### 4. What is the architecture of your project?

**Answer:**

The project follows a frontend-backend-database architecture.

```text
React Frontend
      ↓
Axios
      ↓
Express REST API
      ↓
Middleware
      ↓
Controllers
      ↓
Mongoose
      ↓
MongoDB Atlas
```

Security middleware is placed between the incoming request and application logic.

---

# 🟢 Level 2 — Authentication Questions

### 5. What is authentication?

**Answer:**

Authentication verifies the identity of a user.

For example:

> "Are you really the user associated with this account?"

In this project, authentication is performed using JWT stored in an HttpOnly cookie.

---

### 6. What is authorization?

**Answer:**

Authorization determines what an authenticated user is allowed to do.

For example:

```text
Authentication:
Who are you?

Authorization:
What are you allowed to access?
```

In this project, authorization is implemented using roles such as:

```text
user
admin
```

---

### 7. What is JWT?

**Answer:**

JWT stands for JSON Web Token.

It is a signed token used to securely represent claims about an authenticated user.

In this project, the JWT contains information such as:

```json
{
  "userId": "USER_ID",
  "role": "user"
}
```

The token is signed using a secret stored in an environment variable.

---

### 8. Why did you use JWT?

**Answer:**

JWT allows the server to verify authentication without storing the complete authentication state inside the token itself.

The server can verify the token signature and extract the user's identity and role.

It also works well for REST APIs.

---

### 9. Where do you store the JWT?

**Answer:**

I store the JWT inside an HttpOnly cookie rather than localStorage.

```text
Browser
   ↓
HttpOnly Cookie
   ↓
JWT
```

This prevents normal client-side JavaScript from directly reading the authentication token.

---

### 10. Why didn't you store JWT in localStorage?

**Answer:**

A token stored in localStorage can be accessed by JavaScript.

If an attacker successfully executes malicious JavaScript through an XSS vulnerability, the token could potentially be stolen.

An HttpOnly cookie cannot be directly read using JavaScript.

Therefore, for this project I preferred an HttpOnly cookie-based authentication architecture.

---

### 11. Does HttpOnly completely prevent XSS?

**Answer:**

No.

HttpOnly protects the cookie from being directly read by JavaScript, but it does not eliminate XSS.

An XSS attack could still execute actions as the logged-in user because the browser automatically sends the cookie with applicable requests.

That's why XSS prevention, input handling, CSP and other security controls are still important.

---

# 🟢 Level 3 — Password Security

### 12. How do you store passwords?

**Answer:**

Passwords are hashed using bcrypt.

```text
Plain Password
      ↓
bcrypt
      ↓
Hash
      ↓
MongoDB
```

The original password is never stored.

---

### 13. What is hashing?

**Answer:**

Hashing is a one-way transformation.

A password is converted into a hash, and the original password cannot simply be recovered from the hash.

---

### 14. What is the difference between hashing and encryption?

**Answer:**

Hashing is generally one-way.

Encryption is designed to be reversible using a key.

```text
Hashing:
Password → Hash

Encryption:
Data → Encrypted Data → Decrypted Data
```

Passwords should normally be hashed rather than reversibly encrypted.

---

### 15. How do you verify the password during login?

**Answer:**

I use:

```js
bcrypt.compare(password, user.password)
```

The entered password is compared against the stored bcrypt hash.

---

# 🟡 Level 4 — Middleware & Backend

### 16. What is middleware in Express?

**Answer:**

Middleware is a function that runs during the request-response cycle.

It can:

- Read the request
- Modify the request
- Validate data
- Authenticate users
- Authorize roles
- Reject requests
- Pass control to the next middleware

Example:

```text
Request
  ↓
Rate Limiter
  ↓
Validation
  ↓
Authentication
  ↓
Authorization
  ↓
Controller
```

---

### 17. Why did you separate controllers and middleware?

**Answer:**

For separation of concerns.

Middleware handles cross-cutting concerns such as:

- Authentication
- Authorization
- Validation
- CSRF protection
- Rate limiting

Controllers handle the actual business logic.

This makes the code easier to maintain and scale.

---

### 18. What does your authentication middleware do?

**Answer:**

The authentication middleware:

1. Reads the JWT from the cookie.
2. Checks whether the token exists.
3. Verifies the JWT signature.
4. Finds the user in MongoDB.
5. Checks whether the account is active.
6. Attaches the user to `req.user`.
7. Passes the request to the next middleware/controller.

---

### 19. Why do you query MongoDB after verifying JWT?

**Answer:**

Because JWT verification only proves that the token is valid and signed.

The user's current database state may have changed.

For example:

```text
JWT says:
role = admin

Database says:
user is deactivated
```

The database lookup allows the application to check the user's current status.

---

# 🟡 Level 5 — Role-Based Authorization

### 20. How does admin authorization work?

**Answer:**

The request first passes authentication:

```text
protect
```

Then it passes role authorization:

```text
authorizeRoles("admin")
```

So:

```text
Request
 ↓
JWT Verification
 ↓
User Found
 ↓
Role Check
 ↓
Admin?
 ├── Yes → Continue
 └── No → 403 Forbidden
```

---

### 21. Why isn't frontend role checking enough?

**Answer:**

Because frontend code can be modified or bypassed by the user.

For example, hiding an Admin button does not prevent someone from manually calling:

```text
GET /api/v1/admin/dashboard
```

Therefore, authorization must be enforced on the backend.

---

### 22. What's the difference between 401 and 403?

**Answer:**

`401 Unauthorized` generally means authentication is missing or invalid.

Example:

```text
No valid JWT
```

`403 Forbidden` means the server understood the request, but the authenticated user does not have permission.

Example:

```text
Logged-in normal user
        ↓
Admin endpoint
        ↓
403 Forbidden
```

---

# 🟡 Level 6 — Validation

### 23. Why did you use Joi?

**Answer:**

Joi provides schema-based request validation.

Instead of manually checking every field inside the controller, I define the expected request structure once.

For example:

```text
email → valid email
password → 8–72 characters
fullName → 2–50 characters
```

---

### 24. Why validate on the backend if the frontend already validates?

**Answer:**

Frontend validation is mainly for user experience.

It cannot be trusted for security because users can bypass frontend code completely.

Therefore:

```text
Frontend Validation
        ↓
User Experience

Backend Validation
        ↓
Security Boundary
```

The backend always performs its own validation.

---

### 25. What does `stripUnknown: true` do?

**Answer:**

It removes fields that are not defined in the Joi schema.

For example, if registration only accepts:

```text
fullName
email
password
```

and someone sends:

```json
{
  "fullName": "John",
  "email": "john@example.com",
  "password": "Strong@123",
  "role": "admin"
}
```

the unexpected `role` field is removed.

This helps prevent unwanted field injection.

---

# 🟡 Level 7 — CSRF

### 26. What is CSRF?

**Answer:**

CSRF stands for Cross-Site Request Forgery.

It occurs when an attacker attempts to make a user's browser send an unwanted authenticated request to a website where the user is already logged in.

---

### 27. Why is CSRF relevant to cookie authentication?

**Answer:**

Because browsers automatically send applicable cookies with requests.

If authentication relies on cookies, an attacker may try to exploit that automatic behavior.

CSRF protection adds another verification requirement.

---

### 28. How does your CSRF protection work?

**Answer:**

The application uses a double-submit-cookie style approach.

A CSRF token is generated and made available to the frontend.

For protected state-changing requests, the frontend sends:

```http
X-CSRF-Token: <token>
```

The backend verifies the token before processing the request.

---

### 29. Why is your CSRF cookie not HttpOnly?

**Answer:**

Because the frontend needs to read the CSRF token and send it in the request header.

The authentication cookie is different.

```text
accessToken
→ HttpOnly

csrfToken
→ accessible to frontend
```

The sensitive authentication token remains inaccessible to JavaScript.

---

# 🟡 Level 8 — Rate Limiting

### 30. What is rate limiting?

**Answer:**

Rate limiting restricts how many requests a client can make within a specific time window.

In this project:

```text
Login:
5 requests / 15 minutes

Registration:
10 requests / 15 minutes
```

---

### 31. Why is login rate limiting important?

**Answer:**

It helps reduce brute-force password attacks.

Without rate limiting, an attacker could repeatedly attempt different passwords.

Rate limiting slows down automated guessing attempts.

---

### 32. What happens when the rate limit is exceeded?

**Answer:**

The API returns:

```text
429 Too Many Requests
```

with an appropriate error message.

---

# 🟡 Level 9 — Helmet & CORS

### 33. What is Helmet?

**Answer:**

Helmet is Express middleware that helps configure HTTP security headers.

These headers provide additional browser-level security protections.

In production, this project also enables HSTS configuration.

---

### 34. What is HSTS?

**Answer:**

HSTS stands for HTTP Strict Transport Security.

It tells the browser to use HTTPS for the website for a specified period.

This helps reduce certain downgrade and insecure-connection risks.

---

### 35. What is CORS?

**Answer:**

CORS stands for Cross-Origin Resource Sharing.

It controls which origins are allowed to make browser-based requests to the backend.

In this project, the backend explicitly allows the deployed frontend origin instead of using:

```text
*
```

---

### 36. Why is `credentials: true` required?

**Answer:**

Because the application uses cookies for authentication.

The frontend needs permission to include credentials in cross-origin API requests.

---

# 🟡 Level 10 — Cookies

### 37. What is the difference between HttpOnly, Secure and SameSite?

**Answer:**

### HttpOnly

Prevents JavaScript from directly reading the cookie.

### Secure

Cookie is sent only over HTTPS.

### SameSite

Controls how cookies are sent with cross-site requests.

For the production frontend/backend architecture used here:

```text
Secure = true
SameSite = None
```

---

### 38. Why does production use `SameSite=None`?

**Answer:**

The frontend and backend are deployed on different origins.

For example:

```text
Vercel
   ↓
Frontend

Render
   ↓
Backend
```

Cross-site cookie behavior therefore needs to be configured appropriately, along with HTTPS and CORS credentials.

---

# 🟡 Level 11 — API & HTTP

### 39. Why use REST API?

**Answer:**

REST provides a simple and standardized way for the frontend and backend to communicate using HTTP methods.

For example:

```text
POST   → Create
GET    → Read
PATCH  → Update
DELETE → Delete
```

---

### 40. Why use POST for login?

**Answer:**

Login sends credentials to the server.

POST is appropriate for submitting such data and does not put the credentials into the URL query string.

---

### 41. Why is `/me` useful?

**Answer:**

The `/me` endpoint returns the currently authenticated user based on the authentication cookie.

The frontend can call:

```text
GET /api/v1/auth/me
```

after page reload to determine the current authenticated user's information.

---

# 🟠 Level 12 — Deployment

### 42. Where is your frontend deployed?

**Answer:**

The React + Vite frontend is deployed on Vercel.

---

### 43. Where is your backend deployed?

**Answer:**

The Node.js + Express backend is deployed on Render.

---

### 44. Where is your database?

**Answer:**

MongoDB Atlas.

---

### 45. Why are environment variables important?

**Answer:**

Environment variables keep configuration and sensitive values outside the source code.

Examples include:

```text
MONGODB_URI
JWT_SECRET
CSRF_SECRET
EMAIL_PASSWORD
```

These values should never be committed to GitHub.

---

### 46. What happens if someone gets your JWT secret?

**Answer:**

The attacker could potentially forge valid JWTs.

Therefore, `JWT_SECRET` must be treated as a highly sensitive secret.

If it is accidentally exposed, it should be rotated immediately and affected sessions/tokens should be invalidated according to the application's session strategy.

---

# 🔴 Level 13 — Scenario-Based Security Questions

### 47. What if someone modifies the frontend and changes their role to admin?

**Answer:**

It will not provide real admin access.

The backend checks the authenticated user's role using authorization middleware.

Frontend checks are only for UI behavior.

---

### 48. What if someone sends `role: "admin"` during registration?

**Answer:**

The Joi validation layer uses:

```text
stripUnknown: true
```

so fields not defined in the registration schema are removed.

The backend also controls the default role.

Therefore, the client cannot simply assign itself the admin role through the registration request.

---

### 49. What if the user's account is deactivated after login?

**Answer:**

The authentication middleware queries the user from MongoDB and checks:

```text
isActive
```

If the account is deactivated, the protected request is rejected.

This is one reason the middleware checks the current database state rather than trusting only the JWT payload.

---

### 50. What if an attacker steals the JWT?

**Answer:**

HttpOnly cookies reduce the chance of token theft through direct JavaScript access.

However, if an authentication cookie is genuinely stolen, it can potentially be used until it expires or is otherwise invalidated.

For a more advanced production architecture, I would add short-lived access tokens, refresh-token rotation, session management and token revocation.

---

### 51. Is your application 100% secure?

**Answer:**

No application should honestly claim to be 100% secure.

This project has multiple important security layers:

```text
JWT
HttpOnly Cookies
bcrypt
Joi
CSRF
Rate Limiting
Helmet
CORS
RBAC
Environment Secrets
```

However, enterprise-level security would additionally require areas such as monitoring, logging, MFA, session management, automated security testing, dependency scanning and continuous security review.

---

### 52. What security principle did you follow?

**Answer:**

I followed a **defense-in-depth** approach.

Instead of depending on one security mechanism, multiple independent layers protect the application.

For example:

```text
Validation
   +
Rate Limiting
   +
CSRF
   +
Authentication
   +
Authorization
   +
Secure Cookies
   +
Security Headers
   +
CORS
```

If one layer fails, other layers can still provide protection.

---

# 🔴 Level 14 — Architecture Questions

### 53. Why did you create separate middleware files?

**Answer:**

It improves modularity and separation of concerns.

For example:

```text
authMiddleware.js
→ Authentication

roleMiddleware.js
→ Authorization

validateMiddleware.js
→ Input validation

csrfMiddleware.js
→ CSRF protection

rateLimitMiddleware.js
→ Request limiting
```

This makes each security responsibility easier to understand, test and maintain.

---

### 54. Why separate routes and controllers?

**Answer:**

Routes define:

```text
Which endpoint exists?
Which middleware should run?
Which controller should execute?
```

Controllers contain the actual request/business logic.

This keeps the application organized and scalable.

---

### 55. What happens when `/admin/dashboard` is requested?

**Answer:**

The request passes through:

```text
GET /admin/dashboard
        ↓
protect
        ↓
JWT verification
        ↓
User lookup
        ↓
authorizeRoles("admin")
        ↓
Admin controller
        ↓
Response
```

A normal user receives:

```text
403 Forbidden
```

while an authenticated admin can continue.

---

# 🔥 Level 15 — Difficult Interview Questions

### 56. Why not put the role only in the database and ignore the JWT role?

**Answer:**

It is possible to query the role from the database during authorization.

In this project, the JWT contains the role for efficient identity/authorization context, while the middleware also loads the current user from the database.

For high-security systems, authorization design should consider token lifetime, role changes and revocation strategy carefully.

---

### 57. What happens if a JWT expires?

**Answer:**

`jwt.verify()` throws an error.

The authentication middleware catches the error and returns:

```text
401 Unauthorized
```

The frontend can then redirect the user to the login page.

---

### 58. What happens if the user is deleted but their JWT is still valid?

**Answer:**

The JWT may still be cryptographically valid, but the authentication middleware queries MongoDB.

If the user no longer exists:

```text
401 User no longer exists
```

is returned.

This prevents a deleted user's token from being treated as a valid application identity.

---

### 59. What happens if the JWT says `admin`, but the user is currently inactive?

**Answer:**

The database check takes the current user state into account.

If:

```text
isActive = false
```

the request is rejected even if the JWT itself is valid.

---

### 60. How would you improve this project for enterprise production?

**Answer:**

I would add:

```text
1. Short-lived access tokens
2. Refresh token rotation
3. Session/device management
4. MFA / 2FA
5. Password reset
6. Account lockout/risk-based authentication
7. Centralized structured logging
8. Security monitoring
9. Error tracking
10. Dependency vulnerability scanning
11. Automated security tests
12. Content Security Policy
13. Dedicated transactional email provider
14. Better CSRF/session binding strategy
15. CI/CD security checks
```

---

# 🧠 Quick-Fire Questions

| Question | Short Answer |
|---|---|
| JWT full form? | JSON Web Token |
| bcrypt purpose? | Password hashing |
| Joi purpose? | Input validation |
| Helmet purpose? | Security headers |
| CORS full form? | Cross-Origin Resource Sharing |
| CSRF full form? | Cross-Site Request Forgery |
| 401 means? | Authentication problem |
| 403 means? | Permission/forbidden |
| 429 means? | Too many requests |
| JWT stored where? | HttpOnly cookie |
| Database? | MongoDB Atlas |
| ODM? | Mongoose |
| Backend? | Node.js + Express |
| Frontend? | React + Vite |
| Backend deployment? | Render |
| Frontend deployment? | Vercel |
| Password stored as? | bcrypt hash |
| Admin security enforced where? | Backend |
| Secrets stored where? | Environment variables |
| Brute-force protection? | Rate limiting |
| CSRF protection? | csrf-csrf |
| Security headers? | Helmet |

---

# 🎯 Best 10 Questions to Prepare First

If the interviewer has limited time, prepare these questions extremely well:

```text
1. Explain your project.

2. How does your login system work?

3. Why did you use JWT?

4. Why did you store JWT in an HttpOnly cookie instead of localStorage?

5. Explain your authentication middleware.

6. Authentication vs authorization?

7. How does role-based authorization work?

8. What is CSRF and how did you protect against it?

9. How are passwords stored securely?

10. What security improvements would you make for enterprise production?
```

---

# 🗣️ 60-Second Project Explanation

If the interviewer says:

> "Explain your project."

You can answer:

> **"I built a full-stack authentication and authorization system using React, Node.js, Express and MongoDB. The application supports registration, login, logout, protected routes and role-based access for users and admins.**
>
> **For security, I used bcrypt for password hashing, JWT authentication with HttpOnly cookies instead of localStorage, Joi for backend input validation, CSRF protection for state-changing requests, rate limiting against brute-force attempts, Helmet for security headers and restricted CORS for the frontend origin.**
>
> **The backend follows a modular architecture with routes, controllers, middleware, models and validation layers. The frontend communicates with the backend through Axios.**
>
> **For deployment, I used Vercel for the React frontend, Render for the Node.js backend and MongoDB Atlas for the database. The project follows a defense-in-depth security approach rather than relying on a single security mechanism."**

---

# ⭐ Interview Tip

Don't just memorize the answers.

For every security feature, remember these three things:

```text
WHAT?
 ↓
WHAT DOES IT DO?

WHY?
 ↓
WHY DID I USE IT?

HOW?
 ↓
HOW DID I IMPLEMENT IT?
```

For example:

```text
HttpOnly Cookie

WHAT?
Prevents JavaScript from directly reading the cookie.

WHY?
To reduce authentication-token exposure to client-side JavaScript.

HOW?
JWT is set by the backend in an HttpOnly cookie and the frontend
uses withCredentials for authenticated API requests.
```

This approach makes it much easier to answer follow-up questions naturally during an interview.