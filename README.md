# TODO Exercise

## Introduction

Your task is to build a simple TODO app using Svelte and a mock backend. You will have two repos for this project, this repo will be for your backend application and a separate one you will create yourself for the frontend application. 

## Frontend

We will use the Divblox Svelte Starter as the base for our application. You can find the public repo and instructions to get it up and running here:

https://github.com/divbloxjs/dx-svelte-starter

Some additional resources I suggest you refer to often:

- https://tailwindcss.com/ (CSS utility framework)
- https://daisyui.com/ (UI component framework built on top of tailwindCSS)
- https://github.com/ItalyPaleAle/svelte-spa-router (Client-side routing)

### Tasks

For this we will give you creative freedom but you must be able to:

- View all the todos
- Edit the `title` and `description` for a todo
- Toggle the todo's `complete` state
- Create a new todo
- Delete an existing todo
- Ensure all changes are persisted

You will persist your data using the [JS Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) to connect to the backend we will create in the next step.

## Backend

For the backend please use this repo. It uses [json-server](https://www.npmjs.com/package/json-server) to give you an easy [RESTful](https://aws.amazon.com/what-is/restful-api/) backend with a mock JSON database based on `db.json`.

### Running the backend

First double check that you have [npm and node installed](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm). Try running this command to confirm:

```
npm -v && node -v
```

Then ensure your command line is in the current directory and install the dependencies using:

```
npm install
```

We can now serve the app by running

```
npm run serve
```

The service should now be up and running and give you an output similar to

```
➜  todo git:(main) ✗ npm run serve

> todo@1.0.0 serve
> json-server --watch db.json


  \{^_^}/ hi!

  Loading db.json
  Done

  Resources
  http://localhost:3000/todos

  Home
  http://localhost:3000

  Type s + enter at any time to create a snapshot of the database
  Watching...
```

You should be able to navigate to http://localhost:3000/todos in a browser and see a list of all the todos in the `db.json` file.

If your port 3000 is already in use and the serve fails with a `EADDRINUSE` error. You can either:

- Change the port or disable the service which is interfering.

- Run json server on a different port by updating the `serve` script in `package.json`

### Postman

Included is a [Postman](https://www.postman.com/) Collection with all the basic requests you'll need for debugging and validation purposes.

Import the `todo.postman_collection.json` file into your Postman installation. If needed, help can be found [here](https://learning.postman.com/docs/getting-started/importing-and-exporting-data/#importing-data-into-postman)
