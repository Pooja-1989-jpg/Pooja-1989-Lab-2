# 📘 Assignment: Building REST APIs with FastAPI

## 🎯 Objective

Learn how to design and implement a simple RESTful API using the FastAPI framework in Python. Students will practice creating endpoints, handling requests/responses, and running the application with uvicorn.

## 📝 Tasks

### 🛠️ Set up a FastAPI Application

#### Description
Create a basic FastAPI application with a few endpoints to serve JSON data.

#### Requirements
Completed program should:

- Install `fastapi` and `uvicorn` (note this can be mentioned in comments or requirements).
- Define a FastAPI app instance in a file (e.g., `main.py`).
- Add a root (`/`) GET endpoint that returns a welcome message JSON.
- Start the server using `uvicorn` so that the API is reachable at `http://localhost:8000`.

### 🛠️ Create CRUD Endpoints

#### Description
Extend the application by adding CRUD-style routes for a simple resource, such as `items`.

#### Requirements
Completed program should:

- Define an in-memory store (e.g., a dictionary or list) for items with `id`, `name`, and `description`.
- Implement the following endpoints:
  - `GET /items` to return all items
  - `GET /items/{item_id}` to return a single item by ID (404 if not found)
  - `POST /items` to create a new item (accept JSON payload)
  - `PUT /items/{item_id}` to update an existing item
  - `DELETE /items/{item_id}` to remove an item
- Use appropriate status codes for each response.

### 🛠️ Use Pydantic Models and Validation

#### Description
Define request and response models using Pydantic to enforce data validation.

#### Requirements
Completed program should:

- Create Pydantic models for `ItemCreate` and `Item`.
- Use these models in the endpoint function signatures.
- Validate incoming JSON and return meaningful error messages for invalid data.
