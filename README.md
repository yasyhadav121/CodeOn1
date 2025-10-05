# CodeFunda 

A full-stack LeetCode clone application with code execution, user authentication, and cloud storage capabilities.

## 🚀 Features

- **User Authentication** - JWT-based secure authentication
- **Code Execution** - Real-time code compilation using Judge0 API
- **Problem Database** - MongoDB-based problem storage
- **Redis Caching** - Fast data retrieval with Redis Cloud
- **File Storage** - Cloudinary integration for media uploads
- **AI Integration** - Google Gemini API for code assistance

## 📋 Prerequisites

Before running this project, make sure you have:

- Node.js (v14 or higher)
- MongoDB Atlas account
- Redis Cloud account
- Cloudinary account
- Judge0 RapidAPI subscription
- Google AI API key

## 🔧 Installation

1. **Clone the repository**
```bash
git clone <your-repo-url>
cd codefunda
```

2. **Install dependencies**
```bash
npm install
```

3. **Environment Setup**

Create a `.env` file in the root directory and add the following variables:

```env
# Server Configuration
PORT=3000

# Database
DB_CONNECT_STRING=mongodb+srv://<username>:<password>@codefunda.olmw8vb.mongodb.net/leetcode

# Authentication
JWT_KEY=your_jwt_secret_key

# Redis Cache
REDIS_HOST=redis-11532.c99.us-east-1-4.ec2.redns.redis-cloud.com
REDIS_PORT=11532
REDIS_USERNAME=default
REDIS_PASSWORD=your_redis_password

# Judge0 Code Execution API
JUDGE0_KEY=your_judge0_rapidapi_key

# Google Gemini AI
GOOGLE_API_KEY=your_google_api_key

# Cloudinary Storage
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
CLOUDINARY_URL=cloudinary://api_key:api_secret@cloud_name
```

## 🔐 Getting API Keys

### MongoDB Atlas
1. Go to [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
2. Create a cluster and get your connection string
3. Replace `<username>` and `<password>` with your credentials

### Redis Cloud
1. Sign up at [Redis Cloud](https://redis.com/try-free/)
2. Create a database and get your connection details

### Judge0 API
1. Subscribe to Judge0 on [RapidAPI](https://rapidapi.com/judge0-official/api/judge0-ce)
2. Get your API key from the dashboard

### Google AI (Gemini)
1. Visit [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Generate your API key

### Cloudinary
1. Sign up at [Cloudinary](https://cloudinary.com/)
2. Get your credentials from the dashboard

## 🏃‍♂️ Running the Application

### Development Mode
```bash
npm run dev
```

### Production Mode
```bash
npm start
```

The server will start on `http://localhost:3000`

## 📁 Project Structure

```
codefunda/
├── models/          # Database models
├── routes/          # API routes
├── controllers/     # Business logic
├── middleware/      # Authentication & validation
├── utils/           # Helper functions
├── config/          # Configuration files
├── .env             # Environment variables
├── server.js        # Main application file
└── README.md        # Project documentation
```

## 🔒 Security Notes

- **Never commit `.env` file** to version control
- Add `.env` to your `.gitignore` file
- Rotate your API keys regularly
- Use environment-specific configurations for production

## 📝 Environment Variables Guide

| Variable | Description | Required |
|----------|-------------|----------|
| PORT | Server port number | Yes |
| DB_CONNECT_STRING | MongoDB connection URI | Yes |
| JWT_KEY | Secret key for JWT tokens | Yes |
| REDIS_HOST | Redis server hostname | Yes |
| REDIS_PORT | Redis server port | Yes |
| REDIS_PASSWORD | Redis authentication password | Yes |
| JUDGE0_KEY | Judge0 API key from RapidAPI | Yes |
| GOOGLE_API_KEY | Google Gemini AI API key | Yes |
| CLOUDINARY_* | Cloudinary credentials | Yes |

## 🛠️ Technologies Used

- **Backend**: Node.js, Express.js
- **Database**: MongoDB, Redis
- **Authentication**: JWT (JSON Web Tokens)
- **Code Execution**: Judge0 API
- **AI Integration**: Google Gemini API
- **Storage**: Cloudinary
- **Caching**: Redis Cloud

## 📞 Support

For issues or questions, please create an issue in the repository.

## 📄 License

This project is licensed under the MIT License.

---

**⚠️ Important**: Replace all placeholder values in `.env` file with your actual credentials before running the application.
