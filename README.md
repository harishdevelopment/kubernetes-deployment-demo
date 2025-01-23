# kubernetes-deployment-demo
Kubernetes Deployment Demo

Steps to Deploy:

Create a namespace
kubectl create ns argocddemo


Apply the ConfigMap:
kubectl apply -n argocddemo -f greeting-app-configmap.yaml

Apply the Deployment:
kubectl apply -n argocddemo -f greeting-app-deployment.yaml

Apply the Service:
kubectl apply -n argocddemo -f greeting-app-service.yaml

Access the API:

If using a LoadBalancer, get the external IP:
kubectl get service -n argocddemo greeting-app-service

Access the API at http://<EXTERNAL_IP>/api.
