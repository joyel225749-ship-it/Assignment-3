# Employee App - Backend Integration

A Node.js + Express + MongoDB Atlas backend for the Employee Management application.

## Tech Stack
- **Node.js** + **Express** – REST API server
- **Mongoose** – MongoDB object modelling
- **CORS** – Cross-Origin Resource Sharing
- **MongoDB Atlas** – Cloud database

## Setup & Run

### 1. Install dependencies
```bash
npm install
```

### 2. Configure MongoDB Atlas
Open `app.js` and replace the `mongoURI` value with your own MongoDB Atlas connection string:
```js
const mongoURI = 'mongodb+srv://<username>:<password>@cluster0.mongodb.net/employeeDB?retryWrites=true&w=majority';
```

### 3. Start the server
```bash
npm start
```
The server runs on **http://localhost:3000**

---

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/employeelist` | Get all employees |
| GET | `/api/employeelist/:id` | Get single employee by ID |
| POST | `/api/employeelist` | Add a new employee |
| PUT | `/api/employeelist/:id` | Update an employee by ID |
| DELETE | `/api/employeelist/:id` | Delete an employee by ID |

### Request Body (POST / PUT)
```json
{
  "name": "John Doe",
  "location": "New York",
  "position": "Developer",
  "salary": 60000
}
```
