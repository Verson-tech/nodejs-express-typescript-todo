## Node.js Express TypeScript ToDo Application Models

## `ToDo` application frameworks, libraries, languages and database:

`ExpressJS` - creates a REST API

`Node.js` is used as the runtime environment

`TypeScript` programming language

`MongoDB` can be used as the database.

## Tools and technologies used:

`Postman` - REST API testing

## Middleware:

`body-parser` - parses incoming request bodies as a Buffer and only looks at requests where the Content-Type header matches the type option

For example, in

## /src/models/todo.ts

`export class Todo {`

`constructor(public id: string, public text: string) {`

`}`

`}`

and

## /src/controllers/todos.ts`:

`import { RequestHandler } from "express";`

`import { Todo } from "../models/todo";`

`const TODOS: Todo[] = [];`

`export const createTodo: RequestHandler = (req, res, next`

`=> {`

`const text = (req.body as { text: string }).text;`

`const newTodo = new Todo(Math.random().toString(), text);`

`TODOS.push(newTodo);`

`res.status(201).json({ message: "Created the todo.",`

` createdTodo: newTodo });`

`};`

![Image](/src/imgs/Screenshot%202023-12-11%20at%202.05.37%20PM.png)
