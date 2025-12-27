# Karaama Production Backend API

Express.js and MongoDB backend for the Karaama Production website.

## Features

- RESTful API for contact form submissions
- MongoDB database integration
- CORS enabled for frontend communication
- Error handling and validation
- Health check endpoint

## Setup

1. Install dependencies:
```bash
npm install
```

2. Create `.env` file (or use the provided one):
```env
PORT=5000
MONGO_URL=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
NODE_ENV=production
```

3. Start the server:
```bash
npm start
# or
npm run dev
```

The server will run on `http://localhost:5000`

## API Endpoints

### Contact Form
- `POST /api/contact` - Submit contact form
  - Body: `{ name, email, subject, message }`
  - Returns: `{ success, message, data }`

- `GET /api/contact` - Get all contact submissions

### Health Check
- `GET /api/health` - Server health check

## Project Structure

```
backend/
├── index.js              # Server entry point
├── models/
│   └── Contact.js       # Contact model
├── routes/
│   └── contactRoutes.js # Contact routes
├── .env                 # Environment variables
└── package.json
```

