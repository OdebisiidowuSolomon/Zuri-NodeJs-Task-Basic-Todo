# Mongo CRUD (Node js Solution)

- Task Objective : Setting up of mongo DB connection in a Node.Js server as well as performance of CRUD operations

- Task Description: Create a Node.js server using any framework of choice (optional) and appropriate folder structure (routes, controllers, models, etc.) which will perform the following functions:

> 1. Add a Todo task to a Todo collection
> 2. Update a particular Todo task
> 3. Delete Todo task
> 4. Retrieve all Todo tasks (pagination optional)

 Each Todo document should contain at least the following fields: _id, title, description, timestamp.

> You can use either a local mongoDB instance or a hosted one on any provider of choice.

> Push your code to GitHub and submit your accessible GitHub Link.

## To Run this repo locally

> clone this branch

```bash
git clone https://github.com/kralconomoh/simple_Todolist_api.git
```

> run the following command

```
yarn
```

```
yarn start
```

> after running the yarn start command you should see the following in your terminal / shell

```bash
[nodemon] starting `node index.js`
Mongodb Connected
Server Listening on port 3000
```
<br>
<br>

# Interacting with the endpoints

## To create a todo/task

send a post request to this api endpoint

```bash
    http://localhost:3000/todos/
```

with a request body like this

```bash
    {
        "name": "Go for a walk",
        "description": "Go For a walk with family at the tafawa balewa square",
    }
```

## To fetch a single todo/task

send a get request to this api endpoint

```bash
    http://localhost:3000/todos/todo/6235c4b6eafb61d762520936
```

response payload

```bash
    {
    "_id": "6235c4b6eafb61d762520936",
    "name": "task 2",
    "description": "lorem ipsum soms sjahsgas lehg awehd asssbe jdiifk",
    "createdAt": "2022-03-19T11:55:34.557Z",
    "updatedAt": "2022-03-19T11:55:34.557Z",
    "__v": 0
}
```

## To update a todo/task

send a post request to this api endpoint

```bash
    http://localhost:3000/todos/6235b6911f74e43c9be32cb9
```

with a request body like this.
- Note the id property

```bash
    {
        "name": "Go for a walk",
        "description": "Go For a walk with family at the tafawa balewa square"
    }
```

## To delete a todo/task

send a delete request to this api endpoint

```bash
    http://localhost:3000/todos/6235c4b6eafb61d762520936
```

response payload

```bash
    { message:'task deleted successfully' }
```

## To fetch all open task

send a get request to this api endpoint

```bash
    http://localhost:3000/todos/all
```

response payload

```
   [
    {
        "_id": "6235b6611f74e43c9be32cb7",
        "name": "Go for a walk",
        "description": "Go For a walk with family at the tafawa balewa square",
        "done": false,
        "createdAt": "2022-03-19T10:54:25.099Z",
        "updatedAt": "2022-03-19T10:54:25.099Z",
        "__v": 0
    }
]
```
Thanks for reading, that is all Bye :)
