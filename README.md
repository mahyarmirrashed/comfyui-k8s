# ComfyUI for Kubernetes

Minimal Kubernetes deployment for running ComfyUI on a k3s cluster with NVIDIA
GPU acceleration and private access over Tailscale.

## Prerequisites

- NVIDIA GPU support configured via the NVIDIA GPU Operator (or equivalent
  device plugin).
- Tailscale Kubernetes operator installed and configured for cluster ingress.

## Deployment

If you have `kustomize` configured, from the repository root, apply the
kustomization in the `k8s/` directory:

```sh
kubectl apply -k k8s/
```

Otherwise, apply the manifests manually.

## Credit

This would not be possible without the work done by
[James Brink](https://github.com/jamesbrink) at
[utensils/comfyui-nix](https://github.com/utensils/comfyui-nix). Check out the
`flake.nix` that creates the image used in this repository,
