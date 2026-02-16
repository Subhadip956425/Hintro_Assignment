# TaskOrbit – Real-Time Task Collaboration Platform

**TaskOrbit** is a **real-time task collaboration platform** inspired by tools like **Trello and Notion**.  
It enables teams to collaboratively manage **boards, lists, and tasks** with **live updates**, role-based access, and activity tracking.

This project was built as part of a **Full Stack Engineer Interview Assignment**, focusing on **frontend architecture, backend API design, real-time synchronization, and database modeling**.

---

## 🚀 Features

### Core Functionality
- User authentication (Signup / Login)
- Create and manage **Boards**
- Boards contain multiple **Lists**
- Create, update, delete **Tasks** within lists
- **Drag & drop** tasks across lists
- Assign users to tasks
- **Real-time updates** across multiple users
- Activity history & audit tracking
- Search and pagination support

### Real-Time Capabilities
- Live task updates using **WebSockets**
- Multi-user synchronization without page refresh
- Real-time drag-and-drop reflection across clients

---

## 🧱 Tech Stack

### Frontend
- React (SPA)
- Redux / Context API for state management
- Drag & Drop (React DnD or equivalent)
- WebSocket client for real-time updates

### Backend
- Spring Boot (REST APIs)
- WebSocket (STOMP / Socket-based)
- JWT-based authentication
- Role-based access control

### Databases
- **MySQL** – relational data (users, boards, lists, permissions)
- **MongoDB** – activity logs, history tracking

### Tooling
- Maven
- Node.js + npm
- Git
- Docker-ready structure

---

## 🛠️ Prerequisites

- Java 17+
- Maven
- Node.js (v18+ recommended)
- MySQL
- MongoDB

---

## 📦 Project Structure

```text
taskorbit/
├── backend/
│   ├── controllers
│   ├── services
│   ├── repositories
│   ├── websocket
│   └── security
├── frontend/
│   ├── components
│   ├── redux
│   ├── services
│   └── pages
└── README.md

```

## ⚙️ Setup & Installation

### Backend (Spring Boot)

```bash
# Navigate to the backend directory
cd projectmanagementsystem  # or wherever your Spring Boot project resides

# Build the project
mvn clean install
# or
./mvnw clean install

# Run the application
mvn spring-boot:run
# or
./mvnw spring-boot:run
```

### Frontend (React)

```bash
# Navigate to the frontend directory
cd project-management-react  # or the correct path

# Install dependencies
npm install
# or
yarn install

# Start the development server
npm start
# or
yarn start
```

---

## 🗄️ Database Configuration

### MySQL
- Users
- Boards
- Lists
- Tasks
- Task assignments
- Roles and permissions

### MongoDB
- Activity history
- Audit logs
- Real-time event tracking

---

## 🔌 API Contract (High-Level)

### Authentication
- POST /auth/signup
- POST /auth/login

### Boards
- POST /boards
- GET /boards
- PUT /boards/{boardId}
- DELETE /boards/{boardId}

### Lists
- POST /boards/{boardId}/lists
- GET /boards/{boardId}/lists

### Tasks
- POST /lists/{listId}/tasks
- PUT /tasks/{taskId}
- DELETE /tasks/{taskId}

---

## 🔄 Real-Time Synchronization Strategy

- WebSocket-based communication
- Backend emits task create/update/delete/move events
- Frontend subscribes to board-specific channels
- Instant UI updates without API re-fetch

---

## 🧠 Frontend Architecture

- SPA with React
- Component-based architecture
- Centralized state management
- WebSocket integration
- Optimistic UI updates
- Native form handling

---

## 🧠 Backend Architecture

- Controller → Service → Repository layering
- JWT authentication
- Role-based authorization
- WebSocket gateway
- Global exception handling

---

## 📊 Database Schema (High-Level)

MySQL:
- users
- boards
- lists
- tasks
- task_assignments
- roles
- permissions

MongoDB:
- activity_logs

---

## ⚖️ Assumptions & Trade-offs

- MongoDB used for logs to reduce relational load
- WebSockets preferred over polling
- JWT for stateless auth
- Simplicity over heavy UI animations

---

## 🧪 Testing

- Unit tests for services
- API testing with Postman
- Manual testing for real-time features

---

## 🚀 Deployment Readiness

- Environment-based config
- Docker-compatible
- Frontend: Netlify / Vercel
- Backend: AWS / GCP

---

## Contributing

Contributions are welcome! 🎉  

1. Fork this repo  
2. Create a branch:  
   ```bash
   git checkout -b feature/your-feature
   ```
3. Commit your changes:  
   ```bash
   git commit -m "Add feature"
   ```
4. Push to your branch:  
   ```bash
   git push origin feature/your-feature
   ```
5. Submit a Pull Request  

---

## 🔑 Demo Credentials

Email: demo@taskorbit.com  
Password: Demo@123

---

## License

This project is licensed under the **MIT License**.  
See the [LICENSE](LICENSE) file for details.  

## 👤 Author

**Author:** Subhadip Guchhait  

- GitHub: [Subhadip956425](https://github.com/Subhadip956425)  
- Email: subhadipguchhait106@gmail.com  
