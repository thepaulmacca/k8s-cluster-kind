# Kubernetes Cluster - Kind

## Overview

A Kubernetes cluster using [kind](./setup.sh). This will be regularly updated to use the default node image for each [release](https://github.com/kubernetes-sigs/kind/releases).

Using a local cluster is great for learning, experimentation and practice. It's also useful to have when you're studying for any of the Kubernetes certifications.

> [!NOTE]
> For the [CKS exam](https://training.linuxfoundation.org/certification/certified-kubernetes-security-specialist/), you'll have to create a bare-metal cluster due to limitations with kind. I've found the [cks-course-environment](https://github.com/killer-sh/cks-course-environment/tree/master) repo to be sufficient, although you'll need to tweak it as per the new curriculum.

## Getting Started

### Single Node Cluster

Run `chmod +x setup.sh` and then `./setup.sh` to install a single-node cluster (default).

### Multi-Node Cluster

Run `./setup.sh multi-node.yaml` to install a multi-node cluster (one control plane and 2 worker nodes).

## Installed Software

The `setup.sh` script installs:

- Calico for testing Network Policies
- NGINX Ingress Controller

All other software is currently installed using a [helmfile](helmfile.yaml).
