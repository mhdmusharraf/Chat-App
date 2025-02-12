# Chatty - Real-time Chat Application

Chatty is a real-time chat application built with modern web technologies. It allows users to communicate instantly with each other using WebSockets and stores user details and messages in a MongoDB database.

## Tech Stack

### Frontend

- **Vite** - Fast and optimized frontend development
- **React** - UI framework for building components
- **Tailwind CSS** - Utility-first CSS framework for styling
- **DaisyUI** - Component library for Tailwind CSS
- **Zustand** - State management for React

### Backend

- **Node.js** - Server-side runtime
- **Express.js** - Web framework for Node.js
- **MongoDB** - Database for storing user details and messages
- **Mongoose** - ODM for MongoDB
- **Socket.io** - Real-time bidirectional event-based communication

## Features

- 🔒 **User Authentication** - Secure login and registration system
- 💬 **Real-time Messaging** - Instant chat powered by Socket.io
- 🏆 **User Presence** - See who is online
- 📜 **Chat History** - Messages are stored in MongoDB
- 🎨 **Modern UI** - Responsive and visually appealing design using Tailwind CSS & DaisyUI

## Installation & Setup

### Prerequisites

Make sure you have the following installed on your machine:

- Node.js (v14+ recommended)
- MongoDB (local or cloud instance)

### Clone the Repository

```sh
git clone https://github.com/mhdmusharraf/Chat-App.git
cd chat-app
```

### Backend Setup

1. Navigate to the backend directory:
   ```sh
   cd backend
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Create a `.env` file and configure the following environment variables:
   ```env
   PORT=5000
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_secret_key
   ```
4. Start the backend server:
   ```sh
   npm run dev
   ```

### Frontend Setup

1. Navigate to the frontend directory:
   ```sh
   cd frontend
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Start the frontend server:
   ```sh
   npm run dev
   ```

### Running the Application

Once both the frontend and backend servers are running, open your browser and navigate to:

```
http://localhost:5173
```

## Folder Structure

```
chatty/
├── backend/
│   ├── models/       # Mongoose models (User, Message)
│   ├── routes/       # API routes
│   ├── controllers/  # Controllers for handling requests
│   ├── config/       # Database configuration
│   ├── server.js     # Express server
│   ├── socket.js     # Socket.io logic
│   ├── .env          # Environment variables
│   ├── package.json  # Backend dependencies
│
├── frontend/
│   ├── src/
│   │   ├── components/  # React components
│   │   ├── pages/       # Pages (Login, Chat)
│   │   ├── store/       # Zustand state management
│   │   ├── App.jsx      # Main React app
│   ├── package.json     # Frontend dependencies
│
├── README.md            # Documentation
```

## API Endpoints

| Method | Endpoint                | Description         |
| ------ | ----------------------- | ------------------- |
| POST   | `/api/auth/register`    | Register a new user |
| POST   | `/api/auth/login`       | Login user          |
| GET    | `/api/messages/:chatId` | Get chat messages   |
| POST   | `/api/messages/send`    | Send a new message  |

## WebSocket Events

| Event Name    | Description                  |
| ------------- | ---------------------------- |
| `message`     | Send/receive messages        |
| `user-online` | Notify when a user is online |
| `user-typing` | Show typing indicator        |

## Contributing

Contributions are welcome! If you want to contribute:

1. Fork the repository
2. Create a new branch (`feature-xyz`)
3. Commit your changes
4. Push and create a pull request

## License

This project is licensed under the MIT License.

---

Happy Coding! 🚀
