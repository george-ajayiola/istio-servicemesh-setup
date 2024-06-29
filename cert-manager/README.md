## Verify policy enforcement, mtLS

### Exec into the Pod
Exec into the pod. Use the following command to access the pod:
```
kubectl exec -it <pod-name> -n <namespace> -c istio-proxy -- /bin/bash
```
```
curl http://<service-name>.<namespace>.svc.cluster.local:<port>/<path>
```
```
curl -s -o /dev/null -s -w "Response code: %{http_code}\n" http://frontend.default.svc.cluster.local:80
```
