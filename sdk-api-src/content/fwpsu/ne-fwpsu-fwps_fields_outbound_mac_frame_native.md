---
UID: NE:fwpsu.FWPS_FIELDS_OUTBOUND_MAC_FRAME_NATIVE_
tech.root: fwp
title: FWPS_FIELDS_OUTBOUND_MAC_FRAME_NATIVE
ms.date: 06/05/2024
targetos: Windows
description: Specifies the data field identifiers for the FWPS_LAYER_OUTBOUND_MAC_FRAME_NATIVE run-time filtering layer.
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
 - FWPS_FIELDS_OUTBOUND_MAC_FRAME_NATIVE_
 - FWPS_FIELDS_OUTBOUND_MAC_FRAME_NATIVE
f1_keywords:
 - FWPS_FIELDS_OUTBOUND_MAC_FRAME_NATIVE_
 - fwpsu/FWPS_FIELDS_OUTBOUND_MAC_FRAME_NATIVE_
 - FWPS_FIELDS_OUTBOUND_MAC_FRAME_NATIVE
 - fwpsu/FWPS_FIELDS_OUTBOUND_MAC_FRAME_NATIVE
dev_langs:
 - c++
helpviewer_keywords:
 - FWPS_FIELDS_OUTBOUND_MAC_FRAME_NATIVE_
---

## -description

Specifies the data field identifiers for the [FWPS_LAYER_OUTBOUND_MAC_FRAME_NATIVE](./ne-fwpsu-fwps_builtin_layers.md) run-time filtering layer.

## -enum-fields

### -field FWPS_FIELD_OUTBOUND_MAC_FRAME_NATIVE_NDIS_MEDIA_TYPE

The outbound MAC frame native NDIS media type field.

### -field FWPS_FIELD_OUTBOUND_MAC_FRAME_NATIVE_NDIS_PHYSICAL_MEDIA_TYPE

The outbound MAC frame native NDIS physical media type field.

### -field FWPS_FIELD_OUTBOUND_MAC_FRAME_NATIVE_INTERFACE

The outbound MAC frame native interface field.

### -field FWPS_FIELD_OUTBOUND_MAC_FRAME_NATIVE_INTERFACE_TYPE

The outbound MAC frame native interface type field.

### -field FWPS_FIELD_OUTBOUND_MAC_FRAME_NATIVE_INTERFACE_INDEX

The outbound MAC frame native interface index field.

### -field FWPS_FIELD_OUTBOUND_MAC_FRAME_NATIVE_NDIS_PORT

The outbound MAC frame native NDIS port field.

### -field FWPS_FIELD_OUTBOUND_MAC_FRAME_NATIVE_L2_FLAGS

A bitwise OR of Layer 2 (L2) flags. For a list of filtering condition flags, see [Filtering condition flags](/windows-hardware/drivers/network/filtering-condition-flags).

### -field FWPS_FIELD_OUTBOUND_MAC_FRAME_NATIVE_COMPARTMENT_ID

The compartment that the network interface belongs to.

Supported starting with Windows 10, version 1703.

### -field FWPS_FIELD_OUTBOUND_MAC_FRAME_NATIVE_MAX

The maximum value for this enumeration. This value might change in future versions of the NDIS
header files and binaries.

## -remarks

## -see-also
