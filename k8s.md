# reasons for pod failure
##  Common Causes for  Kubernetes Pod Starting Errors
 * Insufficient Resources: ...
* Image Pulling Issues: ...
*  Networking Problems: ...
* Pod Scheduling Constraints: ...
* Failed Readiness Probes: ...
* Unhealthy Container: ...
* Persistent Volume Mount Failures: ...
* Invalid Pod Configuration:



# restriction to pod to pod communication
## How to restrict Inter Pod communication ?
 * The solution is to use ‘Network Policies’. Networkpolicies can be used to restrict network traffic between pods and enforce security policies.
 ## Network Policies
 * Within a Kubernetes cluster, all Pod to Pod communication is allowed by default. This may cause a major impact if one of the pods gets compromised, all other pods within the namespace can also be compromised since it is allowed to communicate.
 ## Before applying any network policies in the cluster, identify the following.
 * podSelector: For specifying the set of pods.
 * policyTypes: Define Ingress/Egress.
 * from: Incoming traffic that should be allowed or blocked. You can define the source based on IP addresses, pods, or namespaces.
* to: Destination of outgoing traffic that should be allowed or blocked. You can define the destination based on IP addresses, pods,or namespaces.
* port: Port numbers and protocols.
## To list the available networkPolicy in the cluster
* kubectl get networkpolicies — all-namespaces
