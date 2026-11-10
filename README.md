# PRP - Express + MongoDB Basics

A minimal Express server that shows how to connect Node.js to MongoDB and save a document through a REST endpoint.

## Endpoints

| Method | Route | Description |
| --- | --- | --- |
| GET | `/show` | Health check, returns "Hello world" |
| PUT | `/save` | Saves a student record (`regno`, `name`, `marks`) to MongoDB |

## Project structure

```text
index.js  # Express app and routes (port 4000)
db.js     # MongoDB connection
users.js  # data model
```

## Getting started

```bash
git clone https://github.com/aditijain8/PRP.git
cd PRP
npm install
node index.js
```

Make sure MongoDB is running and the connection string in `db.js` points to it.

## Example request

```bash
curl -X PUT http://localhost:4000/save -H "Content-Type: application/json" -d '{"regno":"101","name":"Aditi","marks":90}'
```

## Author

Aditi Jain - [@aditijain8](https://github.com/aditijain8)
