# Generic Ingress Controller Deployment with Azure Application Gateway

This repository contains a generic deployment manifest for an Azure Application Gateway Ingress Controller (AGIC) in an AKS cluster. It provides an example of routing traffic to multiple services using an ingress resource.

## Prerequisites

Before you begin, ensure you have the following tools and infrastructure installed:

1. **AKS Cluster with Azure CNI**: An AKS cluster configured with Azure Container Networking Interface (CNI).
2. **Application Gateway v2**: An Application Gateway v2 deployed in the same virtual network as the AKS cluster.
3. **Microsoft Entra Workload ID**: Configured for your AKS cluster to handle identity and access management.
4. **Cloud Shell**: The Azure Cloud Shell environment, which includes the `az CLI`, `kubectl`, and `helm` tools required for the configuration.

## Steps to Deploy

### 1. Clone the Repository

Clone the repository containing the ingress manifest.

```bash
git clone https://github.com/NashTech-Labs/Application-gateway-Ingress-addon.git
cd Application-gateway-Ingress-addon
```

### 2. Apply the manifest file

```bash
$namespace="namespace"
$file="pet-supplies-ingress.yaml"
kubectl apply -f $file -n $namespace
```

