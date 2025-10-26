# ProBackend - Video Platform Backend

A robust Node.js backend application built for a video-sharing platform, featuring user authentication, video management, and cloud storage capabilities. This project serves as the API server for handling user operations and video content.

## Features

- **User Management**: Complete user authentication system with JWT tokens for access and refresh.
- **Video Operations**: Support for uploading, storing, and managing video content with Cloudinary integration.
- **Security**: Password hashing with bcrypt, secure token generation, and middleware for request handling.
- **Database**: MongoDB integration with Mongoose ODM for data modeling and pagination support.
- **File Handling**: Multer for multipart file uploads and Cloudinary for cloud storage.
- **Error Handling**: Custom API error and response classes for consistent error management.
- **Development**: Enabled with nodemon for hot reloads and Prettier for code formatting.

## Technology Stack

- **Runtime**: Node.js with ES6 modules
- **Framework**: Express.js for API routing
- **Database**: MongoDB with Mongoose
- **Authentication**: JWT for token-based auth
- **File Storage**: Cloudinary for media storage
- **Middleware**: CORS, cookie parsing, body parsing
- **Development Tools**: Nodemon for development, Prettier for code formatting

## Data Models

### User

- Username, email, fullname
- Avatar and cover image support
- Watch history tracking
- Secure password storage with bcrypt
- JWT token generation methods

### Video

- Video file and thumbnail uploads
- Title, description, duration
- View count and publish status
- User ownership with references
- Aggregation plugin for advanced queries

## Project Structure

```
project-root/
├── .env.sample
├── .gitignore
├── .prettierignore
├── .prettierrc
├── package-lock.json
├── package.json
├── Readme.md
├── public/
└── src/
    ├── app.js              # Express app setup with middleware
    ├── constants.js        # Application constants (DB name)
    ├── index.js            # App entry point and server startup
    ├── controllers/        # Route controllers (coming soon)
    ├── db/
    │   └── index.js        # MongoDB connection utility
    ├── middlewares/        # Custom middleware (coming soon)
    ├── models/
    │   ├── user.model.js   # User Mongoose schema
    │   └── video.model.js  # Video Mongoose schema
    ├── routes/             # API routes (coming soon)
    └── utils/              # Utility functions
        ├── apiError.js     # Custom error class
        ├── apiResponse.js  # Standardized response class
        ├── asyncHandler.js # Async error wrapper
        └── cloudinary.js   # Cloud storage configuration
```

## Setup Instructions

1. Clone the repository:

   ```bash
   git clone https://github.com/mayankjain92/probackend.git
   cd probackend
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Create environment file from sample:

   ```bash
   cp .env.sample .env
   ```

4. Configure your environment variables (MongoDB URI, JWT secrets, Cloudinary credentials)

5. Start the development server:
   ```bash
   npm run dev
   ```

## Scripts

- `npm run dev`: Start the server with nodemon in development mode

## Author

Made by Mayank Jain as part of ChaiAurCode tutorials
