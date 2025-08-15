```markdown
# My Fullstack Project

## 📌 Overview
This repository contains a **fullstack web application** with a separate **frontend** and **backend**.  
It is designed for a **team of 4 developers** (1 owner + 3 collaborators) working in a collaborative, review-driven workflow.  
We follow **GitHub best practices** to ensure code quality, prevent accidental overwrites, and maintain a clean commit history.

The goal is to build a **simple but scalable web application** where the frontend communicates with a secure backend API.

---

## 🗂 Repository Structure
```

team-test/
│
├── frontend/                # Frontend code (HTML, CSS, JS or React/Vue)
│   ├── index.html
│   ├── style.css
│   └── script.js
│
├── backend/                 # Backend code (Node.js/Express)
│   ├── server.js
│   ├── routes/
│   │   └── sample-route.js
│   ├── controllers/
│   ├── models/
│   └── config/
│
├── .env.example              # Example environment variables file
├── .gitignore                # Node-specific ignore file
├── README.md                 # Project documentation
└── LICENSE                   # License file

````

---

## 🌿 Branching Strategy

We use **three types of branches** for better workflow and control:

### **1️⃣ main** (Production Branch)
- Contains **production-ready** code only.
- **Protected**: requires PR reviews (minimum 2 approvals) before merging.
- No direct pushes allowed.
- Only merges from `dev` after thorough testing.

### **2️⃣ dev** (Integration Branch)
- Receives code from feature branches after review and testing.
- Requires **1 approval** before merging.
- Used for integration testing before moving to `main`.

### **3️⃣ feature/xxx** (Feature Branches)
- For individual features or bug fixes.
- Branch name format: `feature/<short-description>` (e.g., `feature/user-auth`).
- Created from `dev` and merged back into `dev` after review.
- Direct pushes allowed (no PR required until merging to `dev`).

---

## 🛠 Project Requirements

We aim to build a **frontend + backend** system with the following:

### **Backend (Node.js + Express)**
- RESTful API endpoints:
  - User authentication (register/login)
  - Basic CRUD operations (Create, Read, Update, Delete)
- MongoDB (or MySQL/PostgreSQL) for data storage
- `.env` file for environment variables (API keys, DB credentials)
- Security middleware (Helmet, CORS, etc.)
- Error handling and logging

### **Frontend (HTML/CSS/JS or React)**
- Pages/components:
  - Home / Landing page
  - Login / Register forms
  - Dashboard to display data from the backend
- Fetch API to communicate with backend routes
- Responsive design for mobile & desktop

---

## 🔄 Workflow for Collaborators

1. **Create a feature branch from `dev`**:
   ```bash
   git checkout dev
   git pull origin dev
   git checkout -b feature/my-feature
````

2. **Work locally, commit, and push**:

   ```bash
   git add .
   git commit -m "Add my feature"
   git push origin feature/my-feature
   ```

3. **Open a Pull Request (PR)**:

   * Target branch: `dev`
   * Request at least 1 reviewer
   * Resolve all review comments before merging

4. **Merge to `main`**:

   * Only after `dev` is tested and stable
   * Requires **2 approvals** before merging

---

## 🛡 Branch Protection Rules Summary

| Branch       | Rules                                                                                             |
| ------------ | ------------------------------------------------------------------------------------------------- |
| **main**     | Require PR (2 approvals), Restrict deletions, Block force pushes, Require conversation resolution |
| **dev**      | Require PR (1 approval), Restrict deletions, Block force pushes, Require conversation resolution  |
                                                                       |

---

## ⚙️ Environment Setup

**Install dependencies**:

```bash
cd backend
npm install

cd ../frontend
# If using a frontend framework like React/Vue:
npm install
```

**Run backend locally**:

```bash
cd backend
npm run dev
```

**Run frontend locally**:

```bash
cd frontend
npm start
```

---

## 📄 .gitignore

This project uses the **Node.js .gitignore** template to exclude:

* `node_modules/`
* `.env`
* Logs
* IDE/project files

---

## 🔐 Environment Variables

We do **not** commit `.env` files.
Instead, we use `.env.example` for safe sharing of variable names:

```env
DB_HOST=localhost
DB_USER=root
DB_PASS=password
DB_NAME=my_database
API_KEY=your_api_key_here
```

---

## 👥 Contributors

* **\[Your Name]** (Owner)
* Collaborator 1
* Collaborator 2
* Collaborator 3

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
