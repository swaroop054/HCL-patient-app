# Use the official Node.js image as the base images
FROM node:18-alpine


# Set the working directory inside the container
WORKDIR /app

# Copy the package.json and package-lock.json (if available) first to leverage Docker cache
COPY package*.json ./

# Install the application dependencies
RUN npm install

# Copy the rest of the application files
COPY . .

# Expose the port that the app will run on
EXPOSE 3000

# Set the command to run the app
CMD ["node", "patient.js"]
