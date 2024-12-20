# WordPress Plugin Deployment Action

[![Deploy Plugin](https://github.com/bajpangosh/wp-plugin-deploy/actions/workflows/deploy.yml/badge.svg)](https://github.com/bajpangosh/wp-plugin-deploy/actions/workflows/deploy.yml)

🚀 A GitHub Action for automatically deploying WordPress plugins to your production server using SSH and rsync.

## Features

- ✅ Secure SSH-based deployment
- 🔒 Pre-deployment connection testing
- 📁 WordPress plugin directory verification
- 🔄 Efficient file synchronization using rsync
- 🎯 Selective file exclusion

## Prerequisites

Before using this action, you'll need to set up the following secrets in your GitHub repository:

- `SSH_USER`: Your server's SSH username
- `SSH_HOST`: Your server's hostname or IP address
- `PLUGIN_DIR`: The absolute path to your WordPress plugins directory
- `DEPLOY_KEY`: Your SSH private key for authentication

## Setup

1. Go to your GitHub repository settings
2. Navigate to "Secrets and variables" → "Actions"
3. Add the required secrets mentioned above

## Workflow Configuration

The workflow is triggered on push to the `main` branch. It performs the following steps:

1. Tests SSH connection to your server
2. Verifies WordPress plugins directory accessibility
3. Deploys plugin files using rsync

## Usage

1. Copy the workflow file to `.github/workflows/deploy.yml` in your repository
2. Configure the required secrets in your repository settings
3. Push your changes to the `main` branch

The action will automatically deploy your plugin files to the specified directory on your server.

## File Exclusions

The following files/directories are automatically excluded from deployment:

- `.git/`
- `.github/`
- `deploy_key`

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

If you encounter any problems or have suggestions, please open an issue in the repository.

---
Last updated: December 20, 2024
