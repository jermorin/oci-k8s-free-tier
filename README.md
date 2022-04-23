# oci-k8s-free-tier

## Setup

1. Get the following data from your Oracle Cloud account
   - Compartment OCID
   - Region
1. Execute a `terraform init`
1. Execute a `terraform apply`
1. Create your Kubernetes configuration file using
   ```bash
   $ oci ce cluster create-kubeconfig --cluster-id <cluster OCID> --file ~/.kube/oci-k8s --region <region> --token-version 2.0.0 --kube-endpoint PUBLIC_ENDPOINT
   ```
1. Apply your K8S config for kubectl
   ```bash
   $ export KUBECONFIG=~/.kube/oci-k8s
   ```
1. To verify cluster access, do a `kubectl get nodes`
1. Enjoy 🍺
