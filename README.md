# ⚰️ Cemetery Management System

A scalable, secure, and high-performance **Cemetery Management System** for booking graves, managing burial records, and registering interments. Built using **.NET Core**, **HTML/CSS/JavaScript**, and a **Clean Architecture** approach. Designed for multi-tenant environments with enterprise-grade authentication, optimized logging, and database performance for millions of records.

---

## 🚀 Core Features

- ✅ Grave Booking & Availability Calendar
- 🪦 Burial Register with Filtering & Export
- 📄 Interment Record Management (Deceased, Burial, Date, Plot)
- 🏛️ Cemetery & Section Management
- 👥 Multi-Tenant Support (Admin, Staff Roles)
- 🔐 Auth0 Integration for Secure Authentication
- 📊 Audit Logs & Activity Trails
- 🔎 Searchable Ledger with Millions of Records (Indexed & Optimized)
- 🧾 PDF Certificate generation for interments
- 🌐 Multi-language support
- 📥 Bulk import from Excel/CSV
- 🛰️ Live cemetery map integration (Google Maps)
- 🛡️ Rate limiting and API key management for public access


---

## ⚙️ Tech Stack

| Technology     | Purpose                                        |
|----------------|------------------------------------------------|
| .NET 8 (ASP.NET Core) | Backend Framework                         |
| Entity Framework Core | ORM & Database Access                    |
| SQL Server / PostgreSQL | Relational DB, optimized for scale     |
| HTML/CSS/JavaScript | Frontend Interface                         |
| Auth0          | Authentication & Authorization (OAuth2/OIDC)  |
| Serilog        | Structured Logging                             |
| MediatR        | CQRS & Clean Architecture Messaging            |
| AutoMapper     | DTO Mapping                                    |
| Swagger        | API Documentation                              |
| Docker (Optional) | Containerization Support                    |

---

## 🧱 Architecture Overview

The project follows **Clean Architecture**, ensuring high cohesion, low coupling, and testability.


- **CQRS + MediatR**: All commands/queries are decoupled via request/response pipelines.
- **Multi-Tenant Support**: Data is segregated at the DB level (TenantId column), services scoped accordingly.
- **Modular Services**: Auth, Booking, Registering Burials are separate services for scaling.

---

## 🗄️ Database Design Highlights

- Optimized for **millions of records** using:
  - Indexed columns (`GraveId`, `DateOfBurial`, `TenantId`)
  - Partitioning (if using SQL Server)
  - Batched inserts and soft deletes
- Relational integrity with `Foreign Keys`:
  - `Tenant → Cemetery → Grave → Interment → Deceased`
- Uses `GUIDs` for global uniqueness

---

## 🔐 Authentication & Authorization

- Integrated with **Auth0**
- Supports:
  - JWT-based secure access tokens
  - Role-based permissions (Admin, Registrar, Viewer)
  - Multi-tenant separation via `TenantId` claims
- Middleware checks and guards for sensitive routes

---

## 🪵 Logging & Monitoring

- **Serilog** used for:
  - Structured logs to file/console/Seq
  - Logging request/response and exceptions
  - Per-tenant activity tracing
- Ready for integration with **Azure Monitor** or **ELK stack**

---

## 🌐 API Documentation

- Swagger enabled at `/swagger`
- Fully documented endpoints with:
  - Examples
  - Auth headers
  - Required/optional fields

---


## 🖼️ Screenshots


### 🏠 Dashboard / Home Page  
![Dashboard](https://i.postimg.cc/6qbfct6w/Screenshot-2025-07-05-010427.png)

### 📆 Booking a Grave  
![Booking a Grave](https://i.postimg.cc/wB55Phxw/Screenshot-2025-07-05-010613.png)

### 🪦 Burial Register View  
![Burial Register View](https://i.postimg.cc/wB55Phxw/Screenshot-2025-07-05-010613.png)

### 📋 Interment Details Entry  
![Interment Details Entry](https://i.postimg.cc/hPH9tCfC/Screenshot-2025-07-05-010651.png)

### 🔐 One Link User Access Details  
![User Access](https://i.postimg.cc/XYSCbpzm/Screenshot-2025-07-05-010547.png)



