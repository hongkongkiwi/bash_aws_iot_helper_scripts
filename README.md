# AWS IoT Helper Scripts

A collection of helper scripts for managing AWS IoT provisioning templates using Bash. These scripts streamline the process of handling provisioning templates by automating common tasks such as version management and deletion.

## Features

- **Delete Old Versions**: Automatically delete older versions of an AWS IoT provisioning template while keeping a specified number of the most recent versions.
- **Error Handling**: Robust error handling for AWS CLI commands to ensure reliability.

## Prerequisites

- AWS CLI installed and configured with appropriate permissions to manage IoT provisioning templates.
- `jq` installed for processing JSON data.

## Scripts

### 1. `delete_old_versions.sh`

This script deletes older versions of an AWS IoT provisioning template while keeping a specified number of the most recent versions.

#### Usage

```bash
./delete_old_versions.sh [TEMPLATE_NAME] [VERSIONS_TO_KEEP]
```

- `TEMPLATE_NAME`: (Optional) The name of the provisioning template. Defaults to "BodyCam".
- `VERSIONS_TO_KEEP`: (Optional) The number of recent versions to keep. Defaults to 1.

#### Example

To delete old versions of the template "MyTemplate" while keeping the last 2 versions:

```bash
./remove_old_iot_template_versions MyTemplate 2
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

