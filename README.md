# nodejs-hw

A minimal Express application for working with a notes collection. This is a
learning project demonstrating the basics of a web server setup — handling HTTP
requests, middleware, logging, and 404/500 error handling.

## Tech Stack

- Node.js
- Express
- dotenv
- cors
- pino-http

## Installation

```bash
git clone https://github.com/viktoriia-dmytryk/nodejs-hw.git
cd nodejs-hw
git checkout 01-express
npm install
```

## Environment Variables

Create a `.env` file in the root of the project:

```
PORT=3000
```

If the `PORT` variable is not set, the server defaults to port `3000`.

## Running the App

Development (with auto-restart via nodemon):

```bash
npm run dev
```

Production:

```bash
npm start
```

## API Routes

### GET /notes

Returns all notes.

**Response: 200 OK**

```json
{
  "message": "Retrieved all notes"
}
```

### GET /notes/:noteId

Returns a note by its ID.

**Response: 200 OK**

```json
{
  "message": "Retrieved note with ID: id_param"
}
```

### GET /test-error

A test route for checking error handling. Intentionally throws an error.

**Response: 500 Internal Server Error**

```json
{
  "message": "Simulated server error"
}
```

### Non-existent routes

Any request to a route not listed above returns:

**Response: 404 Not Found**

```json
{
  "message": "Route not found"
}
```

## Deployment

The project is deployed on [Render](https://render.com):

🔗 **Deployed app:** `<>`

🔗 **Source code:**
`https://github.com/viktoriia-dmytryk/nodejs-hw/tree/01-express`
