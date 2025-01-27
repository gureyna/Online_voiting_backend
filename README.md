# Online Voting System Backend

A secure and scalable backend for an online voting system built with Node.js, Express, and MongoDB.

## Features

- User Authentication with JWT
- Role-based Authorization (Admin/User)
- Secure Password Hashing
- CRUD Operations for Users and Votes
- MongoDB Integration with Mongoose
- Input Validation
- Error Handling
- API Rate Limiting
- Security Headers with Helmet

## Prerequisites

- Node.js (v14 or higher)
- MongoDB (v4 or higher)
- npm or yarn

## Installation

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a `.env` file in the root directory with the following variables:
   ```
   PORT=5000
   MONGODB_URI=mongodb://localhost:27017/voting-system
   JWT_SECRET=your_jwt_secret_key_here
   NODE_ENV=development
   ```
4. Start the server:
   ```bash
   # Development mode
   npm run dev
   
   # Production mode
   npm start
   ```

## API Endpoints

### Authentication
- POST /api/auth/register - Register a new user
- POST /api/auth/login - Login user

### Users
- GET /api/users/profile - Get user profile
- PUT /api/users/profile - Update user profile
- GET /api/users - Get all users (Admin only)
- DELETE /api/users/:id - Delete user (Admin only)

### Votes
- POST /api/votes - Cast a vote
- GET /api/votes - Get all votes (Admin only)
- GET /api/votes/election/:electionId - Get votes by election
- GET /api/votes/my-votes - Get user's vote history

## Security Features

- JWT for authentication
- Password hashing with bcrypt
- Input validation and sanitization
- Role-based access control
- Security headers with Helmet
- CORS protection
- Rate limiting

## Error Handling

The API includes comprehensive error handling for:
- Invalid requests
- Authentication errors
- Authorization errors
- Database errors
- Validation errors

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request
