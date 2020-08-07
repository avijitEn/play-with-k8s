# play-with-k8s
https://labs.play-with-k8s.com/


git clone https://github.com/avijitEn/play-with-k8s.git
Cloning into 'play-with-k8s'...
remote: Enumerating objects: 9, done.
remote: Counting objects: 100% (9/9), done.
remote: Compressing objects: 100% (6/6), done.
remote: Total 9 (delta 1), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (9/9), done.

[node1 ~]$ cd play-with-k8s/
[node1 play-with-k8s]$ ll
total 8
-rw-r--r-- 1 root root  48 Aug  7 11:48 README.md
-rw-r--r-- 1 root root 335 Aug  7 11:48 play-with-k8s-clusterSetup.sh

[node1 play-with-k8s]$ chmod +x play-with-k8s-clusterSetup.sh
[node1 play-with-k8s]$ sh play-with-k8s-clusterSetup.sh
Initializing machine ID from random generator.
W0807 11:49:16.579329    1743 configset.go:202] WARNING: kubeadm cannot validate component configs for API groups [kubelet.config.k8s.io kubeproxy.config.k8s.io]
[init] Using Kubernetes version: v1.18.6
[preflight] Running pre-flight checks
        [WARNING Service-Docker]: docker service is not active, please run 'systemctl start docker.service'
        [WARNING IsDockerSystemdCheck]: detected "cgroupfs" as the Docker cgroup driver. The recommended driver is "systemd". Please follow the guide at https://kubernetes.io/docs/setup/cri/
        [WARNING FileContent--proc-sys-net-bridge-bridge-nf-call-iptables]: /proc/sys/net/bridge/bridge-nf-call-iptables does not exist
[preflight] The system verification failed. Printing the output from the verification:
KERNEL_VERSION: 4.4.0-177-generic
DOCKER_VERSION: 19.03.11
DOCKER_GRAPH_DRIVER: vfs
OS: Linux
CGROUPS_CPU: enabled
CGROUPS_CPUACCT: enabled
CGROUPS_CPUSET: enabled
CGROUPS_DEVICES: enabled
CGROUPS_FREEZER: enabled
CGROUPS_MEMORY: enabled
        [WARNING SystemVerification]: failed to parse kernel config: unable to load kernel module: "configs", output: "", err: exit status 1
        [WARNING SystemVerification]: unsupported graph driver: vfs
[preflight] Pulling images required for setting up a Kubernetes cluster
[preflight] This might take a minute or two, depending on the speed of your internet connection
You should now deploy a pod network to the cluster.
Run "kubectl apply -f [podnetwork].yaml" with one of the options listed at:
  https://kubernetes.io/docs/concepts/cluster-administration/addons/

Then you can join any number of worker nodes by running the following on each as root:

kubeadm join 192.168.0.23:6443 --token vyp926.zdd5n70rqn5073hs \
    --discovery-token-ca-cert-hash sha256:e67cb894fc569db3d9bcde638d49f32c8437886aa60f26e6f334877ee5be704d
