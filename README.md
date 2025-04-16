# React example with MindAR 

This is an example project of using [MindAR](https://github.com/hiukim/mind-ar-js) in React 

The react components are:

1. `src/mindar-viewer` (AFRAME version), and 
2. `src/mindar-three-viewer` (ThreeJS version). 

Everything else are created from `create-react-app`, and they are irrelevant. 

# Screenshot
|![alt text](https://github.com/hiukim/mind-ar-js-react/blob/master/screenshot.png?raw=true)|
|-

# It demonstrates:

1. how to import MindAR as a npm package
2. how to create a React component for MindAR

# Prerequisites

- Node.js 18.x (LTS version)
- npm 6.x or later
- Docker and Docker Compose (for Docker setup)

## Installing Node.js 18

### macOS

1. Install nvm (Node Version Manager):
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash
```

2. Install and use Node.js 18:
```bash
nvm install 18
nvm use 18
```

### Ubuntu/Debian

1. Install nvm:
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash
source ~/.bashrc
```

2. Install and use Node.js 18:
```bash
nvm install 18
nvm use 18
```

### Switching Node.js Versions

If you need to switch between different Node.js versions:

1. List available versions:
```bash
nvm ls
```

2. Switch to a specific version:
```bash
nvm use <version>
```

3. Set default version:
```bash
nvm alias default 18
```

# Setup and Running

## Option 1: Using npm

### Installation

1. Install system dependencies:

For macOS:
```bash
brew install pkg-config pixman cairo pango giflib
```

For Ubuntu/Debian:
```bash
sudo apt-get update
sudo apt-get install -y pkg-config libpixman-1-dev libcairo2-dev libpango1.0-dev libgif-dev
```

2. Install project dependencies:
```bash
npm install
```

### Running the Application

For local development:
```bash
npm start
```

## Option 2: Using Docker

### Installation

1. Build and start the container:
```bash
docker-compose up --build
```

The Docker setup includes all necessary system dependencies:
- build-essential (for native module compilation)
- pkg-config
- libpixman-1-dev
- libcairo2-dev
- libpango1.0-dev
- libgif-dev

### Running the Application

The application will be available at:
- http://localhost:3000

# Troubleshooting

## Common Issues and Solutions

### 1. Canvas Installation Issues

If you encounter canvas installation errors, ensure you have the following system dependencies installed:

For macOS:
```bash
brew install pkg-config pixman cairo pango giflib
```

For Ubuntu/Debian:
```bash
sudo apt-get update
sudo apt-get install -y pkg-config libpixman-1-dev libcairo2-dev libpango1.0-dev libgif-dev
```

### 2. Node.js Version Compatibility

If you experience compatibility issues:
- Use Node.js 18.x (LTS version)
- If using nvm, run:
```bash
nvm install 18
nvm use 18
```

# Development Notes

- The application uses Create React App for the development environment
- MindAR components are located in `src/mindar-viewer` and `src/mindar-three-viewer`
- For production builds, use `npm run build`
- For testing, use `npm test`

# License

This project is licensed under the MIT License - see the LICENSE file for details.
