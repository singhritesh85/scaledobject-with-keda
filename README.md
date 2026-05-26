```
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo update
helm install kube-prometheus-stack prometheus-community/kube-prometheus-stack --namespace monitoring --create-namespace --kube-context=gke_wise-trainer-244916_us-central1_multicloud-gke-cluster
```

```
kubectl get secret --namespace monitoring kube-prometheus-stack-grafana -o jsonpath="{.data.admin-password}" --context=gke_wise-trainer-244916_us-central1_multicloud-gke-cluster | base64 --decode; echo
```
