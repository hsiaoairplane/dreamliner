💡 Use Kubernetes without relying on the container registry.

👨‍👨‍👦‍👦 User scenarios:
1. Deploy the YAML manifest with image equals to the Git repository. (Git repository URL + commit/tag/branch)
2. The operator/controller checks whether the related container image (commit/tag/branch) exists in the Kubernetes cluster.
   - If no, run an ephemeral container to build the container and distribute it to all the nodes
   - If yes, launch the Kubernetes resources with the corresponding container image
