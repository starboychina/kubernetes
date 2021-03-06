---
---

## kubectl rollout pause

Mark the provided resource as paused

### 摘要


Mark the provided resource as paused

Paused resources will not be reconciled by a controller.
Use \"kubectl rollout resume\" to resume a paused resource.
Currently only deployments support being paused.

```
kubectl rollout pause RESOURCE
```

### 示例

```
# Mark the nginx deployment as paused. Any current state of
# the deployment will continue its function, new updates to the deployment will not
# have an effect as long as the deployment is paused.
kubectl rollout pause deployment/nginx
```

### 选项

```
  -f, --filename=[]: Filename, directory, or URL to a file identifying the resource to get from a server.
  -R, --recursive[=false]: Process the directory used in -f, --filename recursively. Useful when you want to manage related manifests organized within the same directory.
```

{% include_relative parent_commands.md %}

### 参见

* [kubectl rollout](kubectl_rollout.md)	 - rollout manages a deployment
