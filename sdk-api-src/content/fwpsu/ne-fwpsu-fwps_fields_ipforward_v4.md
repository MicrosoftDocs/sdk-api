---
UID: NE:fwpsu.FWPS_FIELDS_IPFORWARD_V4_
tech.root: fwp
title: FWPS_FIELDS_IPFORWARD_V4
ms.date: 06/05/2024
targetos: Windows
description: Specifies the data field identifiers for the FWPS_LAYER_IPFORWARD_V4 and FWPS_LAYER_IPFORWARD_V4_DISCARD run-time filtering layers.
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
 - FWPS_FIELDS_IPFORWARD_V4_
 - FWPS_FIELDS_IPFORWARD_V4
f1_keywords:
 - FWPS_FIELDS_IPFORWARD_V4_
 - fwpsu/FWPS_FIELDS_IPFORWARD_V4_
 - FWPS_FIELDS_IPFORWARD_V4
 - fwpsu/FWPS_FIELDS_IPFORWARD_V4
dev_langs:
 - c++
helpviewer_keywords:
 - FWPS_FIELDS_IPFORWARD_V4_
---

## -description

Specifies the data field identifiers for the [FWPS_LAYER_IPFORWARD_V4](./ne-fwpsu-fwps_builtin_layers.md) and **FWPS_LAYER_IPFORWARD_V4_DISCARD** run-time filtering layers.

## -enum-fields

### -field FWPS_FIELD_IPFORWARD_V4_IP_SOURCE_ADDRESS

The source IP address.

### -field FWPS_FIELD_IPFORWARD_V4_IP_DESTINATION_ADDRESS

The destination IP address.

### -field FWPS_FIELD_IPFORWARD_V4_IP_DESTINATION_ADDRESS_TYPE

The destination IP address type. The possible values are defined by the [NL_ADDRESS_TYPE](/windows/win32/api/nldef/ne-nldef-nl_address_type) enumeration.

### -field FWPS_FIELD_IPFORWARD_V4_IP_LOCAL_INTERFACE

The locally unique identifier (LUID) for the network interface associated with the
local IP address.

### -field FWPS_FIELD_IPFORWARD_V4_IP_FORWARD_INTERFACE

The LUID for the network interface on which the packet being forwarded is to be sent out.

### -field FWPS_FIELD_IPFORWARD_V4_SOURCE_INTERFACE_INDEX

The index of the source network interface, as enumerated by the network stack.

### -field FWPS_FIELD_IPFORWARD_V4_SOURCE_SUB_INTERFACE_INDEX

The index of the source logical network interface, as enumerated by the network stack.

### -field FWPS_FIELD_IPFORWARD_V4_DESTINATION_INTERFACE_INDEX

The index of the destination network interface, as enumerated by the network stack.

### -field FWPS_FIELD_IPFORWARD_V4_DESTINATION_SUB_INTERFACE_INDEX

The index of the destination logical network interface, as enumerated by the network stack.

### -field FWPS_FIELD_IPFORWARD_V4_FLAGS

A bitwise OR of a combination of filtering condition flags. For information about the possible flags, see [Filtering condition flags](/windows-hardware/drivers/network/filtering-condition-flags).

### -field FWPS_FIELD_IPFORWARD_V4_IP_PHYSICAL_ARRIVAL_INTERFACE

The LUID for the physical network interface that the packet first arrived on.

Supported starting with Windows 7.

### -field FWPS_FIELD_IPFORWARD_V4_ARRIVAL_INTERFACE_PROFILE_ID

The profile identifier (network category) of the arrival interface. The possible network category
values are: public (1), private (2), or domain (3).

Supported starting with Windows 7.

### -field FWPS_FIELD_IPFORWARD_V4_IP_PHYSICAL_NEXTHOP_INTERFACE

The LUID for the physical network interface that will be used to continue forwarding of the outbound packet.

Supported starting with Windows 7.

### -field FWPS_FIELD_IPFORWARD_V4_NEXTHOP_INTERFACE_PROFILE_ID

The profile identifier (network category) of the next-hop interface. The possible network category
values are: public (1), private (2), or domain (3).

Supported starting with Windows 7.

### -field FWPS_FIELD_IPFORWARD_V4_COMPARTMENT_ID

The compartment that the network interface belongs to.

Supported starting with Windows 10, version 1703.

### -field FWPS_FIELD_IPFORWARD_V4_MAX

The maximum value for this enumeration. This value might change in future versions of the NDIS
header files and binaries.

## -remarks

## -see-also
