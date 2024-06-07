---
UID: NE:fwpsu.FWPS_FIELDS_DATAGRAM_DATA_V6_
tech.root: fwp
title: FWPS_FIELDS_DATAGRAM_DATA_V6
ms.date: 05/30/2024
targetos: Windows
description: Specifies the data field identifiers for the FWPS_LAYER_ALE_RESOURCE_ASSIGNMENT_V6 and FWPS_LAYER_ALE_RESOURCE_ASSIGNMENT_V6_DISCARD run-time filtering layers.
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
 - FWPS_FIELDS_DATAGRAM_DATA_V6_
 - FWPS_FIELDS_DATAGRAM_DATA_V6
f1_keywords:
 - FWPS_FIELDS_DATAGRAM_DATA_V6_
 - fwpsu/FWPS_FIELDS_DATAGRAM_DATA_V6_
 - FWPS_FIELDS_DATAGRAM_DATA_V6
 - fwpsu/FWPS_FIELDS_DATAGRAM_DATA_V6
dev_langs:
 - c++
helpviewer_keywords:
 - FWPS_FIELDS_DATAGRAM_DATA_V6_
---

## -description

Specifies the data field identifiers for the [FWPS_LAYER_ALE_RESOURCE_ASSIGNMENT_V6](./ne-fwpsu-fwps_builtin_layers.md) and **FWPS_LAYER_ALE_RESOURCE_ASSIGNMENT_V6_DISCARD** run-time filtering layers.

## -enum-fields

### -field FWPS_FIELD_DATAGRAM_DATA_V6_IP_PROTOCOL

The IP protocol number, as specified in RFC 1700.

### -field FWPS_FIELD_DATAGRAM_DATA_V6_IP_LOCAL_ADDRESS

The local IP address.

### -field FWPS_FIELD_DATAGRAM_DATA_V6_IP_REMOTE_ADDRESS

The remote IP address.

### -field FWPS_FIELD_DATAGRAM_DATA_V6_IP_LOCAL_ADDRESS_TYPE

The local IP address type. The possible values are defined by the [NL_ADDRESS_TYPE](/windows/win32/api/nldef/ne-nldef-nl_address_type) enumeration.

### -field FWPS_FIELD_DATAGRAM_DATA_V6_IP_LOCAL_PORT

The local transport protocol port number.

### -field FWPS_FIELD_DATAGRAM_DATA_V6_IP_REMOTE_PORT

The remote transport protocol port number.

### -field FWPS_FIELD_DATAGRAM_DATA_V6_IP_LOCAL_INTERFACE

The locally unique identifier (LUID) for the network interface associated with the local IP address.

### -field FWPS_FIELD_DATAGRAM_DATA_V6_NEXTHOP_INTERFACE_INDEX

The index of the network interface that will be used to continue forwarding of the outbound
packet, as enumerated by the network stack.

Supported in Windows Server 2008, Windows Vista SP1, and later versions of
Windows.

### -field FWPS_FIELD_DATAGRAM_DATA_V6_SUB_INTERFACE_INDEX

The index of the network subinterface, as enumerated by the network stack.

Supported in Windows Server 2008, Windows Vista SP1, and later versions of
Windows.

### -field FWPS_FIELD_DATAGRAM_DATA_V6_DIRECTION

The possible values are **FWP_DIRECTION_INBOUND** and **FWP_DIRECTION_OUTBOUND**.

### -field FWPS_FIELD_DATAGRAM_DATA_V6_FLAGS

A bitwise OR of a combination of filtering condition flags. For information about the possible
flags, see [Filtering condition flags](/windows-hardware/drivers/network/filtering-condition-flags).

### -field FWPS_FIELD_DATAGRAM_DATA_V6_INTERFACE_TYPE

The type of the local network interface, as defined by the Internet Assigned Numbers Authority
(IANA). For more information, see
[IANAifType-MIB Definitions](https://www.iana.org/assignments/ianaiftype-mib/ianaiftype-mib).

### -field FWPS_FIELD_DATAGRAM_DATA_V6_TUNNEL_TYPE

The encapsulation method used by a tunnel if the
*IfType* member of the **IP_ADAPTER_ADDRESSES** structure is **IF_TYPE_TUNNEL**. The tunnel type is defined
by IANA. For more information, see
[IANAifType-MIB Definitions](https://www.iana.org/assignments/ianaiftype-mib/ianaiftype-mib) and the
Windows SDK.

### -field FWPS_FIELD_DATAGRAM_DATA_V6_COMPARTMENT_ID

The compartment that the network interface belongs to.

Supported starting with Windows 10, version 1703.

### -field FWPS_FIELD_DATAGRAM_DATA_V6_MAX

The maximum value for this enumeration. This value might change in future versions of the Network Driver Interface Specification (NDIS) header files and binaries.

## -remarks

The following macros in `fwpsu.h` are defined with **FWPS_FIELDS_DATAGRAM_DATA_V6** enumeration values:

```cpp
#define FWPS_FIELD_DATAGRAM_DATA_V6_ICMP_TYPE \
        FWPS_FIELD_DATAGRAM_DATA_V6_IP_LOCAL_PORT

#define FWPS_FIELD_DATAGRAM_DATA_V6_ICMP_CODE \
        FWPS_FIELD_DATAGRAM_DATA_V6_IP_REMOTE_PORT
```

Those macros are used to access the following IPV6 data fields:

FWPS_FIELD_DATAGRAM_DATA_V6_ICMP_TYPE

The ICMP type field, as specified in RFC 792.

FWPS_FIELD_DATAGRAM_DATA_V6_ICMP_CODE

The ICMP code field, as specified in RFC 792.

## -see-also
