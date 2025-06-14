# ChatApp

ChatApp is a .NET 9 console application that demonstrates the integration of Microsoft's Semantic Kernel for building AI-powered conversational experiences.

Template was this project for .net 8: [tools-skills-net8/Chapter09](https://github.com/markjprice/tools-skills-net8/tree/main/code/Chapter09)

## Components

The project utilizes:

- Semantic Kernel for orchestrating AI capabilities and chat functions
- Microsoft Extensions Configuration for managing application settings
- Logging for console output and diagnostics
- HTTP Resilience for network communication

## Getting Started

### Prerequisites

- .NET 9 SDK (9.0.300 or later)
- Visual Studio 2022 or VS Code

### Project Location

**Note:** This ChatApp has been moved and integrated into the [ModernWeb solution](https://github.com/pstackebrandt/ModernWeb) where it works alongside other ASP.NET Core and Blazor projects. For the integrated version and to see how ChatApp interacts with web components, visit the ModernWeb repository.

This repository's future development status is uncertain. While the main implementation has moved to the ModernWeb solution, this repository may still be used for experimental features or extended versions of the ChatApp.

## Installation

```bash
cd ChatApp
dotnet restore
dotnet build
```

## Configuration

Create `appsettings.json`:

```json
{
  "Logging": {
    "LogLevel": {
      "Default": "Information"
    }
  },
  "SemanticKernel": {
    "ApiKey": "your-openai-api-key",
    "ModelId": "gpt-4"
  }
}
```

Environment variables can override settings using double underscore notation:

```bash
SemanticKernel__ApiKey=your-api-key
```

## Usage

```bash
dotnet run
```

## Purpose

The application leverages configuration from both appsettings.json and environment variables for flexible deployment scenarios. It demonstrates how to build a chat interface that combines traditional application data with AI-powered conversational abilities.

This project illustrates integration patterns for creating interactive, intelligent applications using .NET 9 and Microsoft Semantic Kernel.
