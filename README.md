# MentorFlow — Frontend

Single-file web client (`index.html`). No build step required.

## Run locally
Just open `index.html` in a browser, or serve it:
```bash
npx serve .
```
When the hostname is `localhost`, it calls the API at `http://localhost:5000/api`.

## Connect to your deployed backend
In `index.html` (around line 315), set your Render backend URL:
```js
const API = window.location.hostname === "localhost"
  ? "http://localhost:5000/api"
  : "https://YOUR-BACKEND-NAME.onrender.com/api"; // ← UPDATE THIS
```

## Deploy to Netlify (free)
- **Drag & drop:** app.netlify.com → drop this folder → done, or
- **From GitHub:** New site → pick this repo → publish directory `.`

After deploy, copy your Netlify URL into the backend's `FRONTEND_URL` env var (for CORS).
