## Endpoints

- **GET /tasks**: Retrieve a list of all tasks.
- **GET /tasks/:id**: Retrieve a specific task by ID.
- **POST /tasks**: Create a new task.
- **PATCH /tasks/:id**: Update an existing task by ID.
- **DELETE /tasks/:id**: Delete a task by ID.

## Usage

1. Clone this repository:
   ```
   https://github.com/karuna-sagar/BackEnd-Project.git
   git clone 
   ```

2. Install dependencies:
   ```
   cd task-management-api
   npm install
   ```

3. Start the server:
   ```
   npm start
   ```

4. The API server will start running at `http://localhost:3000`.

## Documentation

### GET /tasks

Retrieve a list of all tasks.

- **Method**: GET
- **URL**: `/tasks`
- **Response**:
  - **Status Code**: 200 OK
  - **Body**:
    ```json
    [
      {
        "id": 1,
        "title": "Task 1",
        "description": "Description 1"
      },
      {
        "id": 2,
        "title": "Task 2",
        "description": "Description 2"
      }
    ]
    ```

### POST /tasks

Create a new task.

- **Method**: POST
- **URL**: `/tasks`
- **Request Body**:
  ```json
  {
    "title": "New Task",
    "description": "Description of the new task"
  }
  ```
- **Response**:
  - **Status Code**: 201 Created
  - **Body**:
    ```json
    {
      "id": 3,
      "title": "New Task",
      "description": "Description of the new task"
    }
    ```

### GET /tasks/:id

Retrieve a specific task by ID.

- **Method**: GET
- **URL**: `/tasks/:id`
  - Replace `:id` with the ID of the task you want to retrieve.
- **Response**:
  - **Status Code**: 200 OK
  - **Body**:
    ```json
    {
      "id": 1,
      "title": "Task 1",
      "description": "Description 1"
    }
    ```
  - **Status Code**: 404 Not Found
    - If the task with the specified ID does not exist.

### PATCH /tasks/:id

Update an existing task by ID.

- **Method**: PATCH
- **URL**: `/tasks/:id`
  - Replace `:id` with the ID of the task you want to update.
- **Request Body**:
  ```json
  {
    "title": "Updated Task",
    "description": "Updated description of the task"
  }
  ```
- **Response**:
  - **Status Code**: 200 OK
  - **Body**:
    ```json
    {
      "id": 1,
      "title": "Updated Task",
      "description": "Updated description of the task"
    }
    ```
  - **Status Code**: 404 Not Found
    - If the task with the specified ID does not exist.

### DELETE /tasks/:id

Delete a task by ID.

- **Method**: DELETE
- **URL**: `/tasks/:id`
  - Replace `:id` with the ID of the task you want to delete.
- **Response**:
  - **Status Code**: 204 No Content
    - Indicates successful deletion.
  - **Status Code**: 404 Not Found
    - If the task with the specified ID does not exist.
