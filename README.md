你好！
很冒昧用这样的方式来和你沟通，如有打扰请忽略我的提交哈。我是光年实验室（gnlab.com）的HR，在招Golang开发工程师，我们是一个技术型团队，技术氛围非常好。全职和兼职都可以，不过最好是全职，工作地点杭州。
我们公司是做流量增长的，Golang负责开发SAAS平台的应用，我们做的很多应用是全新的，工作非常有挑战也很有意思，是国内很多大厂的顾问。
如果有兴趣的话加我微信：13515810775  ，也可以访问 https://gnlab.com/，联系客服转发给HR。
# Heapster

[![GoDoc](https://godoc.org/k8s.io/heapster?status.svg)](https://godoc.org/k8s.io/heapster) [![Build Status](https://travis-ci.org/kubernetes/heapster.svg?branch=master)](https://travis-ci.org/kubernetes/heapster)

Heapster enables Container Cluster Monitoring and Performance Analysis.

Heapster currently supports [Kubernetes](https://github.com/kubernetes/kubernetes) and CoreOS natively.
*Heapster is compatible with kubernetes versions starting from v1.0.6 only*

It can be extended to support other cluster management solutions easily.

Heapster collects and interprets various signals like compute resource usage, lifecycle events, etc, and exports cluster metrics via [REST endpoints](docs/model.md).
**Note: Some of the endpoints are only valid in Kubernetes clusters**

Use [Kubedash](https://github.com/kubernetes/kubedash) to visualize data exported by Heapster.

Heapster supports multiple sources of data.
More information [here](docs/source-configuration.md).

Heapster supports a pluggable storage backend.
It supports [InfluxDB](http://influxdb.com) with [Grafana](http://grafana.org/docs/features/influxdb), [Google Cloud Monitoring](https://cloud.google.com/monitoring/), [Google Cloud Logging](https://cloud.google.com/logging/), [Hawkular](http://www.hawkular.org), [Riemann](http://riemann.io) and [Kafka](http://kafka.apache.org/).
We welcome patches that add additional storage backends.
Documentation on storage sinks [here](docs/sink-configuration.md)
The current version of Storage Schema is documented [here](docs/storage-schema.md).

### Running Heapster on Kubernetes

To run Heapster on a Kubernetes cluster with,
- InfluxDB use [this guide](docs/influxdb.md).
- Google Cloud Monitoring and Google Cloud Logging use [this guide](docs/google.md).

### Running Heapster on OpenShift

Using Heapster to monitor an OpenShift cluster requires some additional changes to the Kubernetes instructions to allow communication between the Heapster instance and OpenShift's secured endpoints. To run a combination of Heapster and Hawkular-Metrics, follow [this guide](https://github.com/hawkular/hawkular-metrics/blob/master/containers/README.adoc).

### Running Heapster on CoreOS

Heapster communicates with the local fleet server to get cluster information. It expected cAdvisor to be running on all the nodes. Refer to [this guide](docs/coreos.md).

### Running in other cluster management systems.

Heapster can be used to enable cluster-wide monitoring on other cluster management solutions by running a simple cluster-specific buddy container that will help Heapster with discovery of hosts.

### Running in standalone mode.

It is also possible to run Heapster standalone on a host with cAdvisor using [this guide](docs/standalone.md).

#### Troubleshooting guide [here](docs/debugging.md)

### Community

Contributions, questions, and comments are all welcomed and encouraged! Heapster and cAdvisor developers hang out in the [#google-containers](http://webchat.freenode.net/?channels=google-containers) room on freenode.net.  You can also reach us on the [google-containers Google Groups mailing list](https://groups.google.com/forum/#!forum/google-containers).
