# Kubernetes Architecture

## Control Plane
    - kube-apiserver: API gateway for all cluster operations
    - etcd: Distributed key-value store holding cluster state
    - scheduler: Assigns pods to nodes based on resource availablity
    - controller-manager: Ensures desired state is maintained

## Worker Nodes
    - kubelet: Node agent managing pod lifecycle
    - container runtime: Executes containers (CRI-O/Containerd)
    - kube-proxy: Manages networking rules

## Request Flow
    1. kubectl sends request to API server
    2. state stored in etcd
    3. scheduler selects node
    4. kubelet creates pod
    5. controller monitor and self-heal

