# VSCode Settings for Jenkins Extensions

This repository contains VSCode settings for running [Jenkins Runner](https://marketplace.visualstudio.com/items?itemName=dave-hagedorn.jenkins-runner), [Jenkins Pipeline Linter Connector](https://marketplace.visualstudio.com/items?itemName=janjoerke.jenkins-pipeline-linter-connector) and [Code-Groovy](https://marketplace.visualstudio.com/items?itemName=NicolasVuillamy.vscode-groovy-lint) extensions with a local Jenkins instance running in Docker.

## Setup

1. Ensure you have a local Jenkins instance running on `http://localhost:8080`.
2. Install the following VSCode extensions:
   - [Jenkins Runner](https://marketplace.visualstudio.com/items?itemName=dave-hagedorn.jenkins-runner)
   - [Jenkins Pipeline Linter Connector](https://marketplace.visualstudio.com/items?itemName=janjoerke.jenkins-pipeline-linter-connector)
   - [Code-Groovy](https://marketplace.visualstudio.com/items?itemName=NicolasVuillamy.vscode-groovy-lint)
3. Copy the contents of `settings.json` into your VSCode settings.
4. **Important:** Manually create a pipeline job named "default-pipeline" in your Jenkins instance. The Jenkins Runner extension will use this job by default.

## Configuration

The `settings.json` file contains the following configurations:

### Jenkins Runner
- Host configuration for local Jenkins instance
- Default job configuration

### Jenkins Pipeline Linter Connector
- URL for the Pipeline Linter
- Authentication details for accessing Jenkins

### Code-Groovy for Syntax Highlighting
- File associations for Jenkinsfile and *.jenkins files to use Groovy syntax highlighting

## Usage

With these settings in place, you can:

1. Run Jenkins jobs directly from VSCode using the Jenkins Runner extension.
2. Lint your Jenkinsfile using the Jenkins Pipeline Linter Connector extension.
3. Enjoy Groovy syntax highlighting for your Jenkinsfile and *.jenkins files.

Refer to the respective extension documentation for detailed usage instructions.

## Security Note

The current configuration uses plaintext username and password. For improved security, consider using environment variables or a credentials manager to store sensitive information.
