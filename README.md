# Task Manager API

This is a **Task Manager API** built using [FastAPI](https://fastapi.tiangolo.com/) and [SQLAlchemy](https://www.sqlalchemy.org/). It allows users to manage tasks, including creating, reading, updating, and deleting tasks.

## Features

- **Task management**: Create, read, and list tasks.
- **Swagger documentation**: Automatically generated API docs with FastAPI.
- **SQLAlchemy ORM**: Used for database operations.

## Technologies Used

- **FastAPI**: Web framework for building APIs.
- **SQLAlchemy**: ORM for database interactions.
- **Pydantic**: Data validation.
- **SQLite**: Default database (can be switched to PostgreSQL or MySQL).
- **Uvicorn**: ASGI server for running FastAPI apps.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/task-manager-api.git
   cd task-manager-api

2. Create and activate a virtual environment:
   ```bash
   python3 -m venv venv
   source venv/bin/activate

3. Install dependencies:
   ```bash
   pip install -r requirements.txt

4. Install additional dependencies (if needed):
   ```bash
   pip install sqlalchemy

## Database Setup

The default database is SQLite. If you need to use a different database (like PostgreSQL or MySQL), update the SQLALCHEMY_DATABASE_URL in database.py.


### Create a Database
   ```bash
   python -m app.database
   ```

This will create the SQLite database file.

## Running the Application

### Run the FastAPI application using Uvicorn:
   ```bash
   uvicorn app.main:app --reload
   ```
The application will start on http://127.0.0.1:8000.

### API Documentation

Once the app is running, visit http://127.0.0.1:8000/docs to see the auto-generated Swagger UI for the API.

You can also visit http://127.0.0.1:8000/redoc for the ReDoc API documentation.

## Endpoints

- **GET** /tasks/: Retrieve all tasks.
- **POST** /tasks/: Create a new task.
- **GET** /tasks/{id}: Retrieve a single task by its ID.
- **PUT** /tasks/{id}: Update a task by its ID.
- **DELETE** /tasks/{id}: Delete a task by its ID.

## Project Structure

```
task_manager/
│
├── app/
│   ├── main.py        # Application entry point
│   ├── models.py      # SQLAlchemy models
│   ├── schemas.py     # Pydantic schemas
│   ├── crud.py        # CRUD functions
│   └── database.py    # Database connection setup
│
├── .gitignore         # Ignored files in git
├── requirements.txt   # Python dependencies
└── README.md          # Project overview
```

### License

This project is licensed under the MIT License - see the LICENSE file for details.

```
This `README.md` provides installation instructions, an overview of the project structure, and guidance on how to run the API, ensuring users have everything needed to get started.
```