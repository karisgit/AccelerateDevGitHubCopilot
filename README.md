# Library App

## Description
Library App is a small .NET solution that demonstrates a layered architecture for a console-based sample application. It includes an application core with entities and interfaces, an infrastructure project, a console front-end, and unit tests.

## Project Structure
- [AccelerateDevGitHubCopilot.sln](AccelerateDevGitHubCopilot.sln)
- src/
    - [Library.ApplicationCore](src/Library.ApplicationCore/Library.ApplicationCore.csproj)
        - Entities/
        - Enums/
        - Interfaces/
        - Services/
    - [Library.Infrastructure](src/Library.Infrastructure/Library.Infrastructure.csproj)
        - Data/
    - [Library.Console](src/Library.Console/Library.Console.csproj)
        - [appSettings.json](src/Library.Console/appSettings.json)
        - [CommonActions.cs](src/Library.Console/CommonActions.cs)
        - [ConsoleApp.cs](src/Library.Console/ConsoleApp.cs)
        - [ConsoleState.cs](src/Library.Console/ConsoleState.cs)
        - [Program.cs](src/Library.Console/Program.cs)
- tests/
    - UnitTests/
        - [LoanFactory.cs](tests/UnitTests/LoanFactory.cs)
        - (unit test files)

## Key Classes and Interfaces
- Front-end / Console
  - [`Library.Console.ConsoleApp`](src/Library.Console/ConsoleApp.cs)
  - [`Library.Console.CommonActions`](src/Library.Console/CommonActions.cs)
  - [`Library.Console.ConsoleState`](src/Library.Console/ConsoleState.cs)
  - [`Library.Console.Program`](src/Library.Console/Program.cs)
- Core and Infrastructure
  - [`Library.ApplicationCore` project](src/Library.ApplicationCore/Library.ApplicationCore.csproj)
  - [`Library.Infrastructure` project](src/Library.Infrastructure/Library.Infrastructure.csproj)
- Tests
  - [`UnitTests.LoanFactory`](tests/UnitTests/LoanFactory.cs)

> Note: The ApplicationCore contains domain entities, interfaces and service contracts under src/Library.ApplicationCore/. The Infrastructure project implements persistence and data access under src/Library.Infrastructure/.

## Usage
Build and run the solution using the .NET CLI:

```bash
dotnet restore
dotnet build
dotnet run --project src/Library.Console/Library.Console.csproj
```

Run unit tests:

```bash
dotnet test tests/UnitTests/UnitTests.csproj
```

## License
This project is provided under the MIT License. Add a LICENSE file at the repository root to include the full license text.

---
For quick navigation, open the solution: [AccelerateDevGitHubCopilot.sln](AccelerateDevGitHubCopilot.sln)

