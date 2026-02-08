# .NET Observability/Testing Web App Sample

A simple TaskManager (TODO) built with .NET Core 8.0 using PostgreSQL for data storage.

## Quick Setup

### 1. Check PostgreSQL
 Verify PostgreSQL is running

```bash
psql --version
```

### 2. Create Database
```bash
# Connect to PostgreSQL
psql -U postgres

# Create database
CREATE DATABASE TaskManagerDB;
\q
```

### 3. Configure Connection
Edit `appsettings.json`:
```json
"ConnectionStrings": {
  "DefaultConnection": "Host=localhost;Database=TaskManagerDB;Username=postgres;Password=YOUR_PASSWORD"
}
```

### 4. Build & Run

 Restore packages
```
dotnet restore
```
 Apply database migrations
```
dotnet ef database update
```
 Run the app
```
dotnet run
```

## Features
- Add/view/delete tasks

## Tech Stack
- ASP.NET Core 8.0
- PostgreSQL + Entity Framework Core
- Bootstrap 5
```
