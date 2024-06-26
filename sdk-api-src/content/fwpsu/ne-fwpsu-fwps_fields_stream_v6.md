---
UID: NE:fwpsu.FWPS_FIELDS_STREAM_V6_
tech.root: fwp
title: FWPS_FIELDS_STREAM_V6
ms.date: 06/06/2024
targetos: Windows
description: Specifies the data field identifiers for the FWPS_LAYER_STREAM_V6 and FWPS_LAYER_STREAM_V6_DISCARD run-time filtering layers.
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
 - FWPS_FIELDS_STREAM_V6_
 - FWPS_FIELDS_STREAM_V6
f1_keywords:
 - FWPS_FIELDS_STREAM_V6_
 - fwpsu/FWPS_FIELDS_STREAM_V6_
 - FWPS_FIELDS_STREAM_V6
 - fwpsu/FWPS_FIELDS_STREAM_V6
dev_langs:
 - c++
helpviewer_keywords:
 - FWPS_FIELDS_STREAM_V6_
---

## -description

Specifies the data field identifiers for the [FWPS_LAYER_STREAM_V6](./ne-fwpsu-fwps_builtin_layers.md) and **FWPS_LAYER_STREAM_V6_DISCARD** run-time filtering layers.

## -enum-fields

### -field FWPS_FIELD_STREAM_V6_IP_LOCAL_ADDRESS

The local IP address.

### -field FWPS_FIELD_STREAM_V6_IP_LOCAL_ADDRESS_TYPE

The local IP address type. The possible values are defined by the
[NL_ADDRESS_TYPE](/windows/win32/api/nldef/ne-nldef-nl_address_type) enumeration.

### -field FWPS_FIELD_STREAM_V6_IP_REMOTE_ADDRESS

The remote IP address.

### -field FWPS_FIELD_STREAM_V6_IP_LOCAL_PORT

The local transport protocol port number.

### -field FWPS_FIELD_STREAM_V6_IP_REMOTE_PORT

The remote transport protocol port number.

### -field FWPS_FIELD_STREAM_V6_DIRECTION

The possible values are **FWP_DIRECTION_INBOUND** and **FWP_DIRECTION_OUTBOUND**.

### -field FWPS_FIELD_STREAM_V6_FLAGS

A bitwise OR of a combination of filtering condition flags. For information about the possible
flags, see [Filtering condition flags](/windows-hardware/drivers/network/filtering-condition-flags).

Supported in Windows Server 2008, Windows Vista SP1, and later versions of
Windows.

### -field FWPS_FIELD_STREAM_V6_COMPARTMENT_ID

The compartment that the network interface belongs to.

Supported starting with Windows 10, version 1703.

### -field FWPS_FIELD_STREAM_V6_MAX

The maximum value for this enumeration. This value might change in future versions of the NDIS
header files and binaries.

## -remarks

## -see-also
