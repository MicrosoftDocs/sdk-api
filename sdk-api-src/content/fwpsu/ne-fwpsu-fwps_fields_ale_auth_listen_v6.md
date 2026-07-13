---
UID: NE:fwpsu.FWPS_FIELDS_ALE_AUTH_LISTEN_V6_
tech.root: fwp
title: FWPS_FIELDS_ALE_AUTH_LISTEN_V6
ms.date: 05/29/2024
targetos: Windows
description: Specifies the data field identifiers for the FWPS_LAYER_ALE_AUTH_LISTEN_V6 and FWPS_LAYER_ALE_AUTH_LISTEN_V6_DISCARD run-time filtering layers.
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
 - FWPS_FIELDS_ALE_AUTH_LISTEN_V6_
 - FWPS_FIELDS_ALE_AUTH_LISTEN_V6
f1_keywords:
 - FWPS_FIELDS_ALE_AUTH_LISTEN_V6_
 - fwpsu/FWPS_FIELDS_ALE_AUTH_LISTEN_V6_
 - FWPS_FIELDS_ALE_AUTH_LISTEN_V6
 - fwpsu/FWPS_FIELDS_ALE_AUTH_LISTEN_V6
dev_langs:
 - c++
helpviewer_keywords:
 - FWPS_FIELDS_ALE_AUTH_LISTEN_V6_
---

## -description

Specifies the data field identifiers for the [FWPS_LAYER_ALE_AUTH_LISTEN_V6](./ne-fwpsu-fwps_builtin_layers.md) and **FWPS_LAYER_ALE_AUTH_LISTEN_V6_DISCARD** run-time filtering layers.

## -enum-fields

### -field FWPS_FIELD_ALE_AUTH_LISTEN_V6_ALE_APP_ID

The full path of the application.

### -field FWPS_FIELD_ALE_AUTH_LISTEN_V6_ALE_USER_ID

The identifier of the local user.

### -field FWPS_FIELD_ALE_AUTH_LISTEN_V6_IP_LOCAL_ADDRESS

The local IP address.

### -field FWPS_FIELD_ALE_AUTH_LISTEN_V6_IP_LOCAL_ADDRESS_TYPE

The local IP address type. The possible values are defined by the [NL_ADDRESS_TYPE](/windows/win32/api/nldef/ne-nldef-nl_address_type) enumeration.

### -field FWPS_FIELD_ALE_AUTH_LISTEN_V6_IP_LOCAL_PORT

The local transport protocol port number.

### -field FWPS_FIELD_ALE_AUTH_LISTEN_V6_IP_LOCAL_INTERFACE

The locally unique identifier (LUID) for the network interface associated with the local IP address.

### -field FWPS_FIELD_ALE_AUTH_LISTEN_V6_FLAGS

A bitwise OR of a combination of filtering condition flags. For information about the possible
flags, see [Filtering condition flags](/windows-hardware/drivers/network/filtering-condition-flags).

### -field FWPS_FIELD_ALE_AUTH_LISTEN_V6_INTERFACE_TYPE

The type of the local network interface, as defined by the Internet Assigned Numbers Authority
(IANA). For more information, see
[IANAifType-MIB Definitions](https://www.iana.org/assignments/ianaiftype-mib/ianaiftype-mib).

### -field FWPS_FIELD_ALE_AUTH_LISTEN_V6_TUNNEL_TYPE

The encapsulation method used by a tunnel if the
*IfType* member of the **IP_ADAPTER_ADDRESSES** structure is **IF_TYPE_TUNNEL**. The tunnel type is defined
by IANA. For more information, see
[IANAifType-MIB Definitions](https://www.iana.org/assignments/ianaiftype-mib/ianaiftype-mib) and the
Windows SDK.

### -field FWPS_FIELD_ALE_AUTH_LISTEN_V6_LOCAL_INTERFACE_PROFILE_ID

The profile identifier (network category) of the network interface associated with the local IP
address. The possible network category values are: public (1), private (2), or domain (3).

Supported starting with Windows 7.

### -field FWPS_FIELD_ALE_AUTH_LISTEN_V6_SIO_FIREWALL_SOCKET_PROPERTY

The **IP_PROTECTION_LEVEL** property associated with the socket.

Supported starting with Windows 7.

### -field FWPS_FIELD_ALE_AUTH_LISTEN_V6_ALE_PACKAGE_ID

The package identifier is a security identifier (SID) that identifies the associated AppContainer process. For more information about the SID structure, see the description for the SID structure in the Microsoft Windows SDK documentation.

Supported starting with Windows 8.

### -field FWPS_FIELD_ALE_AUTH_LISTEN_V6_ALE_SECURITY_ATTRIBUTE_FQBN_VALUE

TBD

Supported starting with Windows 10.

### -field FWPS_FIELD_ALE_AUTH_LISTEN_V6_COMPARTMENT_ID

The compartment that the network interface belongs to.

Supported starting with Windows 10, version 1703.

### -field FWPS_FIELD_ALE_AUTH_LISTEN_V6_PACKAGE_FAMILY_NAME

Indicates that the resource is a Package Family Name string.

Supported starting with Windows Server 2022 23H2.

### -field FWPS_FIELD_ALE_AUTH_LISTEN_V6_MAX

The maximum value for this enumeration. This value might change in future versions of the Network Driver Interface Specification (NDIS) header files and binaries.

## -remarks

## -see-also
