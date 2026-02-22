# 🏗️ C# Clean Architecture REST API

A production-ready RESTful API built with **ASP.NET Core** following **Clean Architecture** principles. Includes JWT authentication, full CRUD operations, and auto-generated Swagger documentation.

---

## 🚀 Tech Stack

| Layer | Technology |
|-------|-----------|
| Backend | ASP.NET Core 6 / C# |
| ORM | Entity Framework Core |
| Database | SQL Server |
| Auth | JWT Bearer Tokens |
| Docs | Swagger / OpenAPI |
| Container | Docker |

---

## 📁 Project Structure

```
src/
├── API/                  # Controllers, Middlewares, Program.cs
├── Application/          # Use Cases, DTOs, Interfaces
├── Domain/               # Entities, Business Rules
└── Infrastructure/       # EF Core, Repositories, DB Context
```

---

## ✨ Features

- ✅ Clean Architecture (Controller → Service → Repository)
- ✅ JWT Authentication & Authorization
- ✅ Full CRUD with Entity Framework Core
- ✅ Global error handling middleware
- ✅ Swagger UI with auth support
- ✅ Docker-ready

---

## ⚙️ Getting Started

### Prerequisites
- .NET 6 SDK
- SQL Server
- Docker (optional)

### Run locally

```bash
# Clone the repo
git clone https://github.com/elouafi-abderrahmane-2002/csharp-clean-architecture-api.git
cd csharp-clean-architecture-api

# Update connection string in appsettings.json
# Then run migrations
dotnet ef database update

# Start the API
dotnet run --project src/API
```

### Run with Docker

```bash
docker build -t clean-api .
docker run -p 5000:5000 clean-api
```

---

## 📡 API Endpoints

```
POST   /api/auth/login        → Get JWT token
POST   /api/auth/register     → Register new user

GET    /api/items             → Get all items
GET    /api/items/{id}        → Get item by ID
POST   /api/items             → Create item
PUT    /api/items/{id}        → Update item
DELETE /api/items/{id}        → Delete item
```

---

## 🔐 Authentication

```http
POST /api/auth/login
Content-Type: application/json

{
  "email": "user@example.com",
  "password": "yourpassword"
}
```

Use the returned token in subsequent requests:
```
Authorization: Bearer <your_token>
```

---

## 👤 Author

**Abderrahmane ELOUAFI**  
[LinkedIn](https://www.linkedin.com/in/abderrahmane-elouafi-43226736b/) · [GitHub](https://github.com/elouafi-abderrahmane-2002) · [Portfolio](https://my-first-porfolio-six.vercel.app/)
