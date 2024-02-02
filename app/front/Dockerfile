# Use Nginx as the base image
FROM nginx:alpine

# Set working directory to Nginx's serve directory
WORKDIR /usr/share/nginx/html

# Copy the contents of the app/front directory to the workdir
COPY . /usr/share/nginx/html

# Set the environment variable
ENV WS_BACK_URL=http://localhost:8000

# Use exec form of ENTRYPOINT to make Nginx stay in the foreground so Docker can track it
ENTRYPOINT ["nginx", "-g", "daemon off;"]

# Expose port 80 for the web server (you might need to adjust this if there's a port conflict)
EXPOSE 80
