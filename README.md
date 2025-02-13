# FastAPI Application

This is a FastAPI application that provides an API for a user management system. The application uses SQLAlchemy to interact with a SQLite database and supports the following features:

1. **User Management**:
   - Add a new user
   - Change a user's password
   - Block and unblock a user
   - Login functionality

2. **Request Management**:
   - Create a new request
   - Approve or deny a request
   - Connect a request to a user
   - Mark a request as completed

3. **Thread Management**:
   - Create a new thread
   - Add comments to a thread

4. **Rating Management**:
   - Add a review for a completed request
   - Calculate the average rating for all requests

5. **Reporting**:
   - Get a list of all approved requests
   - Get a list of all unapproved requests
   - Get a list of all users (excluding blocked users)
   - Get the average rating for all requests

## Requirements

- Python 3.7 or later
- FastAPI
- SQLAlchemy
- Uvicorn

## Installation

1. Clone the repository:
https://github.com/mosesberco/ComuNeedy.git
2. Navigate to the project directory:
   cd fastapi-app
4. Create a virtual environment and activate it:
   venv\Scripts\activate
5. Install the required dependencies:
   pip install -r requirements.txt
## Usage

1. Start the application:
uvicorn main:app --reload
2. Access the API documentation at `http://localhost:8000`.

## Deployment

To deploy the application, you can use a production-ready server like Gunicorn or Nginx. Here's an example using Gunicorn:

1. Install Gunicorn:
pip install gunicorn
2. Create a `gunicorn.conf.py` file in the project directory with the following content:
```python
bind = "0.0.0.0:8000"
workers = 4
3. start the app:
gunicorn -c gunicorn.conf.py main:app
