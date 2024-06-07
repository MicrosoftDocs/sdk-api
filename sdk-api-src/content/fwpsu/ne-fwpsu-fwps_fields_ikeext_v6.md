---
UID: NE:fwpsu.FWPS_FIELDS_IKEEXT_V6_
tech.root: fwp
title: FWPS_FIELDS_IKEEXT_V6
ms.date: 05/20/2024
targetos: Windows
description: Specifies the data field identifiers for the FWPS_LAYER_IKEEXT_V6 run-time filtering layer.
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
 - FWPS_FIELDS_IKEEXT_V6_
 - FWPS_FIELDS_IKEEXT_V6
f1_keywords:
 - FWPS_FIELDS_IKEEXT_V6_
 - fwpsu/FWPS_FIELDS_IKEEXT_V6_
 - FWPS_FIELDS_IKEEXT_V6
 - fwpsu/FWPS_FIELDS_IKEEXT_V6
dev_langs:
 - c++
helpviewer_keywords:
 - FWPS_FIELDS_IKEEXT_V6_
---

## -description

Specifies the data field identifiers for the [FWPS_LAYER_IKEEXT_V6](./ne-fwpsu-fwps_builtin_layers.md) run-time filtering layer.

## -enum-fields

### -field FWPS_FIELD_IKEEXT_V6_IP_LOCAL_ADDRESS

The local IP address.

### -field FWPS_FIELD_IKEEXT_V6_IP_REMOTE_ADDRESS

The remote IP address.

### -field FWPS_FIELD_IKEEXT_V6_IP_LOCAL_INTERFACE

The locally unique identifier (LUID) for the network interface associated with the local IP address.

### -field FWPS_FIELD_IKEEXT_V6_PROFILE_ID

The profile identifier (network category) of the network interface. The possible network category
values are: public (1), private (2), or domain (3).

Supported starting with Windows 7.

### -field FWPS_FIELD_IKEEXT_V6_IPSEC_SECURITY_REALM_ID

The IPsec security realm identifier.

Supported starting with Windows 10.

### -field FWPS_FIELD_IKEEXT_V6_MAX

The maximum value for this enumeration. This value might change in future versions of the NDIS
header files and binaries.

## -remarks

## -see-also
