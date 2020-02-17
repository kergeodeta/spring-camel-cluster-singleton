# spring-camel-cluster-singleton
Camel based cluster singleton service using camel's core FileLockClusterService.


## Camel Leader Election on Kubernetes and Openshift, based of file cluster service

Based on blog article post: https://www.nicolaferraro.me/2017/10/17/creating-clustered-singleton-services-on-kubernetes/

Original gitlab link: [https://github.com/nicolaferraro/camel-leader-election.git](https://github.com/nicolaferraro/camel-leader-election.git)

## Should be changed to File Cluster Service

Service: ```FileLockClusterService```

Config:  [Camel Cluster Service](https://camel.apache.org/manual/latest/clustering.html)

```
camel.component.file.cluster.service.enabled = true
camel.component.file.cluster.service.id = ${random.uuid}
camel.component.file.cluster.service.root = ${java.io.tmpdir}
camel.component.file.cluster.service.cluster-labels[group]=${project.groupId}
camel.component.file.cluster.service.cluster-labels[app]=${project.artifactId}
```
