# CodeDepot - MERN GitHub Profile Explorer 🚀

CodeDepot is a full-stack MERN application that enables users to search for GitHub profiles, view their repositories, like profiles, and explore popular repositories. It integrates GitHub OAuth for authentication, ensuring a secure and seamless user experience.

---

## Features ✨

- **GitHub OAuth Authentication**: Secure login using GitHub.
- **Profile Search**: Fetch and display GitHub user profiles with their repositories.
- **Profile Likes**: Like GitHub profiles and view your liked profiles.
- **Popular Repositories**: Explore repositories by programming languages.
- **Frontend-Backend Integration**: Fully functional React frontend served from the Express backend.

---

## Tech Stack 🛠️

### **Frontend**
- **React**: Component-based UI development.
- **React Router DOM**: Client-side routing.
- **React Hot Toast**: User notifications.
- **Tailwind CSS**: Modern utility-first CSS framework.

### **Backend**
- **Node.js**: JavaScript runtime for the backend.
- **Express.js**: Lightweight backend framework.
- **Passport.js**: GitHub OAuth integration.
- **MongoDB**: Database for storing user interactions.

---

## Installation and Setup ⚙️

### Prerequisites

- Node.js (latest stable version)
- MongoDB (Atlas or local instance)
- GitHub Developer Account for OAuth credentials

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/CodeDepot.git
cd CodeDepot
```

### 2. Backend Setup

Navigate to the backend directory:

```bash
cd backend
```

Install dependencies:

```bash
npm install
```

Create a `.env` file in the backend directory:

```plaintext
PORT=5000
MONGO_URI=your_mongo_uri
GITHUB_CLIENT_ID=your_github_client_id
GITHUB_CLIENT_SECRET=your_github_client_secret
CLIENT_BASE_URL=http://localhost:5173
```

Start the backend server:

```bash
npm run dev
```

### 3. Frontend Setup

Navigate to the frontend directory:

```bash
cd frontend
```

Install dependencies:

```bash
npm install
```

Start the React development server:

```bash
npm run dev
```

---

## API Endpoints 📡

### Authentication (`auth.route.js`)

| Method | Endpoint                  | Description                        |
|--------|---------------------------|------------------------------------|
| GET    | `/api/auth/github`        | Initiates GitHub OAuth login.      |
| GET    | `/api/auth/github/callback` | Handles OAuth callback.            |
| GET    | `/api/auth/check`         | Checks the user's authentication status. |
| GET    | `/api/auth/logout`        | Logs out the user.                 |

### User Profiles (`user.route.js`)

| Method | Endpoint                        | Description                              |
|--------|---------------------------------|------------------------------------------|
| GET    | `/api/users/profile/:username`  | Fetch GitHub profile and repositories.   |
| GET    | `/api/users/likes`              | Retrieve liked profiles (auth required). |
| POST   | `/api/users/like/:username`     | Like a GitHub profile (auth required).   |

### Explore Repositories (`explore.route.js`)

| Method | Endpoint                        | Description                              |
|--------|---------------------------------|------------------------------------------|
| GET    | `/api/explore/repos/:language`  | Fetch popular repos by language (auth required). |

---

## Scripts 📜

### Backend

- `npm run dev`: Start the backend server in development mode.
- `npm start`: Start the backend server in production mode.

### Frontend

- `npm run dev`: Start the React development server.
- `npm run build`: Build the React app for production.
- `npm run preview`: Preview the production build.

---

## Deployment 🚀

### Production Build

Build the frontend:

```bash
cd frontend
npm run build
```

Serve the built frontend using the backend:

Ensure the `express.static` middleware is correctly configured in `server.js`:

```javascript
app.use(express.static(path.join(__dirname, "/frontend/dist")));
```

Run the backend server:

```bash
npm start
```

---

## Contributing 🤝

1. Fork the repository.
2. Create a new branch:

```bash
git checkout -b feature/your-feature-name
```

3. Commit your changes:

```bash
git commit -m "Add your message here"
```

4. Push the branch:

```bash
git push origin feature/your-feature-name
```

5. Open a pull request.

---

## Contact 📧

For queries or feedback:

- **Author**: Brijesh Poojary
- **Portfolio**: [brijesh.xyz](https://brijesh.xyz)
- **Email**: brijeshpujari333@gmail.com

---
