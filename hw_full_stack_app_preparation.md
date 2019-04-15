# Homework: Full Stack Games Hub App

### Learning Objectives

- Understand the relationship between client, server and database
- Be able to navigate a codebase that you haven't written

## Brief

Your boss has asked to you look over the codebase of a full-stack JavaScript application. The front-end is written in JavaScript using no frameworks, the back-end uses an Express server and a MongoDB database. Your task is to make yourself familiar with the codebase.

The application includes a README.md with instructions on running the application.

![Overview of the tech stack and tooling with commands](images/tech_stack_with_commands.png)

*Overview of the tech stack and tooling with commands*

## MVP

### Task

Draw a diagram showing the dataflow through the application starting with a form submission, ending with the re-rendering of the page. This will involve a multi-direction data-flow with the client posting data to the server and the server sending data back to the client with the response. Detail the client, server and database in the diagram and include the names of the files involved in the process.

### Questions

1. What is responsible for defining the routes of the `games` resource?
 server/helpers/create_router.js

2. What are the the responsibilities of server.js?
  To connect the db to the localhost; creates the Games Collection router; and listens for any requests.

3. What are the responsibilities of the `gamesRouter`?
  Provides routes for all of the views.

4. What process does the the client (front-end) use to communicate with the server?
  RequestHelper.

5. What optional second argument does the `fetch` method take? And what is it used for in this application? Hint: See [Using Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) on the MDN docs
  An init object that allows you to control a number of settings. It's used here to provide instructions for posting a new game that has been submitted as JSON to the url.

6. Which of the games API routes does the front-end application consume (i.e. make requests to)?
  Create, Read and Delete.

7. What are we using the [MongoDB Driver](http://mongodb.github.io/node-mongodb-native/) for?
  To connect the db to the localhost.

## Extension

Why do we need to use [`ObjectId`](https://mongodb.github.io/node-mongodb-native/api-bson-generated/objectid.html) from the MongoDB driver?
