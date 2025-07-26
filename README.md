# Library App

## Description

Library App is a modular .NET application for managing library operations, including patron management, book loans, and membership renewals. It features a console interface and uses JSON files for data persistence. The solution is organized for extensibility and includes unit tests for core functionality.

## Project Structure

- AccelerateDevGitHubCopilot.sln
- README.md
- src/
  - Library.ApplicationCore/
    - Library.ApplicationCore.csproj
    - Entities/
    - Enums/
    - Interfaces/
    - Services/
  - Library.Console/
    - appSettings.json
    - CommonActions.cs
    - ConsoleApp.cs
    - ConsoleState.cs
    - Library.Console.csproj
    - Program.cs
    - Json/
  - Library.Infrastructure/
    - Library.Infrastructure.csproj
    - Data/
- tests/
  - UnitTests/
    - LoanFactory.cs
    - ...

## Key Classes and Interfaces

- `ConsoleApp` ([src/Library.Console/ConsoleApp.cs](src/Library.Console/ConsoleApp.cs)): Main console application logic and state management.
- `JsonData` ([src/Library.Infrastructure/Data/JsonData.cs](src/Library.Infrastructure/Data/JsonData.cs)): Handles loading and saving entities to JSON files.
- `JsonPatronRepository` ([src/Library.Infrastructure/Data/JsonPatronRepository.cs](src/Library.Infrastructure/Data/JsonPatronRepository.cs)): Data access for patrons.
- `JsonLoanRepository` ([src/Library.Infrastructure/Data/JsonLoanRepository.cs](src/Library.Infrastructure/Data/JsonLoanRepository.cs)): Data access for loans.
- `IPatronRepository`, `ILoanRepository` ([src/Library.ApplicationCore/Interfaces/](src/Library.ApplicationCore/Interfaces/)): Interfaces for repository abstraction.
- `ILoanService`, `IPatronService` ([src/Library.ApplicationCore/Services/](src/Library.ApplicationCore/Services/)): Service interfaces for business logic.

## Usage

1. Build the solution using Visual Studio or `dotnet build`.
2. Run the console application:
   ```sh
   dotnet run --project src/Library.Console/Library.Console.csproj