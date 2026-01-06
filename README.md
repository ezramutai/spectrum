# Spectrum

**Spectrum** is a modular, role-based Point of Sale (POS) and business management system built with the **MEAN stack**.  
It is designed around real-world organizational roles such as **Admin, Manager, HR, and Cashier**, with strict **Role-Based Access Control (RBAC)** and secure authentication.

The project prioritizes **architecture, security, and scalability** before feature expansion.

---

## 🎯 Project Vision

Spectrum aims to provide a unified system for:

- Sales and POS operations
- Inventory and stock management
- Supply and procurement
- Human Resources (HR)
- Reporting and auditing
- System administration

Users are authenticated once and **automatically routed** to the correct area of the system based on their role.

---

## 🧠 Core Principles

- Role-Based Access Control (RBAC)
- Authentication-first development
- Role-specific layouts and routing
- Backend as the source of truth
- Scalable, enterprise-style architecture

This project intentionally starts with **login, routing, and access control** before implementing business features.

---

## 🧑‍💼 Supported Roles

| Role     | Description |
|---------|-------------|
| Admin   | Full system control and configuration |
| Manager | Business oversight, reports, inventory |
| HR      | Employee management and activity logs |
| Cashier | Sales and POS operations |

Each role:
- Has a dedicated layout
- Is restricted to specific routes
- Cannot access unauthorized areas

---

## 🗺️ Role-Based Landing Routes

| Role     | Default Route |
|---------|----------------|
| Admin   | `/admin/dashboard` |
| Manager | `/manager/overview` |
| HR      | `/hr/employees` |
| Cashier | `/pos` |

After login, users are **automatically redirected** based on their assigned role.

---

## 🧱 Frontend Architecture (Angular)

Spectrum uses **Angular standalone components** with a clean, scalable folder structure:


### Architectural Decisions
- No Angular modules (`NgModule`)
- Standalone components only
- Route guards enforce RBAC
- UI never trusts client-side role selection

---

## 🔐 Authentication Strategy

- Email / Staff ID + Password
- JWT-based authentication
- Role returned from backend after login
- Planned biometric authentication using **WebAuthn**

Authorization is enforced on both frontend and backend.

---

## 🚧 Project Status

- ✅ Angular project scaffolding
- ✅ Role-based layouts
- ✅ Login UI
- ✅ RBAC-ready routing structure
- 🚧 Authentication logic
- 🚧 Backend (Node.js + Express)
- 🚧 POS, HR, Inventory features

---

## 🛠️ Tech Stack

### Frontend
- Angular (Standalone Components)
- TypeScript
- CSS (Tailwind planned)

### Backend (Planned)
- Node.js
- Express
- MongoDB
- JWT Authentication
- WebAuthn (Biometrics)

---

## 🚀 Getting Started

### Prerequisites
- Node.js v18+
- Angular CLI

### Install Angular CLI
```bash
npm install -g @angular/cli
