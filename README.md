# Boarding House Management System

A web-based rental room management system designed to support boarding house operations such as account management, tenant and landlord workflows, room data, contracts, invoices, and authentication.

This project was built as a practical full-stack application, focusing on real business flow rather than only static CRUD screens.

---

## Overview

The system helps manage common rental house workflows between **landlords** and **tenants**. It provides a backend foundation for user authentication, role-based account handling, contract management, and database-driven rental operations.

The project demonstrates how a real-world management system can be structured with:

- RESTful API design
- Relational database modeling
- Authentication and authorization flow
- Business modules for rental room operations
- Server-side validation and error handling
- Automated testing setup

---

## Key Features

### Authentication & Account Management

- Register new accounts
- Login with JWT-based authentication
- Role-based account flow for landlords and tenants
- Password hashing with bcrypt
- Forgot password and reset password flow
- Basic input validation for username, password, and account profile data

### Landlord & Tenant Management

- Store landlord profile information
- Store tenant profile information
- Support different required fields based on account type
- Manage tenant status and related rental information

### Room & Rental Management

- Manage rental room information
- Support business data for room tracking
- Prepare backend structure for rental operation workflows

### Contract Management

- Create and manage rental contracts
- Retrieve contract list and contract details
- Link contracts with tenant data
- Track contract status
- Auto-check expired contracts with scheduled job logic

### Invoice & Billing Flow

- Support invoice-related management flow
- Handle invoice detail updates and rental payment-related data
- Prepare backend logic for boarding house financial tracking

### Testing Setup

- Jest configured for unit/integration testing
- Supertest configured for API endpoint testing
- Test database configuration uses in-memory SQLite for safer test execution

---

## Tech Stack

| Layer | Technology |
|---|---|
| Runtime | Node.js |
| Backend Framework | Express.js |
| Database | MySQL |
| ORM | Sequelize |
| Authentication | JWT, bcrypt |
| Testing | Jest, Supertest |
| Scheduler | node-cron |
| Package Manager | npm |

---

## Project Highlights for Reviewers

This repository shows practical backend thinking through:

- Separation between authentication, business modules, and database models
- Role-based registration flow for different user types
- Sequelize ORM usage for relational database operations
- JWT-based login flow with secure password hashing
- Contract expiration business rule handled through scheduled service logic
- Test-ready project setup with Jest and Supertest
- Clear direction toward a production-style rental management platform

---

## Business Roles

The system is designed around two main roles:

| Role | Description |
|---|---|
| Landlord | Manages rooms, tenants, contracts, and rental operations |
| Tenant | Registers account, stores personal information, and participates in rental workflows |

---

## Main Modules

```txt
Authentication
Account Management
Landlord Management
Tenant Management
Room Management
Contract Management
Invoice Management
Database Models
Scheduled Services
API Testing
```

---

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/binkadev/quanliphongtro.git
cd quanliphongtro
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

Create a `.env` file in the project root and configure values based on your local environment.

```env
PORT=3000
JWT_SECRET=your_jwt_secret
JWT_THOI_HAN=1h
DB_HOST=127.0.0.1
DB_USER=root
DB_PASSWORD=your_password
DB_NAME=your_database_name
DB_DIALECT=mysql
NODE_ENV=development
```

> The exact database name and credentials should match your local MySQL setup.

### 4. Run the server

```bash
npm start
```

### 5. Run tests

```bash
npm test
```

---

## Suggested API Areas

The project is structured around these API areas:

```txt
POST   /auth/register
POST   /auth/login
POST   /auth/forgot-password
POST   /auth/reset-password
GET    /contracts
GET    /contracts/:id
GET    /contracts/room/:roomId
```

> Endpoint paths may differ depending on the current route configuration. Check the routes folder before testing with Postman.

---

## Database Design Direction

The project uses Sequelize models to represent rental management entities such as:

- Accounts
- Roles
- Landlords
- Tenants
- Rooms
- Contracts
- Invoices

This reflects a relational design approach where business data is separated by responsibility and connected through model associations.

---

## What I Learned

Through this project, I practiced:

- Designing backend APIs for a real management system
- Working with MySQL and Sequelize ORM
- Implementing JWT authentication
- Handling role-based registration logic
- Structuring business modules around real user workflows
- Writing testable backend code with Jest and Supertest
- Thinking beyond simple CRUD by adding contract status and scheduled business logic

---

## Future Improvements

- Add complete API documentation with Swagger/OpenAPI
- Improve request validation with a validation middleware
- Add refresh token flow
- Add centralized error handling
- Add more integration tests for main business modules
- Add screenshots or demo video
- Add Docker setup for easier local development
- Improve README with database diagram and API examples

---

## Author

**Tran Hoang Hai**  
Software Engineering D22 - PTIT  
GitHub: [binkadev](https://github.com/binkadev)

---

## Status

This project is under active improvement and documentation cleanup.
