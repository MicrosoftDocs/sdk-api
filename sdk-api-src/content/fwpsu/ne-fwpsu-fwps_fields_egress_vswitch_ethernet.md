---
UID: NE:fwpsu.FWPS_FIELDS_EGRESS_VSWITCH_ETHERNET_
tech.root: fwp
title: FWPS_FIELDS_EGRESS_VSWITCH_ETHERNET
ms.date: 05/31/2024
targetos: Windows
description: Specifies the data field identifiers for the FWPS_LAYER_EGRESS_VSWITCH_ETHERNET run-time filtering layer.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: fwpsu.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
typedef_isUnnamed: false
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - fwpsu.h
api_name:
 - FWPS_FIELDS_EGRESS_VSWITCH_ETHERNET_
 - FWPS_FIELDS_EGRESS_VSWITCH_ETHERNET
f1_keywords:
 - FWPS_FIELDS_EGRESS_VSWITCH_ETHERNET_
 - fwpsu/FWPS_FIELDS_EGRESS_VSWITCH_ETHERNET_
 - FWPS_FIELDS_EGRESS_VSWITCH_ETHERNET
 - fwpsu/FWPS_FIELDS_EGRESS_VSWITCH_ETHERNET
dev_langs:
 - c++
helpviewer_keywords:
 - FWPS_FIELDS_EGRESS_VSWITCH_ETHERNET_
---

## -description

The **FWPS_FIELDS_EGRESS_VSWITCH_ETHERNET** (formerly **FWPS_FIELDS_EGRESS_VSWITCH_802_3**) enumeration type specifies the data field identifiers for the [FWPS_LAYER_EGRESS_VSWITCH_ETHERNET](./ne-fwpsu-fwps_builtin_layers.md) run-time filtering layer.

## -enum-fields

### -field FWPS_FIELD_EGRESS_VSWITCH_ETHERNET_MAC_SOURCE_ADDRESS

The virtual switch egress MAC source address field.

### -field FWPS_FIELD_EGRESS_VSWITCH_ETHERNET_MAC_SOURCE_ADDRESS_TYPE

The virtual switch egress MAC source address type field.

### -field FWPS_FIELD_EGRESS_VSWITCH_ETHERNET_MAC_DESTINATION_ADDRESS

The virtual switch egress MAC destination address field.

### -field FWPS_FIELD_EGRESS_VSWITCH_ETHERNET_MAC_DESTINATION_ADDRESS_TYPE

The virtual switch egress MAC destination address type field.

### -field FWPS_FIELD_EGRESS_VSWITCH_ETHERNET_ETHER_TYPE

The virtual switch egress Ethernet EtherType field.

### -field FWPS_FIELD_EGRESS_VSWITCH_ETHERNET_VLAN_ID

The virtual switch egress virtual LAN (VLAN) identifier field.

### -field FWPS_FIELD_EGRESS_VSWITCH_ETHERNET_VSWITCH_TENANT_NETWORK_ID

The virtual switch egress tenant network identifier field.

### -field FWPS_FIELD_EGRESS_VSWITCH_ETHERNET_VSWITCH_ID

The virtual switch egress Ethernet virtual switch identifier field.

### -field FWPS_FIELD_EGRESS_VSWITCH_ETHERNET_VSWITCH_NETWORK_TYPE

The virtual switch egress Ethernet virtual switch network type field.

### -field FWPS_FIELD_EGRESS_VSWITCH_ETHERNET_VSWITCH_SOURCE_INTERFACE_ID

The virtual switch egress Ethernet virtual switch source identifier field.

### -field FWPS_FIELD_EGRESS_VSWITCH_ETHERNET_VSWITCH_SOURCE_INTERFACE_TYPE

The virtual switch egress Ethernet virtual switch source interface type field.

### -field FWPS_FIELD_EGRESS_VSWITCH_ETHERNET_VSWITCH_SOURCE_VM_ID

TBD

### -field FWPS_FIELD_EGRESS_VSWITCH_ETHERNET_VSWITCH_DESTINATION_INTERFACE_ID

The virtual switch egress Ethernet virtual switch destination interface identifier field.

### -field FWPS_FIELD_EGRESS_VSWITCH_ETHERNET_VSWITCH_DESTINATION_INTERFACE_TYPE

The virtual switch egress Ethernet virtual switch destination interface type field.

### -field FWPS_FIELD_EGRESS_VSWITCH_ETHERNET_VSWITCH_DESTINATION_VM_ID

The virtual switch egress Ethernet virtual switch destination virtual machine (VM) identifier field.

### -field FWPS_FIELD_EGRESS_VSWITCH_ETHERNET_L2_FLAGS

A bitwise OR of Layer 2 (L2) flags. For a list of filtering condition flags, see [Filtering condition flags](/windows-hardware/drivers/network/filtering-condition-flags).

### -field FWPS_FIELD_EGRESS_VSWITCH_ETHERNET_COMPARTMENT_ID

The compartment that the network interface belongs to.

Supported starting with Windows 10, version 1703.

### -field FWPS_FIELD_EGRESS_VSWITCH_ETHERNET_MAX

The maximum value for this enumeration. This value might change in future versions of the NDIS header files and binaries.

## -remarks

## -see-also
