# Minikube Registry

A parent chart that contains a nginx controller, docker registry and
dashboard.  Uses basic auth to protect the registry, so a user will
need to use docker login.

## Configure Minikube

```bash
# Docker engine needs to be advised to use an insecure registry
minikube start --cpus 4 --disk-size 100g --memory 6000 --insecure-registry registry.minikube.st81ess.com:80
```

## Install

```bash
#Add the repo if you haven't yet.
helm repo add lakowske https://lakowske.github.io/charts
#After adding the repo, update your index.
helm repo update

helm install lakowske/minikube-registry
```

## Login

```bash
docker login registry.minikube.st81ess.com:80
```

