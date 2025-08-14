# Insights API Postman Collection

This repository contains a Postman collection and environment configuration for testing and interacting with the Polestar Insights API.

## 📋 Overview

The Insights API provides access to Polestar's analytics and insights platform. This Postman collection includes pre-configured requests for authentication, data retrieval, and various API endpoints.

**API Documentation**: [Polestar API Documentation](https://developers.polestarglobal.com/docs/polestar-api/cf89bb09c7puy-introduction-to-pole-star-ap-is)

## 📁 Files

- `Insights API's.postman_collection.json` - Main Postman collection with all API requests
- `One Platform (PRODUCTION).postman_environment.json` - Production environment configuration

## 🚀 Getting Started

### Prerequisites

- [Postman](https://www.postman.com/downloads/) installed on your machine
- Valid Polestar API credentials (username, password, account_id)

### Setup Instructions

1. **Import the Collection**
   - Open Postman
   - Click "Import" in the top left
   - Select `Insights API's.postman_collection.json`

2. **Import the Environment**
   - In Postman, go to Environments
   - Click "Import"
   - Select `One Platform (PRODUCTION).postman_environment.json`

3. **Configure Environment Variables**
   - Select the "One Platform (PRODUCTION)" environment
   - Update the following secret variables with your credentials:
     - `username`: Your Polestar username
     - `password`: Your Polestar password
     - `account_id`: Your account ID
     - `user_email`: Your user email

4. **Set Active Environment**
   - Make sure "One Platform (PRODUCTION)" is selected as your active environment

## 🔐 Authentication

The collection includes automated authentication handling:

- **Signin Request**: Authenticates with the API and automatically extracts:
  - Access Token
  - Refresh Token
  - Account ID
  - User ID
  - Session ID (if available)

These tokens are automatically stored in environment variables for use in subsequent requests.

## 🌐 Environment Configuration

### Production Environment
- **Base URL**: `https://api.polestar-production.com`
- **Environment**: One Platform (PRODUCTION)

### Required Variables
- `server_url`: API base URL
- `username`: Your username (secret)
- `password`: Your password (secret)
- `account_id`: Your account ID (secret)
- `user_email`: Your email address (secret)

## 📝 Usage

1. **Start with Authentication**
   - Run the "Signin" request first to authenticate and set up tokens
   - Verify that the tests pass and tokens are extracted

2. **Use Other Endpoints**
   - All other requests will automatically use the authentication tokens
   - Tokens are refreshed automatically when needed

## 🧪 Testing

The collection includes automated tests for:
- Status code validation
- Token extraction and storage
- Response data validation

## 🔧 Troubleshooting

### Common Issues

1. **401 Unauthorized**
   - Verify your credentials in the environment variables
   - Run the Signin request to refresh your tokens

2. **Environment Variables Not Set**
   - Ensure you've selected the correct environment
   - Check that all required secret variables are configured

3. **Token Expiration**
   - Re-run the Signin request to get fresh tokens
   - Check if your account has the necessary permissions

## 📞 Support

For API-related questions and support:
- Review the [official API documentation](https://developers.polestarglobal.com/docs/polestar-api/cf89bb09c7puy-introduction-to-pole-star-ap-is)
- Contact your Polestar representative for access issues

## 🔄 Updates

To update the collection:
1. Make changes in Postman
2. Export the updated collection
3. Replace the existing JSON file in this repository
4. Commit and push changes

---

**Note**: Keep your credentials secure and never commit them to version control. The environment file contains placeholder values that should be updated with your actual credentials.
