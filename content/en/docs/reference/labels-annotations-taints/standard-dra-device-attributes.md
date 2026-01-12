---
title: Standard DRA Device Attributes 
weight: 10
---

<!-- overview -->

Kubernetes reserves all DRA device attribute names in the `kubernetes.io` namespace.

This document serves both as a reference to the values and as a coordination point

for assigning values.

<!-- body -->

## DRA Device Attributes

### resource.kubernetes.io/pcieRoot

Type: Device Attribute

Example: `resource.kubernetes.io/pcieRoot: {"stringValue": "pci0000:1a"}`

Used in: ResourceSlice

Used to describe the PCIe (Peripheral Component Interconnect Express) Root Complex
of a PCI device. This attribute MAY be implemented by DRA drivers to enable
identification of devices that share the same PCIe root complex. A value for this
device attribute must be in the format `pci<domain>:<bus>`.

### resource.kubernetes.io/pciBusID

Type: Device Attribute

Example: `resource.kubernetes.io/pciBusID: {"stringValue": "0000:00:01.0"}`

Used in: ResourceSlice

Used to describe the PCI (Peripheral Component Interconnect) Bus Address of a
PCI device. This attribute MAY be implemented by DRA drivers to identify PCI devices.
A value for this device attribute must be in the extended BDF format
(<socket>:<bus>:<domain>.<function>).