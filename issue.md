# Issue: Setup Project Skeleton with Bun, ElysiaJS, Drizzle, and MySQL

## Goal
Initialize a new web service project using the Bun runtime, featuring a high-performance API layer with ElysiaJS and a type-safe database layer with Drizzle ORM connected to MySQL.

## High-Level Requirements

### 1. Project Initialization
- Initialize a new Bun project in the current directory.
- Configure `package.json` with essential metadata.
- Set up TypeScript configuration (`tsconfig.json`) optimized for Bun and Elysia.

### 2. Dependency Management
- Install **ElysiaJS** as the primary web framework.
- Install **Drizzle ORM** and the `mysql2` driver.
- Install development dependencies including `drizzle-kit` for migrations.

### 3. Database Schema & Connection
- Define a base Drizzle schema (e.g., a simple `users` or `items` table) to validate the setup.
- Implement a database connection module using Drizzle and the MySQL driver.
- Configure environment variable handling (e.g., `.env`) for database credentials (HOST, USER, PASSWORD, DATABASE).

### 4. API Foundation
- Create a basic Elysia application instance.
- Implement a health check endpoint (`GET /health`) that confirms the API is running.
- Set up a sample route that interacts with the database using Drizzle to ensure the full stack is integrated.

### 5. Developer Experience
- Configure `drizzle-kit` for schema pushing and migration generation.
- Add Bun scripts for:
    - `dev`: Running the Elysia server in watch mode.
    - `db:push`: Syncing the schema to the database.
    - `db:generate`: Generating migration files.

## Definition of Done
- Bun is configured and running.
- ElysiaJS server responds to requests.
- Drizzle can successfully query and mutate data in a MySQL instance.
- Project structure is clean and ready for further feature development.
