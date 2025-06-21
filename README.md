# Mini Express.js REST API

A simple RESTful API built with Node.js and Express.js supporting full CRUD operations with in-memory data storage.

## Features

- Basic Express setup with middleware
- Routes:
  - `GET /items` - Get all items
  - `GET /items/:id` - Get a single item by ID
  - `POST /items` - Create a new item
  - `PUT /items/:id` - Update an existing item
  - `DELETE /items/:id` - Delete an item
- Data validation and error handling
- In-memory data store
- Test-ready with Postman or curl

## Getting Started

```bash
npm install
npm start
```

Visit: `http://localhost:3000`

---

## Example API Requests

### ➕ Create Item

```bash
curl -X POST http://localhost:3000/items \
  -H "Content-Type: application/json" \
  -d '{"name": "Notebook", "description": "A small lined notebook"}'
```

### 📥 Get All Items

```bash
curl http://localhost:3000/items
```

### 📄 Get One Item by ID

```bash
curl http://localhost:3000/items/1
```

### 🔄 Update Item

```bash
curl -X PUT http://localhost:3000/items/1 \
  -H "Content-Type: application/json" \
  -d '{"name": "Updated Notebook", "description": "Now a hardcover version"}'
```

### ❌ Delete Item

```bash
curl -X DELETE http://localhost:3000/items/1
```

---

## Notes

- Use a tool like **Postman** or **curl** to test endpoints.
- This project uses an in-memory array, so data resets on every restart.
