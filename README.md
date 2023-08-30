# dogecoin-core-kubernetes
Configs for running Dogecoin full node in Kubernetes

Useful commands:

Deployment
- `kubernetes create -f any/<FILE_NAME>.yml`
- `kubectl delete -f any/<FILE_NAME>.yml`

General
- `kubectl get all -n dogecoin`
- `kubectl get pvc -n dogecoin`
- `kubectl get pv`

Specific
- `export PODNAME=$(kubectl get pods -o wide -n dogecoin | grep dogecoin | awk '{print $1}')`
- `kubectl describe pod -n dogecoin $PODNAME`
- `kubectl exec -it -n dogecoin $PODNAME -- bash`
- > `gosu dogecoin bash`
- > `dogecoin-cli getmininginfo`
- > `dogecoin-cli getwalletinfo`
- > `dogecoin-cli listreceivedbyaddress 1 true`
