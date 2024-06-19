# TinyUrl Project

---

## Overview

TinyUrl is a URL shortening and management service designed to create compact, easy-to-share links and track their usage. This README provides an overview of the project, its features, installation instructions, and usage guidelines.

## Features

- **URL Shortening**: Convert long URLs into short, manageable links (e.g., https://tinyurl.co.il/14875).
- **Redirection**: Users are redirected from the short URL to the original long URL seamlessly.
- **Click Tracking**: Track each click on the shortened URL, recording timestamps and IP addresses for analytics.
- **Customizable Links**: Add targeting parameters to URLs for campaign tracking and segmentation (e.g., ?source=facebook).
- **User Management**: Registration and management for users to create, manage, and analyze their own set of shortened links.
- **RESTful API**: API endpoints for link shortening, redirection, and analytics retrieval.
- **Database**: MongoDB used for efficient storage and retrieval of shortened URLs and click data.
- **Technologies**: Node.js, Express.js, MongoDB, Mongoose.

## Installation

To run TinyUrl locally, follow these steps:

1. Clone the repository: `git clone https://github.com/your/repository.git`
2. Navigate to the project directory: `cd TinyUrl`
3. Install dependencies: `npm install`
4. Set up MongoDB locally or configure connection to a remote MongoDB instance.
5. Start the server: `npm start`
6. Access TinyUrl at: `http://localhost:3000`

## Usage

### Shorten a URL

Send a POST request to `/api/shorten` with JSON payload:
```json
{
  "longUrl": "https://example.com/very/long/url"
}
```

### Redirect

Shortened URLs redirect to the original long URL:
```
https://tinyurl.co.il/14875 -> https://example.com/very/long/url
```

### Analytics

Retrieve click analytics for a shortened URL:
```
GET /api/analytics?url=14875
```

## Contributing

Contributions are welcome! Follow these steps to contribute:

1. Fork the repository.
2. Create a new branch: `git checkout -b feature/new-feature`.
3. Make your changes and commit them: `git commit -am 'Add new feature'`.
4. Push to the branch: `git push origin feature/new-feature`.
5. Submit a pull request.
