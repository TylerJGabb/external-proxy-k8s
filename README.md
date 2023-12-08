# K8s Svc/Ing Sandbox

Following this tutorial to try and get an ingress that uses a backend service that rountes to external ip
https://www.kristhecodingunicorn.com/post/kubernetes-service-to-proxy-to-external-services/

## Unanswered Questions:
1. How to use a service to proxy to an external service?
2. How to use an ingress to proxy to an external service?
3. What is the ingress class `gce-internal` and how does it work?

# Running Locally

1. Install kind cluster `kind create cluster`
2. Install the manifests `kubectl apply -f external-proxy/`
3. View the ingress object `kubectl get ing proxy-service-ingress -o yaml`
4. **PROBLEM** Note that at this point, the ingress object has no ip address. Is this is because the ingress controller is not running? I installed the nginx ingress controller and its still not working.

