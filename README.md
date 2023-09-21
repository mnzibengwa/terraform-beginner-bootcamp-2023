# Terraform Beginner Bootcamp 2023

## Semantic Versioning :mage:
This project is going to utilize semantic versioning for its tagging. 
[semver.org](https://semver.org/)

Given a version number **MAJOR.MINOR.PATCH,** increment the:

- **MAJOR** version when you make incompatible API changes**
- **MINOR** version when you add functionality in a backward compatible manner**
- **PATCH** version when you make backward compatible bug fixes**
- **Additional
88 labels for pre-release and build metadata are available as extensions to the MAJOR.MINOR.PATCH format.**

## Install the Terraform CLI 

### Considerations with the Terraform CLI Changes 

TF CLI installation instructions have changed due to gpg keyring. Updating the installation procedure to allow successful installation via bash script following steps in TF website

### Refactoring into Bash Scripts 
To make Gitpod task file easier to read, moved installation to bash script. Also improves portability since as same script can be used in other projects. 
Bash script location [./bin/install_terraform_cli.sh](./bin/install_terraform_cli.sh)

[Install Terraform CLI](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli)

### OS considerations 
It may be necessary to modify script for your OS 
Current script runs on Debian/Ubuntu 
Use command cat /ets/os-release to check your OS and make changes if necessary

### Linux Permissions
Script requires execute permissions 
Use chmod u+x ./bin/install_terraform_cli to grant script necessary permissions or chmod 744 ./bin/install_terraform_cli

### Gitpod Lifecycle 
Be careful when using Init, workspace will not run init on restart.
Use before instead 
https://www.gitpod.io/docs/configure/workspaces/workspace-lifecycle