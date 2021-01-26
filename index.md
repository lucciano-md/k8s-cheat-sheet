# What is Kubernetes?

From [https://kubernetes.io/](https://kubernetes.io/docs/concepts/overview/what-is-kubernetes/)
    
>  Kubernetes is a portable, extensible, open-source platform for managing containerized workloads and services, that facilitates both declarative configuration and automation. It has a large, rapidly growing ecosystem. Kubernetes services, support, and tools are widely available.
 >   The name Kubernetes originates from Greek, meaning helmsman or pilot. Google open-sourced the Kubernetes project in 2014. Kubernetes combines over 15 years of Google's experience running production workloads at scale with best-of-breed ideas and practices from the community.

We sometimes refer it as *k8s*, the same way internationalization is referred a *i18n* or localization, *l10n*.

## Kubernetes Flavors

## What this mean?
  While kubernetes is a container orchestration system, this dosen't mean that all kubernetes are deployed in the same way, or has the same api, in fact some of the managed options may disable experimental features in order to provide a more stable environment.

# Concepts

* Node
>Kubernetes runs your workload by placing containers into Pods to run on Nodes. A node may be a virtual or physical machine, depending on the cluster. Each node contains the services necessary to run Pods, managed by the control plane.

* Workloads
    * Pod
        >Pods are the smallest deployable units of computing that you can create and manage in Kubernetes.

    * Deployment and ReplicaSet.
        > Deployment is a good fit for managing a stateless application workload on your cluster, where any Pod in the Deployment is interchangeable and can be replaced if needed.

    * StatefulSet
        >lets you run one or more related Pods that do track state somehow. For example, if your workload records data persistently, you can run a StatefulSet that matches each Pod with a PersistentVolume.

    * DaemonSet
        >defines Pods that provide node-local facilities. Every time you add a node to your cluster that matches the specification in a DaemonSet, the control plane schedules a Pod for that DaemonSet onto the new node.

    * Job and CronJob
        > define tasks that run to completion and then stop. Jobs represent one-off tasks, whereas CronJobs recur according to a schedule.

More glossary terms on [kubernetes.io](https://kubernetes.io/docs/reference/glossary/).

# Installing your own.

Depending of your own requirements and possibilities, you will

* provision your own cluster for production or development
    For development
    * docker desktop, this is the current recommended setup for windows users.
    * kind
    * minikube
    * [k1s](https://github.com/maniaque/k1s)
    * https://k3s.io/

    For production / testing
    * kubeadmin
    * kubespray
    * kOps

* Provision a managed server
    * Amazon (EKS)
    * Azure (AKS)
    * Google (GKE)

Once the cluster is deployed you will need [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/) to access it.
Also as a reference take a look to  [https://kubectl.docs.kubernetes.io/](https://kubectl.docs.kubernetes.io/)

# Addeding basic services

 * [Metrics Server](https://github.com/kubernetes-sigs/metrics-server)

# Defining K8s Applications.

 * [Example: Deploying WordPress and MySQL with Persistent Volumes](https://kubernetes.io/docs/tutorials/stateful-application/mysql-wordpress-persistent-volume/)
 * 


# Learning resources:

* https://kubernetes.io/training/
* https://github.com/cncf/curriculum

* https://jamesdefabia.github.io/docs/

* https://github.com/kelseyhightower/kubernetes-the-hard-way
* https://github.com/yinchuan/kubernetes-the-hard-way-virtualbox


# Other tools
* https://github.com/pulumi/pulumi-kubernetes
* https://tanka.dev/tutorial/overview
* https://cdk8s.io/
* https://ramitsurana.gitbook.io/awesome-kubernetes/docs/installers/installers
* https://github.com/RehanSaeed/Kubernetes-Cheat-Sheet
* https://k8slens.dev/
* https://github.com/kubernetes-sigs/metrics-server
