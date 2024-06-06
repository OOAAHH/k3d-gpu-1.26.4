# k3d-gpu
custom k3d image to run cuda workloads

Original Docs: https://k3d.io/v5.3.0/usage/advanced/cuda/
- The example code in the official docs is out of date

Modification: https://github.com/k3d-io/k3d/issues/1108
- Applied modifications from the GitHub issue to make the build working.

# result
vlatitude/k3d-gpu/rancher/k3s:v1.26.4-k3s1-cuda 

k3d集群调用GPU需要专属镜像，构建了单一节点使用的image，

`k3d cluster create "kubeflow" \
  --image "vlatitude/k3d-gpu/rancher/k3s:v1.26.4-k3s1-cuda" \
  --volume '/home/sunhao:/home/sunhao@all' \
  --port '8080:80@loadbalancer' \
  --gpus all`
