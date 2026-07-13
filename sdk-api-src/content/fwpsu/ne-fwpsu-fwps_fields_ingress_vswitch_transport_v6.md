---
UID: NE:fwpsu.FWPS_FIELDS_INGRESS_VSWITCH_TRANSPORT_V6_
tech.root: fwp
title: FWPS_FIELDS_INGRESS_VSWITCH_TRANSPORT_V6
ms.date: 06/04/2024
targetos: Windows
description: Specifies the data field identifiers for the FWPS_LAYER_INGRESS_VSWITCH_TRANSPORT_V6 run-time filtering layer.
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
 - FWPS_FIELDS_INGRESS_VSWITCH_TRANSPORT_V6_
 - FWPS_FIELDS_INGRESS_VSWITCH_TRANSPORT_V6
f1_keywords:
 - FWPS_FIELDS_INGRESS_VSWITCH_TRANSPORT_V6_
 - fwpsu/FWPS_FIELDS_INGRESS_VSWITCH_TRANSPORT_V6_
 - FWPS_FIELDS_INGRESS_VSWITCH_TRANSPORT_V6
 - fwpsu/FWPS_FIELDS_INGRESS_VSWITCH_TRANSPORT_V6
dev_langs:
 - c++
helpviewer_keywords:
 - FWPS_FIELDS_INGRESS_VSWITCH_TRANSPORT_V6_
---

## -description

Specifies the data field identifiers for the [FWPS_LAYER_INGRESS_VSWITCH_TRANSPORT_V6](./ne-fwpsu-fwps_builtin_layers.md) run-time filtering layer.

## -enum-fields

### -field FWPS_FIELD_INGRESS_VSWITCH_TRANSPORT_V6_IP_SOURCE_ADDRESS

The virtual switch ingress IP source address field.

### -field FWPS_FIELD_INGRESS_VSWITCH_TRANSPORT_V6_IP_DESTINATION_ADDRESS

The virtual switch ingress IP destination address field.

### -field FWPS_FIELD_INGRESS_VSWITCH_TRANSPORT_V6_IP_PROTOCOL

The virtual switch ingress IP protocol field.

### -field FWPS_FIELD_INGRESS_VSWITCH_TRANSPORT_V6_IP_SOURCE_PORT

The virtual switch ingress IP source port field.

### -field FWPS_FIELD_INGRESS_VSWITCH_TRANSPORT_V6_IP_DESTINATION_PORT

The virtual switch ingress IP destination port field.

### -field FWPS_FIELD_INGRESS_VSWITCH_TRANSPORT_V6_VLAN_ID

The virtual switch ingress virtual LAN (VLAN) identifier field.

### -field FWPS_FIELD_INGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_TENANT_NETWORK_ID

The virtual switch ingress virtual switch tenant network identifier field.

### -field FWPS_FIELD_INGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_ID

The virtual switch ingress virtual switch identifier field.

### -field FWPS_FIELD_INGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_NETWORK_TYPE

The virtual switch ingress virtual switch network type field.

### -field FWPS_FIELD_INGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_SOURCE_INTERFACE_ID

The virtual switch ingress virtual switch source interface identifier field.

### -field FWPS_FIELD_INGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_SOURCE_INTERFACE_TYPE

The virtual switch ingress virtual switch source interface type field.

### -field FWPS_FIELD_INGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_SOURCE_VM_ID

The virtual switch ingress virtual switch source virtual machine (VM) identifier field.

### -field FWPS_FIELD_INGRESS_VSWITCH_TRANSPORT_V6_L2_FLAGS

A bitwise OR of Layer 2 (L2) flags. For a list of filtering condition flags, see [Filtering condition flags](/windows-hardware/drivers/network/filtering-condition-flags).

### -field FWPS_FIELD_INGRESS_VSWITCH_TRANSPORT_V6_COMPARTMENT_ID

The compartment that the network interface belongs to.

Supported starting with Windows 10, version 1703.

### -field FWPS_FIELD_INGRESS_VSWITCH_TRANSPORT_V6_MAX

The maximum value for this enumeration. This value might change in future versions of the NDIS header files and binaries.

## -remarks

## -see-also
