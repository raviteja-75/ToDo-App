# NextGen Tasks - Multi-Page Todo Application

A premium, full-featured multi-page Todo Application built with **React**, **Vite**, **Vanilla CSS** (dark mode / glassmorphism), and **NodeJS / Express**.

---

## Repository Structure

```
├── backend/
│   ├── data/
│   │   └── todos.json      # File database (auto-generated)
│   ├── db.js               # Safe atomic file database utility
│   ├── server.js           # REST API endpoints (CORS enabled)
│   └── package.json        # Backend configuration
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── ListApp.jsx     # Dashboard component
│   │   │   └── DetailApp.jsx   # Single task details component
│   │   ├── styles/
│   │   │   ├── theme.css       # Design variables, typography & layout resets
│   │   │   ├── list.css        # Dashboard styling & grids
│   │   │   └── detail.css      # Detailed view & subtasks checklist
│   │   ├── main-list.jsx       # Entry logic for dashboard
│   │   └── main-detail.jsx     # Entry logic for detail view
│   ├── index.html          # HTML entry for dashboard
│   ├── todo.html           # HTML entry for detail view
│   ├── vite.config.js      # Vite multi-page routing config
│   └── package.json        # Frontend configuration
│
├── README.md               # Quickstart guide
└── features.md             # Functional and architectural specifications
```

---

## Features

- **True Multi-Page Architecture**: Implemented with Vite's native multi-entry point building to serve distinct pages (`index.html` & `todo.html`).
- **Dynamic Stats Dashboard**: Real-time counters and interactive progress bar representing completion percentage, pending tasks, and overdue items.
- **Advanced Filtering**: Filter tasks in real-time by search strings, categories (Work, Personal, Health, Shopping, Other), and priority tags (High, Medium, Low).
- **Interactive Checklist (Subtasks)**: Break down larger tasks into smaller steps inside the task details view with a micro-progress meter.
- **Glassmorphism Dark Theme**: Harmonies of dark indigo backgrounds, smooth transitions, glowing keyframe animations, and custom scrollbars.
- **RESTful API backend**: Fully tested CRUD endpoints with atomic JSON file persistence.

---

## Setup & Running the Application

### Prerequisites
Make sure you have [Node.js](https://nodejs.org) (v18+) and [npm](https://www.npmjs.com/) installed on your machine.

---

### Step 1: Start the Backend Server
1. Navigate to the `backend/` directory:
   ```bash
   cd backend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the dev server (uses `nodemon` for auto-reloading):
   ```bash
   npm run dev
   ```
   The backend will start running at `http://localhost:5000`.

---

### Step 2: Start the Frontend Application
1. Open a new terminal window and navigate to the `frontend/` directory:
   ```bash
   cd frontend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Run the Vite development server:
   ```bash
   npm run dev
   ```
   The application will start running. Vite will display a local address (e.g. `http://localhost:3000`).
4. Click or visit `http://localhost:3000` (or the displayed URL) in your browser to view the application.

---

## Verification and Testing

1. **Creating a task**: Click **"New Task"** on the dashboard, fill in the details, and hit create.
2. **Filtering**: Type in the search box or select category pills to watch the tasks list dynamically update.
3. **Detail Page**: Click on a card. The browser will navigate to `todo.html?id=<id>` where you can add subtasks, edit metadata, or click **"Back to dashboard"** to return home.
