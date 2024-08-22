# Roulettech-Assesment

# Screenshots
![Screenshot Note it](https://github.com/sithum20210380/Roulettech-Assesment/blob/main/frontend/src/assets/screenshots/ss1.png)


![Screenshot Note it](https://github.com/sithum20210380/Roulettech-Assesment/blob/main/frontend/src/assets/screenshots/ss2.png)

## Overview

This project demonstrates the implementation of a full-stack web application using React.js for the frontend and Django for the backend. The application features a simple web page built with React.js and a Django backend that provides API endpoints for CRUD operations.

## Features

- **Frontend**: A React.js web page showcasing the use of components.
- **Backend**: A Django application with API endpoints to perform CRUD operations.

## Technologies Used

- **Frontend**: React.js
- **Backend**: Django
- **Database**: SQLite (default with Django)
- **API Communication**: Fetch API (or Axios)

## Getting Started

### Prerequisites

- Python 3.x
- Node.js and npm/yarn
- Django
- React

### Frontend Setup

1. **Navigate to the Frontend Directory**

    ```bash
    cd frontend
    ```

2. **Install Dependencies**

    ```bash
    npm install
    # or
    yarn install
    ```

3. **Start the Development Server**

    ```bash
    npm start
    # or
    yarn start
    ```

   The frontend should now be running at [http://localhost:3000](http://localhost:3000).

### Backend Setup

1. **Navigate to the Backend Directory**

    ```bash
    cd backend
    ```

2. **Create and Activate a Virtual Environment**

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. **Install Dependencies**

    ```bash
    pip install -r requirements.txt
    ```

4. **Run Migrations**

    ```bash
    python manage.py migrate
    ```

5. **Start the Django Development Server**

    ```bash
    python manage.py runserver
    ```

   The backend API should now be running at [http://localhost:8000](http://localhost:8000).

## API Endpoints

### 1. **List Items**

- **Endpoint**: `/api/items/`
- **Method**: GET
- **Description**: Retrieve a list of items.

### 2. **Create Item**

- **Endpoint**: `/api/items/`
- **Method**: POST
- **Description**: Create a new item.
- **Request Body**:
    ```json
    {
        "name": "Item Name",
        "description": "Item Description"
    }
    ```

### 3. **Retrieve Item**

- **Endpoint**: `/api/items/{id}/`
- **Method**: GET
- **Description**: Retrieve details of a specific item.

### 4. **Update Item**

- **Endpoint**: `/api/items/{id}/`
- **Method**: PUT
- **Description**: Update a specific item.
- **Request Body**:
    ```json
    {
        "name": "Updated Item Name",
        "description": "Updated Item Description"
    }
    ```

### 5. **Delete Item**

- **Endpoint**: `/api/items/{id}/`
- **Method**: DELETE
- **Description**: Delete a specific item.

## Frontend

The React.js frontend includes:

- **Components**: 
  - `ItemList`: Displays a list of items.
  - `ItemForm`: Allows the creation and editing of items.

- **State Management**: 
  - Manages the state of items and interacts with the backend API.

## Backend

The Django backend includes:

- **Models**:
  - `Item`: Represents an item with attributes `name` and `description`.

- **Views**:
  - API views for CRUD operations on items.

- **Serializers**:
  - Converts model instances to JSON format and validates incoming data.

- **URLs**:
  - Configured to route requests to the appropriate views.

## Testing

### Frontend

1. **Run Tests**

    ```bash
    npm test
    # or
    yarn test
    ```

### Backend

1. **Run Tests**

    ```bash
    python manage.py test
    ```