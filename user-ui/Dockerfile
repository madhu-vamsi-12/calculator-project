# Use a specific version of Node.js from NodeSource
FROM node:14

# Set the working directory to /home/node/app
WORKDIR /usr/src/app

# Copy package.json and package-lock.json first to leverage Docker cache
COPY package*.json ./

# Install application dependencies
RUN npm install

# Copy the rest of the application files
COPY . .

# Expose any necessary ports for your Node.js application
EXPOSE 3000

# Set the entrypoint to run the Node.js application
CMD ["npm", "run", "start"]
