# ArgoCD + Kustomize Starter Repo

## Overview
This repo demonstrates deploying an Nginx app using Kustomize overlays and ArgoCD for GitOps.

## Environments
- dev: 1 replica
- staging: 2 replicas
- prod: 3 replicas

## Usage
1. Install ArgoCD in your Kubernetes cluster.
2. Apply an ArgoCD Application:

```bash
kubectl apply -f argo-app-dev.yaml
kubectl apply -f argo-app-staging.yaml
kubectl apply -f argo-app-prod.yaml
```

3. Observe the app deployment in the ArgoCD UI or CLI.
4. Modify base or overlay configs in Git; ArgoCD will reconcile changes automatically.
