# Frontend React Application Deployment Pipeline

This repository contains the Azure DevOps pipeline setup to deploy a frontend React application. The pipeline automates the process of building the application, storing the artifacts, and deploying it using NGINX on a deployment server.

## Pipeline Steps

1. **Checkout Code from GitHub**: The pipeline starts by fetching the source code from the GitHub repository.

2. **Build Process**: The code is built using Gradle and npm to compile the necessary dependencies.

3. **Artifact Creation**: Once the build process is completed, the application build is stored as an artifact. This artifact contains the compiled code ready for deployment.

4. **Deployment**: The artifact is then copied to a deployment server. On the deployment server, NGINX is configured to serve the application. Users can access the deployed application via the deployment server's IP address or domain name.

## Prerequisites

Before running the pipeline, ensure the following prerequisites are met:

- Azure DevOps account with appropriate permissions to create and manage pipelines.
- Access to a build server capable of running Gradle and npm.
- A deployment server configured with NGINX to host the React application.

## Pipeline Configuration

To set up the pipeline in your Azure DevOps environment, follow these steps:

1. **Clone Repository**: Clone this repository to your local machine or fork it directly within your GitHub account.

2. **Azure DevOps Configuration**: Log in to your Azure DevOps account and create a new pipeline.

3. **Pipeline Setup**: Choose the appropriate repository (the one you cloned or forked) and configure the pipeline to trigger on changes to the master branch.

4. **Pipeline Tasks**: Define the pipeline tasks as described in the pipeline steps above. Ensure proper configuration for checking out code, building the application, and deploying it to the deployment server.

5. **Variables**: Set any necessary environment variables or pipeline variables required for the deployment process.

6. **Run Pipeline**: Once configured, trigger the pipeline manually or wait for changes to the master branch to automatically trigger it.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvement, feel free to open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
