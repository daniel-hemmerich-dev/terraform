# Terraform Tutorial

## Setup
You need to setup your cloud provider credentials as environment variables.

###  Amazon Web Services (AWS)
```shell
export AWS_ACCESS_KEY_ID=<YOUR_ACCESS_KEY_ID>
export AWS_SECRET_ACCESS_KEY=<YOUR_SECRET_ACCESS_KEY>
```

###  Microsoft Azure
```shell
export ARM_CLIENT_ID="<APPID_VALUE>"
export ARM_CLIENT_SECRET="<PASSWORD_VALUE>"
export ARM_SUBSCRIPTION_ID="<SUBSCRIPTION_ID>"
export ARM_TENANT_ID="<TENANT_VALUE>"
```

###  Google Cloud Platform (GCP)
1. Save your service account key json file as `service-account-key.json` in the `./gcp` folder.
2. Set your `project_id` in the `variables.tf` file.

### Docker
1. Install and start Docker

### Kubernetes
1. Install and start Docker
2. Install and start Minikube `minikube start`

### Helm
1. Install and start Docker
2. Install and start Minikube `minikube start`


## Terraform most used commands
Use the -chdir parameter to navigate between the different providers. Valid values are:
- ```aws```
- ```azure```
- ```docker```
- ```gcp```
- ``````
- ```helm```

To run the Google Cloud Platform example run:
```shell 
terraform -chdir=./gcp init
```

### Initialize project
Initializes the project and download the needed providers.
```shell 
terraform -chdir=<aws|azure|gcp|docker|k8s|helm> init
```

### Validate
Checks if the configuration files are valid.
```shell
terraform -chdir=<aws|azure|gcp|docker|k8s|helm> validate
```

### Plan
Show changes that will be made if the apply command is executed.
```shell
terraform -chdir=<aws|azure|gcp|docker|k8s|helm> plan
```

### Apply
Apply the changes (update or create) of the configuration files.
```shell
terraform -chdir=<aws|azure|gcp|docker|k8s|helm> apply
```

### Show
Shows the current state.
```shell
terraform -chdir=<aws|azure|gcp|docker|k8s|helm> show
```

### Output
Shows the output values specified in the output files.
```shell
terraform -chdir=<aws|azure|gcp|docker|k8s|helm> output
```

### Destroy
Destroys created infrastructure.
```shell
terraform -chdir=<aws|azure|gcp|docker|k8s|helm> destroy
```

### Format
Format all configuration files to the standard.
```shell
terraform -chdir=<aws|azure|gcp|docker|k8s|helm> fmt
```