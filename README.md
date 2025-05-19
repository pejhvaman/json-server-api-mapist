# 📦 json-server-api-mapist

Mock REST API using `json-server` for development and testing purposes.
Deployed on [Railway](https://railway.app/) for public use.

---

## 🚀 Live API

👉 **Base URL**:
`https://json-server-api-mapist-production.up.railway.app`

> Example endpoint:
> `GET /cities` → `https://json-server-api-mapist-production.up.railway.app/cities`

---

## 📁 Project Structure

```bash
.
├── db.json               # Mock database
├── package.json          # Project metadata and start script
```

---

## 📦 Installation (Local)

1. Clone the repo:

   ```bash
   git clone https://github.com/your-username/json-server-api-mapist.git
   cd json-server-api-mapist
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Start server locally:

   ```bash
   npm start
   ```

---

## 📄 API Endpoints

Assuming the base URL is `/`, available endpoints (based on your `db.json`) include:

- `GET /cities` – List all cities
- `GET /cities/:id` – Get a city by ID
- `POST /cities` – Add a new city
- `PUT /cities/:id` – Update a city
- `DELETE /cities/:id` – Delete a city

You can modify the `db.json` to create other resources (like `users`, `posts`, etc.).

---

## ☁️ Deployment Guide (Railway)

### 1. Setup Project

```bash
npm init -y
npm install json-server
```

### 2. Add `db.json` File

```json
{
  "cities": [
    { "id": 1, "name": "Tehran", "country": "Iran" },
    { "id": 2, "name": "Shiraz", "country": "Iran" }
  ]
}
```

### 3. Update `package.json`

```json
"scripts": {
  "start": "json-server --watch db.json"
}
```

### 4. Push to GitHub

```bash
git init
git remote add origin https://github.com/your-username/json-server-api-mapist.git
git add .
git commit -m "Initial commit"
git push -u origin main
```

### 5. Deploy to Railway

- Go to [Railway](https://railway.app/)
- Click **New Project** → **Deploy from GitHub repo**
- Select your repo
- Use `npm start` as the Start Command
- From Settings > Networking, click **"Generate Public Domain"**

---

## 🧪 Example Usage in Code

```js
fetch("https://json-server-api-mapist-production.up.railway.app/cities")
  .then((res) => res.json())
  .then((data) => console.log(data))
  .catch((err) => console.error("Error:", err));
```

---

## 🧰 Tech Stack

- [Node.js](https://nodejs.org/)
- [json-server](https://github.com/typicode/json-server)
- [Railway](https://railway.app/) – Hosting
