# Event Management System (ASP.NET Core 8) - Web API

This is a simple ASP.NET Core 8 Web API project for an Event Management System using SQLite and Entity Framework Core.

## Requirements
- .NET 8 SDK installed
- (Optional) dotnet-ef tool for migrations: `dotnet tool install --global dotnet-ef`

## Setup
1. Restore packages:
   ```
   dotnet restore
   ```

2. Add EF Core tools (if not installed) and create initial migration:
   ```
   dotnet ef migrations add InitialCreate
   dotnet ef database update
   ```

   *If you prefer not to run migrations manually, the app will call `Database.Migrate()` on startup and create the SQLite DB automatically.*

3. Run the app:
   ```
   dotnet run
   ```

4. Open Swagger (in Development environment) at `https://localhost:5001/swagger` to test API endpoints.

## Project structure
- `Program.cs` - app entry and DI configuration
- `Data/ApplicationDbContext.cs` - EF Core DbContext
- `Models/Event.cs` - Event entity
- `Controllers/EventsController.cs` - CRUD API endpoints

## Notes
- This project intentionally targets a Web API (no front-end). You can add a React/Angular/Blazor frontend later or create Razor pages if desired.
