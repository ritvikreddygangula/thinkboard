Thinkboard — MERN Notes Application

Thinkboard is a full-stack MERN application for creating, viewing, and managing notes.
The project focuses on clean architecture, modern React routing, API rate limiting, and a polished UI, closely resembling real-world production patterns.

Overview

Thinkboard allows users to:

Create and manage notes

View notes in a responsive grid layout

Interact with a RESTful backend API

Experience graceful handling of API rate limits

The application is built with a modern MERN stack and integrates Redis-based rate limiting to prevent abuse.

Features

Full CRUD functionality for notes

Responsive UI using Tailwind CSS

Client-side routing with React Router v7 (Data Router API)

Backend API built with Express

MongoDB Atlas for persistent storage

Redis-based rate limiting using Upstash

Clean separation of frontend and backend

Environment-based configuration

Defensive UI rendering to prevent runtime crashes

Tech Stack
Frontend

React (Vite)

React Router v7 (Data Router API)

Tailwind CSS

Axios

Lucide Icons

React Hot Toast

Backend

Node.js

Express.js

MongoDB Atlas

Mongoose

Upstash Redis

dotenv

Project Structure
mern-thinkboard/
├── backend/
│   ├── src/
│   │   ├── config/
│   │   ├── controllers/
│   │   ├── models/
│   │   ├── routes/
│   │   └── server.js
│   └── package.json
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── App.jsx
│   │   └── main.jsx
│   └── package.json
│
└── README.md

Getting Started
Clone the repository
git clone https://github.com/<your-username>/mern-thinkboard.git
cd mern-thinkboard

Backend Setup
cd backend
npm install


Create a .env file in the backend directory:

PORT=5001
MONGO_URI=your_mongodb_connection_string
UPSTASH_REDIS_REST_URL=your_upstash_url
UPSTASH_REDIS_REST_TOKEN=your_upstash_token


Start the backend server:

npm run dev

Frontend Setup
cd ../frontend
npm install
npm run dev


Open the application in your browser:

http://localhost:5173

API Endpoints
Method	Endpoint	Description
GET	/api/notes	Fetch all notes
POST	/api/notes	Create a note
PUT	/api/notes/:id	Update a note
DELETE	/api/notes/:id	Delete a note
Routing Architecture

This project uses React Router v7 with the Data Router API:

createBrowserRouter

RouterProvider

Route loaders for data fetching

Automatic revalidation after mutations

This removes the need for manual useEffect-based data fetching and improves reliability and performance.

Rate Limiting and Caching

Upstash Redis is used to enforce API rate limits

Requests exceeding the limit receive HTTP 429 responses

The frontend handles rate limits gracefully with a dedicated UI state

UI and Design

Utility-first styling with Tailwind CSS

Responsive grid layout

Modern visual effects with layered gradients

Component-driven architecture

Purpose of the Project

Thinkboard was built to:

Practice full-stack MERN development

Learn modern React Router patterns

Integrate Redis-based rate limiting

Build a project close to production standards

Possible Improvements

Authentication and user accounts

Search and filtering for notes

Rich text editor support

Optimistic UI updates

Theme switching (light/dark)

License

This project is licensed under the MIT License.
