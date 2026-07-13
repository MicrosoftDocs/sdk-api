---
UID: NE:fwpsu.FWPS_FIELDS_STREAM_PACKET_V4_
tech.root: fwp
title: FWPS_FIELDS_STREAM_PACKET_V4
ms.date: 06/06/2024
targetos: Windows
description: Specifies the data field identifiers for the FWPS_LAYER_STREAM_PACKET_V4 run-time filtering layer.
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
 - FWPS_FIELDS_STREAM_PACKET_V4_
 - FWPS_FIELDS_STREAM_PACKET_V4
f1_keywords:
 - FWPS_FIELDS_STREAM_PACKET_V4_
 - fwpsu/FWPS_FIELDS_STREAM_PACKET_V4_
 - FWPS_FIELDS_STREAM_PACKET_V4
 - fwpsu/FWPS_FIELDS_STREAM_PACKET_V4
dev_langs:
 - c++
helpviewer_keywords:
 - FWPS_FIELDS_STREAM_PACKET_V4_
---

## -description

Specifies the data field identifiers for the [FWPS_LAYER_STREAM_PACKET_V4](./ne-fwpsu-fwps_builtin_layers.md) run-time filtering layer.

## -enum-fields

### -field FWPS_FIELD_STREAM_PACKET_V4_IP_LOCAL_ADDRESS

The local IP address.

### -field FWPS_FIELD_STREAM_PACKET_V4_IP_REMOTE_ADDRESS

The remote IP address.

### -field FWPS_FIELD_STREAM_PACKET_V4_IP_LOCAL_PORT

The local transport protocol port number.

### -field FWPS_FIELD_STREAM_PACKET_V4_IP_REMOTE_PORT

The remote transport protocol port number.

### -field FWPS_FIELD_STREAM_PACKET_V4_IP_LOCAL_INTERFACE

The locally unique identifier (LUID) for the network interface associated with the
local IP address.

### -field FWPS_FIELD_STREAM_PACKET_V4_INTERFACE_INDEX

The index of the network interface, as enumerated by the network stack.

### -field FWPS_FIELD_STREAM_PACKET_V4_SUB_INTERFACE_INDEX

The index of the logical network interface, as enumerated by the network stack.

### -field FWPS_FIELD_STREAM_PACKET_V4_DIRECTION

The possible values are **FWP_DIRECTION_INBOUND** and **FWP_DIRECTION_OUTBOUND**.

### -field FWPS_FIELD_STREAM_PACKET_V4_FLAGS

A bitwise OR of a combination of filtering condition flags. For information about the possible
flags, see [Filtering condition flags](/windows-hardware/drivers/network/filtering-condition-flags).

### -field FWPS_FIELD_STREAM_PACKET_V4_INTERFACE_TYPE

The type of the arrival network interface, as defined by the Internet Assigned Numbers Authority
(IANA). For more information, see
IANAifType-MIB Definitions.

### -field FWPS_FIELD_STREAM_PACKET_V4_TUNNEL_TYPE

The encapsulation method used by a tunnel if the
*IfType* member of the **IP_ADAPTER_ADDRESSES** structure is **IF_TYPE_TUNNEL**. The tunnel type is defined
by IANA. For more information, see
[IANAifType-MIB Definitions](https://www.iana.org/assignments/ianaiftype-mib/ianaiftype-mib) and the
Windows SDK.

### -field FWPS_FIELD_STREAM_PACKET_V4_COMPARTMENT_ID

The compartment that the network interface belongs to.

Supported starting with Windows 10, version 1703.

### -field FWPS_FIELD_STREAM_PACKET_V4_MAX

The maximum value for this enumeration. This value might change in future versions of the NDIS
header files and binaries.

## -remarks

## -see-also
