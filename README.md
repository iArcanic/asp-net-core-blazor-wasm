# ASP.NET Core Web App with Blazor WebAssembly Integration

This project consists of an ASP.NET Core web application that hosts and serves a Blazor WebAssembly SPA (Single Page Application).

## Project structure
- [asp-net-core-web-app](https://github.com/iArcanic/asp-net-core-blazor-wasm/tree/main/asp-net-core-web-app)
  - The main ASP.NET Core MVC web application
- [blazor-wasm-web-app](https://github.com/iArcanic/asp-net-core-blazor-wasm/tree/main/blazor-wasm-web-app)
  - The Blazor WebAssembly client-side project:
    - [Client](https://github.com/iArcanic/asp-net-core-blazor-wasm/tree/main/blazor-wasm-web-app/Client)
      - The actual WebAssembly Blazor app
    - [Server](https://github.com/iArcanic/asp-net-core-blazor-wasm/tree/main/blazor-wasm-web-app/Server)
      - Unused server Blazor hosting
    - [Shared](https://github.com/iArcanic/asp-net-core-blazor-wasm/tree/main/blazor-wasm-web-app/Shared)
      - Any shared code between client/server

# Development setup
- Install the latest .NET 7 SDK and any other relevant tools via the Visual Studio Installer
- Clone the repo and open the solution in Visual Studio
- Run the [asp-net-core-web-app](https://github.com/iArcanic/asp-net-core-blazor-wasm/tree/main/asp-net-core-web-app) project for the ASP.NET host
- [asp-net-core-web-app](https://github.com/iArcanic/asp-net-core-blazor-wasm/tree/main/asp-net-core-web-app) will serve the Blazor files and components

# Adding Blazor components
- Add new pages/components within the [blazor-wasm-web-app.Client](https://github.com/iArcanic/asp-net-core-blazor-wasm/tree/main/blazor-wasm-web-app/Client) project
- Reference them from [asp-net-core-web-app](https://github.com/iArcanic/asp-net-core-blazor-wasm/tree/main/asp-net-core-web-app) view pages or shared layout
- Use standard Blazor form handling, routing etc.

# Deployment
- Publish just the [asp-net-core-web-app](https://github.com/iArcanic/asp-net-core-blazor-wasm/tree/main/asp-net-core-web-app)
- [asp-net-core-web-app](https://github.com/iArcanic/asp-net-core-blazor-wasm/tree/main/asp-net-core-web-app);s published [wwwroot](https://github.com/iArcanic/asp-net-core-blazor-wasm/tree/main/asp-net-core-web-app/wwwroot) will contain Blazor files
- Can deploy to a hosting provider like other ASP.NET applications

# Implementation overview
- [asp-net-core-web-app](https://github.com/iArcanic/asp-net-core-blazor-wasm/tree/main/asp-net-core-web-app) sets up client-size Blazor hosting
- [Index.cshtml](https://github.com/iArcanic/asp-net-core-blazor-wasm/blob/main/asp-net-core-web-app/Pages/Index.cshtml) references counter example component
- ```MapFallbackToFile``` serves as ```index.html``` for non-file routes
