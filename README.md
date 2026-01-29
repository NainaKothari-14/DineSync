# DineSync — Restaurant Reservation System

A modern, full-stack restaurant reservation platform built with the MERN stack (MongoDB, Express.js, React, Node.js). DineSync streamlines the table booking process with an intuitive interface and robust backend architecture.

## Overview

DineSync provides a complete solution for restaurant table reservations, featuring real-time availability checking, booking management, and a responsive user interface. The application handles the entire reservation workflow from browsing available time slots to confirmation and management.

### Core Features

**User Functionality**
- Browse restaurant information and available time slots
- Select reservation date, time, and party size
- Submit bookings with contact information
- Real-time form validation and error handling
- Booking confirmation and management

**Technical Capabilities**
- RESTful API architecture
- Persistent data storage with MongoDB
- Token-based authentication (if implemented)
- Responsive design for mobile and desktop
- Environment-based configuration

---

## Technology Stack

**Frontend**
- React 18+ with Hooks
- React Router for navigation
- Axios for HTTP requests
- CSS3/Styled Components

**Backend**
- Node.js runtime
- Express.js framework
- MongoDB with Mongoose ODM
- JWT authentication (optional)

**Development Tools**
- Postman for API testing
- Git version control
- ESLint & Prettier

**Deployment**
- Vercel (Frontend)
- Render/Railway (Backend)
- MongoDB Atlas (Database)

---

## Prerequisites

Ensure you have the following installed:

- **Node.js** (v16.x or higher)
- **npm** or **yarn**
- **MongoDB** (Atlas account or local instance)
- **Git**

---

## Installation & Setup

### 1. Clone Repository

```bash
git clone https://github.com/your-username/dinesync.git
cd dinesync
```

### 2. Backend Setup

```bash
cd backend
npm install
```

Create a `.env` file in the `backend` directory:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
FRONTEND_URL=http://localhost:3000
NODE_ENV=development
```

### 3. Frontend Setup

```bash
cd frontend
npm install
```

Create a `.env` file in the `frontend` directory:

```env
REACT_APP_API_URL=http://localhost:5000
```

### 4. Running the Application

**Start Backend Server**
```bash
cd backend
npm run dev
```
Server runs at `http://localhost:5000`

**Start Frontend Application**
```bash
cd frontend
npm start
```
Application opens at `http://localhost:3000`

---

## API Documentation

### Reservation Endpoints

| Method | Endpoint | Description | Auth Required |
|--------|----------|-------------|---------------|
| POST | `/api/reservations` | Create new reservation | No |
| GET | `/api/reservations` | Retrieve all reservations | Yes |
| GET | `/api/reservations/:id` | Get reservation by ID | Yes |
| PATCH | `/api/reservations/:id` | Update reservation | Yes |
| DELETE | `/api/reservations/:id` | Cancel reservation | Yes |

### Request/Response Examples

**Create Reservation (POST /api/reservations)**

Request Body:
```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "phone": "+1234567890",
  "date": "2024-02-15",
  "time": "19:00",
  "partySize": 4,
  "specialRequests": "Window seat preferred"
}
```

Response:
```json
{
  "success": true,
  "data": {
    "_id": "65abc123...",
    "name": "John Doe",
    "confirmationCode": "RES-2024-001"
  }
}
```

---

## Application Workflow

1. **User Interface** — Customer selects reservation parameters (date, time, party size)
2. **Validation** — Frontend validates input and checks availability
3. **API Request** — Booking data sent to backend via REST API
4. **Database Operation** — MongoDB stores reservation with timestamp
5. **Confirmation** — User receives booking confirmation with unique ID
6. **Management** — Users can view, modify, or cancel bookings

---

## Deployment Guide

### Frontend Deployment (Vercel)

1. Push code to GitHub repository
2. Connect repository to Vercel
3. Configure build settings:
   - **Build Command:** `npm run build`
   - **Output Directory:** `build`
4. Add environment variables in Vercel dashboard
5. Deploy

### Backend Deployment (Render/Railway)

1. Create new web service
2. Connect GitHub repository
3. Configure environment variables:
   - `MONGO_URI`
   - `FRONTEND_URL`
   - `NODE_ENV=production`
4. Set build and start commands
5. Deploy service

### Database Setup (MongoDB Atlas)

1. Create cluster on MongoDB Atlas
2. Configure network access (whitelist IP)
3. Create database user
4. Copy connection string to `MONGO_URI`

---

## Development

### Available Scripts

**Backend**
```bash
npm run dev      # Start development server with nodemon
npm start        # Start production server
npm test         # Run test suite
```

**Frontend**
```bash
npm start        # Start development server
npm run build    # Create production build
npm test         # Run tests
```

### Code Quality

The project follows industry best practices:
- ESLint for code linting
- Prettier for code formatting
- Conventional commits
- Component-based architecture

---

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

Please ensure your code follows the existing style and includes appropriate tests.

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## Contact & Support

**Developer:** Naina Kothari  
**Email:**nainavasai@gmail.com  
**GitHub:** [@NainaKothari-14](https://github.com/NainaKothari-14)  

For bug reports and feature requests, please open an issue on GitHub.

---

## Acknowledgments

- Built with the MERN stack ♥
- Inspired by modern restaurant booking systems
