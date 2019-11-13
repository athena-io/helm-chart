# Athena Backend Server - Helm Chart

1. Add the repo to helm:
`helm repo add athenarepo https://athena-io.github.io/helm-chart`
2. Update helm
`helm repo update`
3. Install the chart
`helm install --name athena-be athenarepo/athena-be`
4. Check with `kubectl` that the BE is running:
`kubectl get pods`
5. Forward the port (The service listen port is 5000)
`kubectl port-forward svc/athena-be 8888:5000`

*Note*:
The backend server should have a fixed IP+PORT address.
