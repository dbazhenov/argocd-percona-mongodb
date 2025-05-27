# ArgoCD Percona MongoDB Deployment  

This repository provides an **automated deployment** of Percona Server for MongoDB using **ArgoCD**. It simplifies the setup and management of MongoDB clusters in a Kubernetes environment using GitOps principles.  

## Quick Start  

To deploy the ArgoCD application, run:  

```sh
kubectl apply -f argocd.yaml -n argocd
```

This will create and configure all necessary ArgoCD Applications to manage the MongoDB cluster.

## Repository Structure

* argocd.yaml – Main ArgoCD configuration file, handling GitOps tracking

* apps/ – Directory containing separate ArgoCD Application manifests:

    * mongodb-operator.yaml – Deploys the Percona MongoDB operator

    * psmdb-db.yaml – Deploys and configures the MongoDB cluster


## Configuration

* The repository uses ArgoCD to continuously manage the state of MongoDB deployments in Kubernetes.

* Applications use the Percona Helm charts to deploy MongoDB and its operator.

* The MongoDB cluster runs inside the clusters namespace.