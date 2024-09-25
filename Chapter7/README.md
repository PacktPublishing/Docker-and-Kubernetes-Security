# Chapter 7

Here lies some files that complete the content written on Chapter 7 of the book "Docker and Kubernetes Security".

## Kubelet Config

The file `kubelet-config.yaml` is a more complete example of a config file for Kubelet.

### Key Components:

1.  **Network Settings**: The Kubelet listens on all interfaces (`0.0.0.0`) and serves HTTP requests on port `10250`.
2.  **Authentication & Authorization**: Anonymous access is disabled, and it uses a webhook and `x509` certificates for authentication.
3.  **TLS Configuration**: The TLS certificates for securing communication between Kubelet and other cluster components.
4.  **Eviction Thresholds**: Configures when to evict pods based on memory, disk space, and inodes.
5.  **Resource Limits**: Limits CPU and memory usage with policies for managing CPU and other resources.
6.  **Logging & Monitoring**: Includes logging settings and `cAdvisor` for monitoring system resources.
7.  **Volume and Plugin Management**: Manages storage through Container Storage Interface (CSI) migration.
8.  **Resource Reservations**: Ensures that certain resources (CPU, memory, and disk) are reserved for system and Kubernetes daemons.
9.  **Pod and Node Management**: Limits the maximum number of pods and the frequency of node status updates.