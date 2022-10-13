Learn Kubernetes: Basics to Advanced Concepts
1. Kubernetes Terminology
Terms that you should be familiar with before starting off with Kubernetes are enlisted below:

Terms	Explanation
Cluster	It can be thought of as a group of physical or virtual servers where Kubernetes is installed.
Nodes	
There are two types of Nodes, 

Master node is a physical or virtual server that is used to control the Kubernetes cluster.
Worker node is the physical or virtual server where workload runs in given container technology.
Pods	The group of containers that shares the same network namespaces.
Labels	These are the key-value pairs defined by the user and associated with Pods.
Master	It controls plane components to provide access points for admins to manage the cluster workloads.
Service	It can be viewed as an abstraction that serves as a proxy for a group of Pods performing a "service".
Since now we have a fair understanding of what Kubernetes is, let's now jump to the cheat sheet.

2. Kubernetes Commands
Viewing Resource Information:

1. Nodes: 

ShortCode = no

A Node is a worker machine in Kubernetes and may be either a virtual or a physical machine, depending on the cluster. Each Node is managed by the control plane. A Node can have multiple pods, and the Kubernetes control plane automatically handles scheduling the pods across the Nodes in the cluster.

Commands	Description
kubectl get node	To list down all worker nodes.
kubectl delete node <node_name>	Delete the given node in cluster.
kubectl top node	Show metrics for a given node.
kubectl describe nodes | grep ALLOCATED -A 5	Describe all the nodes in verbose.
kubectl get pods -o wide | grep <node_name>	List all pods in the current namespace, with more details.
kubectl get no -o wide	List all the nodes with mode details.
kubectl describe no	Describe the given node in verbose.
kubectl annotate node <node_name>	Add an annotation for the given node.
kubectl uncordon node <node_name>	Mark my-node as schedulable.
kubectl label node	Add a label to given node
