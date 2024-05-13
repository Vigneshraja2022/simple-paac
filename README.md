# Simple Jenkins Pipeline as Code

This repository contains a simple Jenkins pipeline script written in Groovy, used for automating build, test, and deployment processes.

## Author

- **Vignesh**

## Usage

### Prerequisites

- Jenkins server with Pipeline plugin installed.
- Maven and Oracle JDK 11 installed on the Jenkins agent.

### Pipeline Setup

1. Create a new Jenkins pipeline job.
2. In the pipeline configuration, select "Pipeline script from SCM" as the definition.
3. Provide the repository URL: `https://github.com/hkhcoder/vprofile-project/`.
4. Specify the branch to build (e.g., `main`).
5. Save the configuration.

### Pipeline Execution

1. Jenkins will automatically trigger the pipeline when changes are pushed to the specified branch in the repository.
2. The pipeline consists of the following stages:
   - **Fetch Code**: Fetches the code from the GitHub repository.
   - **Build**: Builds the project using Maven. Tests are skipped during the build.
   - **Unit Tests**: Runs unit tests using Maven.
3. Artifacts (WAR files) are archived if the build is successful.

## Contributing

Contributions are welcome! If you find any bugs or want to suggest improvements, please feel free to submit a pull request or open an issue.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
