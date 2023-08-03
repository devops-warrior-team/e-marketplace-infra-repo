# e-marketplace-infra-repo
Repository for infrastructure as a code and Continous deployment in E-marketplace Environment

## Structure Folder
This repository will be contains services manifest for deployment in kubernetes, and will be use ArgoCD for maintenance the Continous Deployment\
We **Don't** trigger sync in argocd by Github Actions, but we set automatically sync in ArgoCD for detect change in this repo.\
```
./github/workflows -> Location Github action worfklows for update image tag triggered from app repository
./<service-name>  -> Name of service
./<service-name>/argocd-manifest  -> ArgoCD manifest application
./<service-name>/kubernetes-manifest -> Kubernetes manifest for updating from ArgoCD
```

## Getting Started
Before using this repo, we must prepare the configuration first for argoCD, we apply argocd-manifest\
`kubectl apply -f ./<service-name>/argocd-manifest/application.yaml`






## References
[Kubernetes CI/CD with Github, Github Actions and ArgoCD](https://igboie.medium.com/kubernetes-ci-cd-with-github-github-actions-and-argo-cd-36b88b6bda64)