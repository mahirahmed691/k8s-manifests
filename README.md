# Kubernetes Manifests for App

This repository contains Kubernetes manifests for deploying the **app-name** application on a Kubernetes cluster.

## Files:
- `deployment.yaml`: Defines the deployment of the app.
- `service.yaml`: Defines how the app is exposed internally.
- `ingress.yaml`: Defines the ingress resource for external access (optional).
- `argo-app.yaml`: Defines the Argo CD Application for syncing the repo to the cluster.

## Usage:

1. Clone this repository:
    ```bash
    git clone https://github.com/your-username/k8s-manifest-repo.git
    cd k8s-manifest-repo
    ```

2. Apply Kubernetes manifests manually or using Argo CD:
    - Using `kubectl`:
      ```bash
      kubectl apply -f apps/app-name/deployment.yaml
      kubectl apply -f apps/app-name/service.yaml
      kubectl apply -f apps/app-name/ingress.yaml
      ```
    - Using Argo CD (if Argo CD is set up):
      ```bash
      argocd app create -f argo-app.yaml
      argocd app sync app-name
      ```

## Argo CD Integration

This repository is integrated with Argo CD. If you have Argo CD running, you can use it to automatically sync these manifests to your Kubernetes cluster.


