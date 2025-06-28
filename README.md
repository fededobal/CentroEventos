# .NET Seminar - University Sports Center Management System (Final Project)

## Team Members

  * Bie, Leandro [@](https://github.com/leandrobie)
  * Castañeda, Isabella [@](https://github.com/isa-cast)
  * Dobal, Federico ***.this***
  * Villca, Facundo [@](https://github.com/EIKOO1)

## General Description

This project is the final version of the **University Sports Center Management System**. Building upon a base with event, person, and reservation management, this version expands functionality to include comprehensive user management, a new web interface, and data persistence through a database.

## Key Features

  * **User Management**: Complete functionality for managing system users, including first name, last name, email, and password. The first registered user assumes the Administrator role with full permissions. The Administrator can delegate user management permissions to other accounts. New users start with read-only permissions.
  * **Web Interface with Blazor**: A new user interface was developed using Blazor in a project called `CentroEventos.UI`, replacing the previous console application.
  * **Persistence with Entity Framework Core**: Entity Framework Core is used with a SQLite database to persist all information, applying a "code-first" methodology.
  * **Password Security**: Passwords are not stored in plain text; instead, a hash (using SHA-256) is stored to ensure security.
  * **Authentication and Session**: User login and registration flow. The user session is managed through a Scoped service in Blazor.

## System Architecture

The project maintains a Clean Architecture to ensure low coupling and high cohesion among its components.

  * **CentroEventos.Aplicacion**: The core of the system, containing business logic, entities, use cases, and interfaces.
  * **CentroEventos.Repositorios**: Data access layer that implements application interfaces using Entity Framework Core and SQLite.
  * **CentroEventos.UI**: The presentation layer, developed with Blazor. It is the entry point for the end-user.

## Instructions to Run the Program

### Prerequisites

  * **.NET 8.0** SDK - [Download](https://dotnet.microsoft.com/es-es/download/dotnet/8.0).
  * **SQLite** Database Manager - [Download](https://sqlite.org/download.html).

### Steps to Execute

1.  **Clone the repository**:
    ```bash
    git clone https://github.com/fededobal/CentroEventos.git
    ```
2.  **Navigate to the solution directory**:
    ```bash
    cd CentroEventos/CentroEventos
    ```
3.  **Navigate to the UI project**:
    ```bash
    cd CentroEventos.UI
    ```
4.  **Run the application**:
    ```bash
    dotnet run
    ```
5.  **Open in browser**: Once the application is running, go to the address indicated in the console (`http://localhost:xxxx`). The first time it runs, Entity Framework will automatically create the SQLite database thanks to code first.
