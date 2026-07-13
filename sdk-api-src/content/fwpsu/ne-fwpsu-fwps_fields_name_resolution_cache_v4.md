---
UID: NE:fwpsu.FWPS_FIELDS_NAME_RESOLUTION_CACHE_V4_
tech.root: fwp
title: FWPS_FIELDS_NAME_RESOLUTION_CACHE_V4
ms.date: 06/05/2024
targetos: Windows
description: Specifies the data field identifiers for the FWPS_LAYER_NAME_RESOLUTION_CACHE_V4 run-time filtering layer.
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
 - FWPS_FIELDS_NAME_RESOLUTION_CACHE_V4_
 - FWPS_FIELDS_NAME_RESOLUTION_CACHE_V4
f1_keywords:
 - FWPS_FIELDS_NAME_RESOLUTION_CACHE_V4_
 - fwpsu/FWPS_FIELDS_NAME_RESOLUTION_CACHE_V4_
 - FWPS_FIELDS_NAME_RESOLUTION_CACHE_V4
 - fwpsu/FWPS_FIELDS_NAME_RESOLUTION_CACHE_V4
dev_langs:
 - c++
helpviewer_keywords:
 - FWPS_FIELDS_NAME_RESOLUTION_CACHE_V4_
---

## -description

Specifies the data field identifiers for the [FWPS_LAYER_NAME_RESOLUTION_CACHE_V4](./ne-fwpsu-fwps_builtin_layers.md) run-time filtering layer.

## -enum-fields

### -field FWPS_FIELD_NAME_RESOLUTION_CACHE_V4_ALE_USER_ID

The identifier of the local user.

### -field FWPS_FIELD_NAME_RESOLUTION_CACHE_V4_ALE_APP_ID

The full path of the application.

### -field FWPS_FIELD_NAME_RESOLUTION_CACHE_V4_IP_REMOTE_ADDRESS

The remote IP address.

### -field FWPS_FIELD_NAME_RESOLUTION_CACHE_V4_PEER_NAME

The machine name that is associated with the destination IP address.

### -field FWPS_FIELD_NAME_RESOLUTION_CACHE_V4_COMPARTMENT_ID

The compartment that the network interface belongs to.

Supported starting with Windows 10, version 1703.

### -field FWPS_FIELD_NAME_RESOLUTION_CACHE_V4_MAX

The maximum value for this enumeration. This value might change in future versions of the NDIS
header files and binaries.

## -remarks

## -see-also
