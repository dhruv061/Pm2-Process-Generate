
# PM2 Process Generator

This repository contains two files:

1. **index.html**: Displays a simple "Hello" message.
2. **server.js**: A PM2 application that generates PM2 processes and logs to a `server.log` file.

## How It Works

The `server.js` file is designed to generate a PM2 process with a specified port. Each new process creates or updates a `server.log` file to capture server logs.

### Adding a New PM2 Process

To add a new PM2 process, follow these steps:

1. Navigate to the directory where `server.js` is stored.
2. Use the following command to start the process, replacing the port number as needed:

```bash
PORT=<your-port> pm2 start server.js --name "server-<your-port>"
```

For example, to run the application on port `3004`, use:

```bash
PORT=3004 pm2 start server.js --name "server-3004"
```

### Log File

The `server.js` process generates a file named `server.log` that captures all server logs. Each PM2 process will append logs to this file.

