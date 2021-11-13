# Network-Driver

Because the driver does not require  any hardware interactions (software only),  it is easier to understand the technical interface and the usage of various NDIS functions 
without the confusion of hardware-specific code that is normally the case of in a functional driver.

The driver can be installed either manually with the Add Hardware wizard or on a virtual bus (like a toaster bus).

If a single instance of the virtual Miniport exists, it would drop the send packets and complete the send operation until it finishes. 
If there are multiple virtual Miniport instances, the instances behave as if they were multiple network interface cards (NICs) connected into a single Ethernet hub.
This "hub" indicates the incoming send packets to all of the virtual Miniport instances.
