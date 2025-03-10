# Microsoft Azure AKS Project

## Overview
This project is focused on deploying and managing Kubernetes clusters using Azure Kubernetes Service (AKS). AKS simplifies the deployment, management, and operations of Kubernetes.

## Prerequisites
- Azure Subscription
- Azure CLI
- kubectl
- Helm

## Setup

### 1. Install Azure CLI
Follow the instructions to install the Azure CLI from the [official documentation](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli).

### 2. Install kubectl
Install kubectl to interact with your Kubernetes cluster. Instructions can be found [here](https://kubernetes.io/docs/tasks/tools/install-kubectl/).

### 3. Install Helm
Helm is a package manager for Kubernetes. Install it from the [official documentation](https://helm.sh/docs/intro/install/).

## Deployment

### 1. Login to Azure
```sh
az login
```

### 2. Create a Resource Group
```sh
az group create --name myResourceGroup --location eastus
```

### 3. Create an AKS Cluster
```sh
az aks create --resource-group myResourceGroup --name myAKSCluster --node-count 1 --enable-addons monitoring --generate-ssh-keys
```

### 4. Get AKS Credentials
```sh
az aks get-credentials --resource-group myResourceGroup --name myAKSCluster
```

### 5. Verify the Cluster
```sh
kubectl get nodes
```

## Usage

### Deploying Applications
You can deploy applications to your AKS cluster using kubectl or Helm charts. For example, to deploy a sample Nginx application:
```sh
kubectl apply -f https://k8s.io/examples/application/deployment.yaml
```

### Monitoring and Logging
AKS integrates with Azure Monitor for monitoring and logging. You can view metrics and logs in the Azure portal.

## Contributing
Contributions are welcome! Please submit a pull request or open an issue to discuss your ideas.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact
For any questions or support, please contact [support@eficode.com](mailto:support@eficode.com).
