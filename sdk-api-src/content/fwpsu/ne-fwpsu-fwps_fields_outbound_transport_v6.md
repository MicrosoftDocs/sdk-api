---
UID: NE:fwpsu.FWPS_FIELDS_OUTBOUND_TRANSPORT_V6_
tech.root: fwp
title: FWPS_FIELDS_OUTBOUND_TRANSPORT_V6
ms.date: 06/06/2024
targetos: Windows
description: Specifies the data field identifiers for the FWPS_LAYER_OUTBOUND_TRANSPORT_V6 and FWPS_LAYER_OUTBOUND_TRANSPORT_V6_DISCARD run-time filtering layers.
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
 - FWPS_FIELDS_OUTBOUND_TRANSPORT_V6_
 - FWPS_FIELDS_OUTBOUND_TRANSPORT_V6
f1_keywords:
 - FWPS_FIELDS_OUTBOUND_TRANSPORT_V6_
 - fwpsu/FWPS_FIELDS_OUTBOUND_TRANSPORT_V6_
 - FWPS_FIELDS_OUTBOUND_TRANSPORT_V6
 - fwpsu/FWPS_FIELDS_OUTBOUND_TRANSPORT_V6
dev_langs:
 - c++
helpviewer_keywords:
 - FWPS_FIELDS_OUTBOUND_TRANSPORT_V6_
---

## -description

Specifies the data field identifiers for the [FWPS_LAYER_OUTBOUND_TRANSPORT_V6](./ne-fwpsu-fwps_builtin_layers.md) and **FWPS_LAYER_OUTBOUND_TRANSPORT_V6_DISCARD** run-time filtering layers.

## -enum-fields


### -field FWPS_FIELD_OUTBOUND_TRANSPORT_V6_IP_PROTOCOL

The IP protocol number, as specified in RFC 1700.

### -field FWPS_FIELD_OUTBOUND_TRANSPORT_V6_IP_LOCAL_ADDRESS

The local IP address.

### -field FWPS_FIELD_OUTBOUND_TRANSPORT_V6_IP_LOCAL_ADDRESS_TYPE

The local IP address type. The possible values are defined by the
[NL_ADDRESS_TYPE](/windows/win32/api/nldef/ne-nldef-nl_address_type) enumeration.

### -field FWPS_FIELD_OUTBOUND_TRANSPORT_V6_IP_REMOTE_ADDRESS

The remote IP address.

### -field FWPS_FIELD_OUTBOUND_TRANSPORT_V6_IP_LOCAL_PORT

The local transport protocol port number.

### -field FWPS_FIELD_OUTBOUND_TRANSPORT_V6_IP_REMOTE_PORT

The remote transport protocol port number.

### -field FWPS_FIELD_OUTBOUND_TRANSPORT_V6_IP_LOCAL_INTERFACE

The locally unique identifier (LUID) for the network interface associated with the
local IP address.

### -field FWPS_FIELD_OUTBOUND_TRANSPORT_V6_INTERFACE_INDEX

The index of the logical network interface, as enumerated by the network stack.

### -field FWPS_FIELD_OUTBOUND_TRANSPORT_V6_SUB_INTERFACE_INDEX

The index of the logical network interface, as enumerated by the network stack.

### -field FWPS_FIELD_OUTBOUND_TRANSPORT_V6_IP_DESTINATION_ADDRESS_TYPE

The destination IP address type. The possible values are defined by the [NL_ADDRESS_TYPE](/windows/win32/api/nldef/ne-nldef-nl_address_type) enumeration.

### -field FWPS_FIELD_OUTBOUND_TRANSPORT_V6_FLAGS

A bitwise OR of a combination of filtering condition flags. For information about the possible
flags, see [Filtering condition flags](/windows-hardware/drivers/network/filtering-condition-flags).

Supported in Windows Server 2008, Windows Vista SP1, and later versions of
Windows.

### -field FWPS_FIELD_OUTBOUND_TRANSPORT_V6_INTERFACE_TYPE

The type of the arrival network interface, as defined by the Internet Assigned Numbers Authority
(IANA). For more information, see
[IANAifType-MIB Definitions](https://www.iana.org/assignments/ianaiftype-mib/ianaiftype-mib).

### -field FWPS_FIELD_OUTBOUND_TRANSPORT_V6_TUNNEL_TYPE

The encapsulation method used by a tunnel if the
*IfType* member of the **IP_ADAPTER_ADDRESSES** structure is **IF_TYPE_TUNNEL**. The tunnel type is defined
by IANA. For more information, see
[IANAifType-MIB Definitions](https://www.iana.org/assignments/ianaiftype-mib/ianaiftype-mib) and the
Windows SDK.

### -field FWPS_FIELD_OUTBOUND_TRANSPORT_V6_PROFILE_ID

The profile identifier (network category) of the network interface. The possible network category
values are: public (1), private (2), or domain (3).

Supported starting with Windows 7.

### -field FWPS_FIELD_OUTBOUND_TRANSPORT_V6_IPSEC_SECURITY_REALM_ID

The IPsec security realm identifier.

Supported starting with Windows 10.

### -field FWPS_FIELD_OUTBOUND_TRANSPORT_V6_COMPARTMENT_ID

The compartment that the network interface belongs to.

Supported starting with Windows 10, version 1703.

### -field FWPS_FIELD_OUTBOUND_TRANSPORT_V6_MAX

The maximum value for this enumeration. This value might change in future versions of the NDIS
header files and binaries.

## -remarks

## -see-also
