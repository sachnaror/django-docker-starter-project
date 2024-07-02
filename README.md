# DjangoBoilerPlate

## Description and Purpose

A well-organised project structure is essential for the success of any Django application. By adhering to best practices and adopting a consistent structure, you’ll not only streamline development but also ensure your project remains manageable, maintainable, and scalable. Whether you’re starting a new project or refactoring an existing one, investing time in structuring your Django application is a wise decision that pays off in the long run.

# Project Name

A Django project with the app name "App". (You can give any name to your project and app. I gave the name 'backend' for reference sake here)

## Why Project Structure Matters

Before diving into the specifics, let’s understand why a well-defined project structure matters:

- **Maintainability**: A clear project structure makes it easier to locate and update different parts of your application. This is particularly important as your project grows.

- **Collaboration**: When working in teams, a standardized structure helps team members understand where to find specific code and resources.

- **Scalability**: A well-structured project can be easily extended without introducing unnecessary complexity.

## Directory and File Structure

Here’s a breakdown of the common components you might find in a well-structured Django project:


<pre>
```
project_name/
├── app/
│   ├── api/
│   │   └── v1/
│   │       ├── serializers.py
│   │       ├── urls.py
│   │       └── views.py
│   ├── migrations/
│   │   └── __init__.py
│   ├── static/
│   │   └── app/
│   │       ├── css
│   │       ├── img
│   │       └── js
│   ├── templates/
│   │   └── app/
│   ├── test/
│   │   ├── test_models.py
│   │   ├── test_setup.py
│   │   └── test_views.py
│   ├── __init__.py
│   ├── actions.py
│   ├── admin.py
│   ├── apps.py
│   ├── constants.py
│   ├── exceptions.py
│   ├── filters.py
│   ├── forms.py
│   ├── managers.py
│   ├── messages.py
│   ├── models.py
│   └── views.py
├── backend/
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── common/
│   ├── __init__.py
│   ├── constants.py
│   ├── custom_logger.py
│   ├── exceptions.py
│   ├── filters.py
│   ├── generics.py
│   ├── messages.py
│   ├── mixins.py
│   ├── models.py
│   ├── pagination.py
│   ├── permissions.py
│   ├── swagger.py
│   ├── utils.py
│   └── viewsets.py
├── static/
│   ├── css
│   ├── img
│   └── js
├── templates/
├── .dockerignore
├── .gitignore
├── .sample.env
├── Dockerfile
├── docker-compose.yaml
├── manage.py
└── requirements.txt
```
</pre>



### Components Explained

1. **backend/**: This is the root directory of your Django project, containing settings, routing, and other high-level configurations.

   - **settings.py**: Houses project-wide settings, including database configurations, middleware, and installed apps.
   - **urls.py**: Manages URL routing for your application.
   - **asgi.py**: Handles asynchronous requests and is used with ASGI-compatible servers, ideal for real-time applications.
   - **wsgi.py**: Handles synchronous requests and is used with WSGI-compatible servers, suitable for traditional web applications.

2. **app/**: Within this directory, you create Django apps, each with a specific purpose. Apps are reusable components that can be integrated into other projects.

   - **api/**: Subdirectory for organizing API-related code.
   - **v1/**: You can version your API by creating subdirectories for different versions.
   - **serializers.py**: Defines how data is converted to and from Python objects.
   - **views.py**: Defines your API views.
   - **urls.py**: Handles URL routing for this API version.
   - **migrations/**: Stores Django migration files, managing database schema changes.
   - **static/**: Houses static files (CSS, JavaScript, images) specific to this app.
   - **templates/**: Contains HTML templates for rendering views.
   - **test/**: Location for writing unit tests for this app.

3. **common/**: This directory is often used to store shared code, constants, utilities, and mixins.

   - **constants.py**: For constants and configuration values.
   - **custom_logger.py**: Custom logging configurations.
   - **exceptions.py**: Implement custom exceptions if needed.
   - **filters.py**: Custom filters for querying data.
   - **messages.py**: Store messages and error messages.
   - **models.py**: Shared models that can be reused across different apps.
   - **permissions.py**: Define custom permissions for your project.
   - **utils.py**: General-purpose utility functions.
   - **viewsets.py**: Define custom viewsets for your project.

4. **static/**: This directory stores static files shared across the entire project.

5. **templates/**: Templates shared across different apps or the entire project.

6. **Other Files**: Various configuration and utility files like `.dockerignore`, `.gitignore`, `Dockerfile`, `docker-compose.yaml`, `manage.py`, and `requirements.txt` are crucial for managing development and deployment processes.



