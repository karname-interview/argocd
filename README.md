# ArgoCD 

## Configure existing ArgoCD

Just make sure to add these two fields to ArgoCDs `argo-cm` configmap
```
  kustomize.buildOptions: --load-restrictor LoadRestrictionsNone
  timeout.reconciliation: 60s

```

## Install fresh ArgoCD

Install ArgoCD using following command 
```bash 
kubectl create ns argocd
kubectl apply -f install.yaml
```

