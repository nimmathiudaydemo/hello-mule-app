# Hello Mule App

A simple Mule 4 application that provides a "Hello World" REST API endpoint.

## Overview

This is a basic MuleSoft application that demonstrates:
- HTTP Listener configuration
- Simple JSON response
- Mule 4.6.0 runtime compatibility

## API Endpoint

- **URL**: `http://localhost:8081/hello`
- **Method**: GET
- **Response**: `{"message": "Hello World"}`
- **Content-Type**: application/json

## Project Structure

```
hello-mule-app/
├── src/
│   └── main/
│       └── mule/
│           └── hello.xml          # Main flow configuration
├── pom.xml                        # Maven configuration
├── mule-artifact.json            # Mule artifact descriptor
└── README.md                     # This file
```

## Prerequisites

- Java 8 or higher
- Maven 3.6 or higher
- MuleSoft Anypoint Studio (optional)

## Running the Application

1. **Local Development**:
   ```bash
   mvn clean compile
   mvn mule:run
   ```

2. **CloudHub Deployment**:
   - Requires CLIENT_ID and CLIENT_SECRET configured as environment variables
   - Deploy using Anypoint Platform or CI/CD pipeline

## Configuration

The application uses the following dependencies:
- Mule HTTP Connector 1.9.0
- Mule Sockets Connector 1.2.4
- Mule Validation Module 2.0.4

## Testing

Once the application is running, test the endpoint:
```bash
curl http://localhost:8081/hello
```

Expected response:
```json
{"message": "Hello World"}
```

## Deployment Secrets

This repository requires the following secrets for CloudHub deployment:
- `CLIENT_ID`: Anypoint Platform Client ID
- `CLIENT_SECRET`: Anypoint Platform Client Secret

These should be configured as GitHub repository secrets for CI/CD pipelines.