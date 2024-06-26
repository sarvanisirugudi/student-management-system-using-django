# Student Management System

The Student Management System is a Django-based web app for managing student details, allowing users to add, edit, update, and delete information with immediate updates. It ensures efficient database management, a user-friendly interface, and secure operations.

## Table of Contents
1. Project Setup
    - Install Django
    - Create a Django Project
    - Create a Django App
2. Run Migrations
3. Admin Interface
4. Running the Server
5. Create Superuser
6. Usage

## Project Setup

### Install Django

First, ensure you have Python installed on your system. Then, install Django using pip:

 ```bash
    pip install django
 ```
### Create a Django Project

Create a new Django project called `studentproject`:

 ```bash
    django-admin startproject studentproject
 ```

### Create a Django App

Within it, create a new app called `students`:

```bash
   django-admin startapp students .
```

### Add the App to Project Settings

Add the `students` app to your project's settings in `studentproject/settings.py`:

```python
    INSTALLED_APPS = [
        ...
        'students',
    ]
```

## Run Migrations

Create and apply initial migrations for your database:

```bash
    python manage.py makemigrations
    python manage.py migrate
```

## Admin Interface

To manage student records via the admin interface, register the `Student` model in `students/admin.py`:

```python
    from django.contrib import admin
    from .models import Student

    @admin.register(Student)
```
## Running the Server

Start the Django development server to run your application:

```bash
    python manage.py runserver
```
## Create Superuser
To access the Django admin interface, create a superuser:

 ```bash
    python manage.py createsuperuser
 ```

Follow the prompts to set up the superuser account.

## Usage

### Activate Virtual Environment

Clone the repository.
Before running the project, activate your virtual environment named `studentenvironment`. If you haven't created it yet, you can create it and activate it using the following commands:

```bash
    # Create a virtual environment named studentenvironment
    python -m venv studentenvironment
    # Activate the virtual environment (Windows)
    studentenvironment\Scripts\activate
```

Start the Django development server to run your application:

```bash
    python manage.py runserver
```

1. Access the admin interface at `http://127.0.0.1:8000/admin/` and log in using the superuser credentials.
2. Add, edit, update, and delete student records through the admin interface.

Open your browser and navigate to `http://127.0.0.1:8000/` to see your application running.

