# k8s_argocd

helm repo add argo https://argoproj.github.io/argo-helm

helm repo update

helm show values argo/argo-cd --version 3.35.4 > argocd-defaults.yaml

## Terraform
terraform init

terraform apply

## Kubectl

kubectl get pods =n argocd

kubectl get secrets -n argocd

kubectl get secrets argocd-initial-admin-secret -o yaml -n argocd

kubectl "<YOUR_PASSWORD>" | base64 -d

kubectl port-forward svc/argocd-server -n argocd 8080:80

## Docker

docker login --username <YOUR_USERNAME>

docker pull nginx:1.23.3

docker tag nginx:1.23.3 simbamon/nginx:v0.1.0

docker push simbamon/nginx:v0.1.0