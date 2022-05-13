# minecraft-manifests
## prerequirement
phantom-macos --server ${server}:${port}

## update whitelist
```
kubectl cp whitelist.json \
  $(kubectl get pod -l app=mc-bedrock -o custom-columns=:metadata.name):/data/whitelist.json

kubectl rollout restart deployment/mc-bedrock
```

## refs
http://caseywest.com/run-minecraft-server-on-kubernetes/
