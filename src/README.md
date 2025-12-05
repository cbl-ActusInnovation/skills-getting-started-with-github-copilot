# Mergington High School Activities API

A super simple FastAPI application that allows students to view and sign up for extracurricular activities.

## Features

- View all available extracurricular activities
- Sign up for activities

## Getting Started

1. Install the dependencies:

   ```
   pip install fastapi uvicorn
   ```

2. Run the application:

   ```
   python app.py
   ```

3. Open your browser and go to:
   - API documentation: http://localhost:8000/docs
   - Alternative documentation: http://localhost:8000/redoc

## API Endpoints

| Method | Endpoint                                                          | Description                                                         |
| ------ | ----------------------------------------------------------------- | ------------------------------------------------------------------- |
| GET    | `/activities`                                                     | Get all activities with their details and current participant count |
| POST   | `/activities/{activity_name}/signup?email=student@mergington.edu` | Sign up for an activity                                             |

## Data Model

The application uses a simple data model with meaningful identifiers:

1. **Activities** - Uses activity name as identifier:

   - Description
   - Schedule
   - Maximum number of participants allowed
   - List of student emails who are signed up

2. **Students** - Uses email as identifier:
   - Name
   - Grade level

All data is stored in memory, which means data will be reset when the server restarts.

## FAQ

### What is GitHub Codespaces?

[GitHub Codespaces](https://github.com/features/codespaces) is a cloud-based development environment that allows you to code directly in your browser or through VS Code. It provides a fully configured development environment with all the tools and dependencies you need, eliminating the need for local setup.

### What is the difference between a "GitHub Space" and a "GitHub Codespace"?

**"GitHub Space" is not an official GitHub product or term.** The correct term is **GitHub Codespaces** (or GitHub Codespace for a single instance). If you've heard the term "GitHub Space," it may be a shortened or informal reference to GitHub Codespaces.

GitHub Codespaces provides:
- A cloud-hosted development environment
- Pre-configured containers with your project's dependencies
- Integration with VS Code (in browser or desktop)
- Port forwarding for testing web applications
- Persistent storage for your work
