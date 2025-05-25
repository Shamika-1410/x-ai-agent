# AI Agent for X ( ex-Twitter )

A server application that integrates with Google's Generative AI and provides MCP (Model Context Protocol) functionality. Built with Node.js and Express.

## Features

- 🤖 Integration with Google's Generative AI
- ⚡ Fast and efficient message handling
- 🔒 Environment variable configuration for API keys
- 🔄 MCP (Model Context Protocol) server implementation
- 🛠️ Custom tools for number addition and Twitter post creation

## Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- Google AI API key

## Project Structure

```
├── server/                # Node.js backend server
│   ├── index.js          # Express server setup
│   ├── mcp.tool.js       # MCP tool implementations
│   ├── .env             # Server environment variables
│   └── package.json      # Backend dependencies
│
├── client/               # Node.js client application
│   ├── index.js         # Client application entry point
│   ├── .env            # Client environment variables
│   └── package.json     # Client dependencies
│
├── node_modules/         # Project dependencies
├── package.json          # Root package.json
└── package-lock.json     # Dependency lock file
```

## Setup Instructions

1. Clone the repository:
```bash
git clone <repository-url>
cd <project-directory>
```

2. Install dependencies:
```bash
npm install
```

3. Create `.env` files:

In the server directory (`server/.env`):
```
GEMINI_API_KEY=your_gemini_api_key_here
```

In the client directory (`client/.env`):
```
TWITTER_API_KEY=your_twitter_api_key_here
TWITTER_API_SECRET=your_twitter_api_secret_here
TWITTER_ACCESS_TOKEN=your_twitter_access_token_here
TWITTER_ACCESS_TOKEN_SECRET=your_twitter_access_token_secret_here
```

4. Start the server:
```bash
cd server
node index.js
```

5. In a new terminal, start the client:
```bash
cd client
node index.js
```

The server will be running at `http://localhost:3001`

## Environment Variables

### Server Environment Variables
Create a `.env` file in the server directory with:
- `GEMINI_API_KEY`: Your Gemini API key

### Client Environment Variables
Create a `.env` file in the client directory with:
- `TWITTER_API_KEY`: Your Twitter API key
- `TWITTER_API_SECRET`: Your Twitter API secret key
- `TWITTER_ACCESS_TOKEN`: Your Twitter access token
- `TWITTER_ACCESS_TOKEN_SECRET`: Your Twitter access token secret

To get these Twitter API credentials:
1. Go to the [Twitter Developer Portal](https://developer.twitter.com/en/portal/dashboard)
2. Create a new project and app
3. Navigate to your app's settings
4. Generate your API keys and tokens
5. Make sure to enable the necessary permissions for your app

## Technologies Used

- Backend:
  - Node.js
  - Express
  - dotenv for environment variables
  - @google/generative-ai for AI integration
  - @modelcontextprotocol/sdk for MCP implementation
  - Zod for schema validation

## API Endpoints

- `GET /sse`: Establishes an SSE connection for real-time communication
- `POST /messages`: Handles incoming messages with session management

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Acknowledgments

- Google Generative AI for providing the AI capabilities
- Model Context Protocol team for the MCP implementation 
