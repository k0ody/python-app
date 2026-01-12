
Instalar o ingress
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/kind/deploy.yaml


iniciar o argocd
helm upgrade --install argocd argo/argo-cd \
  -n argocd --create-namespace \
  -f charts/argocd/values-argo.yaml

verificar senha admin argo
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d

- instalar actions runner controller
  acessar https://github.com/actions/actions-runner-controller/blob/master/docs/quickstart.md
  instalar kubectl apply -f https://github.com/cert-manager/cert-manager/releases/download/v1.8.2/cert-manager.yaml
  
  gerar um token de acesso a nivel de repo
  
  instalar via helm passando o token

  applicar runnerdeploy
  

  