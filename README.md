# Todo Web API

## Stack and Tooling

- ASP.NET Core .NET 6
- IDE Visual Studio Code

## Create Initial Project

1. Create Solution by running:
    dotnet new sln
2. Create Web.Api project and Web.Api.Tests project from the solution

## Run the App

```bash
dotnet run --project src/Todo.Api --launch-profile "Todo.Api"
```
then go to:

https://localhost:7098/swagger/index.html

## Run Local Infra

```bash
docker compose up -d
docker compose down
```

## Add Packages

```bash
dotnet add package NSwag.AspNetCore
dotnet add package Microsoft.EntityFrameworkCore -v 6.0.4
dotnet add package Microsoft.EntityFrameworkCore.Design -v 6.0.4
dotnet add package Microsoft.EntityFrameworkCore.SqlServer -v 6.0.4
dotnet add package Microsoft.EntityFrameworkCore.Tools -v 6.0.4
```

## Install ef tool globall
dotnet tool install --global dotnet-ef

## Create Migration

```bash
dotnet ef migrations add InitialCreate
dotnet ef database update
```