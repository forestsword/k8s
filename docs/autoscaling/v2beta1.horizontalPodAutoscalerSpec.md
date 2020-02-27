
## horizontalPodAutoscalerSpec
HorizontalPodAutoscalerSpec describes the desired functionality of the HorizontalPodAutoscaler.

**Functions:**

[`fn .withMaxReplicas`](#fn-withmaxreplicas)  
[`fn .withMetrics`](#fn-withmetrics)  
[`fn .withMinReplicas`](#fn-withminreplicas)  
[`fn scaleTargetRef.withName`](#fn-scaletargetrefwithname)  

---


### `fn .withMaxReplicas`
maxReplicas is the upper limit for the number of replicas to which the autoscaler can scale up. It cannot be less that minReplicas.
```jsonnet
{
  withMaxReplicas(maxReplicas):: {}
}
```

### `fn .withMetrics`
metrics contains the specifications for which to use to calculate the desired replica count (the maximum replica count across all metrics will be used).  The desired replica count is calculated multiplying the ratio between the target value and the current value by the current number of pods.  Ergo, metrics used must decrease as the pod count is increased, and vice-versa.  See the individual metric source types for more information about how each type of metric must respond.
```jsonnet
{
  withMetrics(metrics):: {}
}
```

### `fn .withMinReplicas`
minReplicas is the lower limit for the number of replicas to which the autoscaler can scale down.  It defaults to 1 pod.  minReplicas is allowed to be 0 if the alpha feature gate HPAScaleToZero is enabled and at least one Object or External metric is configured.  Scaling is active as long as at least one metric value is available.
```jsonnet
{
  withMinReplicas(minReplicas):: {}
}
```

### `fn scaleTargetRef.withName`
Name of the referent; More info: http://kubernetes.io/docs/user-guide/identifiers#names
```jsonnet
{
  withName(name):: {}
}
```
