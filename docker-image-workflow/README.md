# Docker Image Workflow

This project provides a workflow for building and pushing a Docker image for a Node.js application.

## Project Structure

```
docker-image-workflow
├── .github
│   └── workflows
│       └── docker-image.yml      # GitHub Actions workflow for Docker image
├── docker
│   └── Dockerfile                 # Dockerfile for building the image
├── src
│   └── app.js                     # Main application file
├── package.json                   # npm configuration file
└── README.md                      # Project documentation
```

## Prerequisites

- Docker installed on your machine.
- Node.js and npm installed.
- Access to a container registry (e.g., Docker Hub, AWS ECR).

## Building the Docker Image

1. Navigate to the project directory:
   ```
   cd docker-image-workflow
   ```

2. Build the Docker image using the following command:
   ```
   docker build -t your-image-name:tag ./docker
   ```

## Running the Docker Container

To run the Docker container, use the following command:
```
docker run -p 3000:3000 your-image-name:tag
```

Replace `your-image-name:tag` with the name and tag of your Docker image.

## GitHub Actions Workflow

The GitHub Actions workflow defined in `.github/workflows/docker-image.yml` will automatically build and push the Docker image to your specified container registry on every push to the main branch.

## License

This project is licensed under the MIT License.