# Django ToDo List Application

This is a simple ToDo List application built with Django. It allows users to register, log in, and manage their tasks. Users can add, update, and delete tasks from their list.

## Features

- User Registration
- User Authentication (Login/Logout)
- Add ToDo tasks
- Update task status
- Delete tasks
- Task management is user-specific

## Requirements

- Python 3.x
- Django 3.x or later
- SQLite (default database for development)

## Installation

1. **Clone the repository:**

    ```bash
    git clone https://github.com/nityakommana/Todolist-App.git
    cd todolist-app
    ```

2. **Create a virtual environment and activate it:**

    ```bash
    python -m venv env
    source env/bin/activate  # On Windows use `env\Scripts\activate`
    ```

3. **Install the dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

4. **Run migrations:**

    ```bash
    python manage.py migrate
    ```

5. **Create a superuser (optional, for admin access):**

    ```bash
    python manage.py createsuperuser
    ```

6. **Run the development server:**

    ```bash
    python manage.py runserver
    ```

7. **Open your browser and navigate to:**

    ```
    http://127.0.0.1:8000
    ```

## Usage

1. **Register an account** by clicking on the Register link.
2. **Log in** with your credentials.
3. **Add tasks** using the task input form on the homepage.
4. **Update task status** by clicking on the update link next to the task.
5. **Delete tasks** by clicking on the delete link next to the task.

## Project Structure

```plaintext
todolist-app/
│
├── manage.py
├── todoapp/
│   ├── migrations/
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── tests.py
│   ├── views.py
│   ├── urls.py
│   └── templates/
│       └── todoapp/
│           ├── login.html
│           ├── register.html
│           └── todo.html
├── todolist/
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
└── requirements.txt
```

## Views

- **home**: Displays the user's ToDo list and allows adding new tasks.
- **register**: Handles user registration.
- **loginpage**: Handles user login.
- **LogoutView**: Logs out the user.
- **DeleteTask**: Deletes a specified task.
- **Update**: Updates the status of a specified task.

## Models

- **todo**: Represents a task with fields for the user, task name, and status.

## URLs

- `/`: Home page (requires login)
- `/register`: User registration page
- `/login`: User login page
- `/logout`: Logs out the user
- `/delete/<task_name>`: Deletes a specific task
- `/update/<task_name>`: Updates the status of a specific task

## Templates

- `login.html`: Template for the login page
- `register.html`: Template for the registration page
- `todo.html`: Template for the home page (task list)

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

This application was created as a learning project for understanding Django user authentication and task management.

## Contact

For any inquiries, please contact [nityakommana@gmail.com]