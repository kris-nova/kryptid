# kyrptid

From the creators of [kubicorn](https://github.com/kubicorn/kubicorn) comes an exciting new adventure. The closest thing to Kubernetes from scratch.

An opinionated Kubernetes distribution specifically for Arch linux.

### bin

In here you will find many useful bash scripts for setting up kube.

```
# Used to bootstrap a new cluster
./bin/karch-init

# Used to provision CNI in a new cluster
./bin/karch-cni
```

### make

Here is the bulk of my work. Use the Makefile to build the Kubernetes components and start the systemd services.

```
make
sudo -E make install
sudo -E make enable start
```

### CNI

To destroy CNI virtual interfaces


```
ip link list
ip link destroy <interface>
```

### Nova todo

 - cilium install --ipam=kubernetes --helm-set endpointRoutes.enabled=true
 - Add cilium cli tool the Makefile
 - Add cilium --ipam kubernetes