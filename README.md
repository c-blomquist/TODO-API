# TODO-api  

For the second phase of the project, the developer should create a RESTful API in front of the database. The CLI connected directly to the database, which in general is considered to be dangerous. **After creating a RESTful API,  the CLI should be migrated to make HTTP calls to the API instead of connecting to the database correctly.**

The following routes will be required:

```bash
# fetch a list of task objects
GET /tasks

# create a new task with the provided ID
POST /tasks

# update a task with the provided ID
PATCH /tasks/:taskId
```

The `GET` route should return an array of task objects from the database. The `POST` route will be responsible for creating a new task. The API should accept a request body  containing the name of the task. As before, the `createdDate` and `completed` properties should be set automatically by the API.

The `PATCH` route will be responsible for updating a task. Specifically, it will be used to change a task’s completed status to complete.
