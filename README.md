# EventsLogger

:construction: **This repository is under development.**

EventsLogger is Kubernetes Component that logging events.

## Installation

```shell
$ kubectl apply -k manifests
```

## Usage

```shell
$ kubectl logs -l app=events-logger
{"metadata":{"name":"events-logger-586d65786c-fcpln.15d85ffc3af8ce7b","namespace":"default","selfLink":"/apis/events.k8s.io/v1beta1/namespaces/default/events/events-logger-586d65786c-fcpln.15d85ffc3af8ce7b","uid":"1110e36f-2dad-4832-b216-7cdcc7e4dc5d","resourceVersion":"2413","creationTimestamp":"2019-11-18T21:46:46Z"},"eventTime":"2019-11-18T21:46:46.691762Z","reportingController":"default-scheduler","reportingInstance":"default-scheduler-minikube","action":"Binding","reason":"Scheduled","regarding":{"kind":"Pod","namespace":"default","name":"events-logger-586d65786c-fcpln","uid":"2bf55e16-960e-42ce-9396-342f3d5de91e","apiVersion":"v1","resourceVersion":"2408"},"note":"Successfully assigned default/events-logger-586d65786c-fcpln to minikube","type":"Normal","deprecatedSource":{"component":"default-scheduler"},"deprecatedFirstTimestamp":null,"deprecatedLastTimestamp":null}
{"metadata":{"name":"events-logger-586d65786c-fcpln.15d85ffc7cac67a3","namespace":"default","selfLink":"/apis/events.k8s.io/v1beta1/namespaces/default/events/events-logger-586d65786c-fcpln.15d85ffc7cac67a3","uid":"f5567268-c40d-4393-9846-2d9ccfab0e20","resourceVersion":"2418","creationTimestamp":"2019-11-18T21:46:47Z"},"eventTime":null,"reason":"Pulling","regarding":{"kind":"Pod","namespace":"default","name":"events-logger-586d65786c-fcpln","uid":"2bf55e16-960e-42ce-9396-342f3d5de91e","apiVersion":"v1","resourceVersion":"2409","fieldPath":"spec.containers{controller}"},"note":"Pulling image \"docker.pkg.github.com/kaidotdev/events-logger/events-logger:6bd1d07\"","type":"Normal","deprecatedSource":{"component":"kubelet","host":"minikube"},"deprecatedFirstTimestamp":"2019-11-18T21:46:47Z","deprecatedLastTimestamp":"2019-11-18T21:46:47Z","deprecatedCount":1}
{"metadata":{"name":"minikube.15d85e95b7177385","namespace":"default","selfLink":"/apis/events.k8s.io/v1beta1/namespaces/default/events/minikube.15d85e95b7177385","uid":"91aec71d-ade1-46db-a9a5-00f133699095","resourceVersion":"269","creationTimestamp":"2019-11-18T21:21:13Z"},"eventTime":null,"reason":"NodeHasNoDiskPressure","regarding":{"kind":"Node","name":"minikube","uid":"minikube"},"note":"Node minikube status is now: NodeHasNoDiskPressure","type":"Normal","deprecatedSource":{"component":"kubelet","host":"minikube"},"deprecatedFirstTimestamp":"2019-11-18T21:21:06Z","deprecatedLastTimestamp":"2019-11-18T21:21:07Z","deprecatedCount":8}
```
