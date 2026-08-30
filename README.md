# Kubernetes Exercises & Reference

This section contains questions, commands, and exercises related to Kubernetes.

## Core Concepts

- **Pod**: Smallest deployable unit in Kubernetes.
- **Service**: Abstraction defining a logical set of Pods and a policy to access them.
- **Deployment**: Declarative updates for Pods and ReplicaSets.
- **Ingress**: Manages external access to services in a cluster.

## Quick Command Reference

```bash
# Get cluster nodes
kubectl get nodes

# Check pod status and details
kubectl get pods -o wide
kubectl describe pod <pod-name>

# View logs (with tail/follow)
kubectl logs -f <pod-name> -c <container-name>

# Check resource usage (requires metrics-server to be running)
kubectl top nodes
kubectl top pods --all-namespaces
```

## Useful Troubleshooting Steps

1. Check pod events: `kubectl describe pod <pod-name>`
2. Fetch logs from previous failed instance: `kubectl logs <pod-name> --previous`
3. Execute interactive shell inside pod: `kubectl exec -it <pod-name> -- /bin/sh`