To build and run your Docker container, follow these steps:

### Build the Docker Image
First, we'll build the Docker image for our application. Ensure you are in the directory containing the Dockerfile, then run the following command:

```bash
docker build -t nginx:1.0.0 .
```

This command creates a Docker image named `nginx` with the tag `1.0.0`. The `.` at the end of the command indicates that Docker should look for the Dockerfile in the current directory.

### Running the Docker Container
Once the image is built, you can run it as a container. To do this, use the following command:

```bash
docker run -d -p 8080:80 nginx:1.0.0
```

This command does the following:
- `docker run`: Creates and starts a container.
- `-d`: Runs the container in detached mode, running in the background.
- `-p 8080:80`: Maps port 8080 on the host to port 80 on the container. This means you can access the application on `http://localhost:8080`.
- `nginx:1.0.0`: Specifies the image to use for the container.

With these commands, your Docker container running Nginx should now be accessible through your local host on port 8080.



