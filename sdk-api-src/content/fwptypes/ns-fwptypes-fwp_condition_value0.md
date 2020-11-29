---
UID: NS:fwptypes.FWP_CONDITION_VALUE0_
title: FWP_CONDITION_VALUE0 (fwptypes.h)
description: Contains values that are used in filter conditions when testing for matching filters.
helpviewer_keywords: ["FWP_CONDITION_VALUE0","FWP_CONDITION_VALUE0 structure [Filtering]","fwp.fwp_condition_value0","fwptypes/FWP_CONDITION_VALUE0"]
old-location: fwp\fwp_condition_value0.htm
tech.root: fwp
ms.assetid: edc34005-dbc1-45a4-b6c7-fbb8b13fa388
ms.date: 12/05/2018
ms.keywords: FWP_CONDITION_VALUE0, FWP_CONDITION_VALUE0 structure [Filtering], fwp.fwp_condition_value0, fwptypes/FWP_CONDITION_VALUE0
req.header: fwptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwptypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FWP_CONDITION_VALUE0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWP_CONDITION_VALUE0_
 - fwptypes/FWP_CONDITION_VALUE0_
 - FWP_CONDITION_VALUE0
 - fwptypes/FWP_CONDITION_VALUE0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwptypes.h
api_name:
 - FWP_CONDITION_VALUE0
---

# FWP_CONDITION_VALUE0 structure


## -description

The **FWP_CONDITION_VALUE0** structure contains values that are used in filter conditions when testing for matching filters.

## -struct-fields

### -field type

Specifies the data type of the condition value.

See [FWP_DATA_TYPE](ne-fwptypes-fwp_data_type.md) for more information.

### -field uint8

Available when **type** is FWP_UINT8.

An unsigned 8-bit integer.

### -field uint16

Available when **type** is FWP_UINT16.

An unsigned 16-bit integer.

### -field uint32

Available when **type** is FWP_UINT32.

An unsigned 32-bit integer.

### -field uint64

Available when **type** is FWP_UINT64.

A pointer to an unsigned 64-bit integer.

> [!NOTE]
> This value cannot be null.

### -field int8

Available when **type** is FWP_INT8.

A signed 8-bit integer.

### -field int16

Available when **type** is FWP_INT16.

A signed 16-bit integer.

### -field int32

Available when **type** is FWP_INT32.

A signed 32-bit integer.

### -field int64

Available when **type** is FWP_INT64.

A pointer to a signed 64-bit integer.

> [!NOTE]
> This value cannot be null.

### -field float32

Available when **type** is FWP_FLOAT.

A single-precision floating-point  value.

### -field double64

Available when **type** is FWP_DOUBLE.

A pointer to a double-precision floating-point  value.

> [!NOTE]
> This value cannot be null.

### -field byteArray16

Available when **type** is FWP_BYTE_ARRAY16_TYPE.

A pointer to a [FWP_BYTE_ARRAY16](ns-fwptypes-fwp_byte_array16.md)  structure.

> [!NOTE]
> This value cannot be null.

### -field byteBlob

Available when **type** is FWP_BYTE_BLOB_TYPE.

A pointer to a [FWP_BYTE_BLOB](ns-fwptypes-fwp_byte_blob.md)  structure.

> [!NOTE]
> [FWP_BYTE_BLOB](ns-fwptypes-fwp_byte_blob.md) structure cannot be null.

### -field sid

Available when **type** is FWP_SID.

A pointer to a security identifier (SID) structure.

> [!NOTE]
> This security identifier cannot be null.

### -field sd

Available when **type** is FWP_SECURITY_DESCRIPTOR_TYPE.

A pointer to a security descriptor contained in a [FWP_BYTE_BLOB](ns-fwptypes-fwp_byte_blob.md)  structure.

> [!NOTE]
> Security descriptors cannot be null when used in filter conditions. Moreover, they need to be in self-relative format.

### -field tokenInformation

Available when **type** is FWP_TOKEN_INFORMATION_TYPE.

A pointer to token information contained in a [FWP_TOKEN_INFORMATION](ns-fwptypes-fwp_token_information.md)  structure.

### -field tokenAccessInformation

Available when **type** is FWP_TOKEN_ACCESS_INFORMATION_TYPE.

A pointer to token access information contained in a [FWP_BYTE_BLOB](ns-fwptypes-fwp_byte_blob.md) structure.

> [!NOTE]
> [FWP_BYTE_BLOB](ns-fwptypes-fwp_byte_blob.md) structure cannot be null.

### -field unicodeString

Available when **type** is FWP_UNICODE_STRING_TYPE.

A pointer to a null-terminated unicode string.

> [!NOTE]
> This value cannot be null.

### -field byteArray6

Available when **type** is FWP_BYTE_ARRAY6_TYPE.

A pointer to a [FWP_BYTE_ARRAY6](ns-fwptypes-fwp_byte_array6.md)  structure.

> [!NOTE]
> This value cannot be null.

> [!NOTE]
> Available only in Windows 7 and Windows Server 2008 R2.

### -field bitmapArray64

### -field v4AddrMask

Available when **type** is FWP_V4_ADDR_MASK.

A pointer to an IPv4 address contained in  an [FWP_V4_ADDR_AND_MASK](ns-fwptypes-fwp_v4_addr_and_mask.md)  structure.

### -field v6AddrMask

Available when **type** is FWP_V6_ADDR_MASK.

A pointer to an IPv6 address contained in  an [FWP_V6_ADDR_AND_MASK](ns-fwptypes-fwp_v6_addr_and_mask.md)  structure.

### -field rangeValue

Available when **type** is FWP_RANGE_TYPE.

A pointer to a range contained in  an [FWP_RANGE0](ns-fwptypes-fwp_range0.md)  structure.

## -remarks

The data type of 
**FWP_CONDITION_VALUE0** must be compatible with the data type of the
[FWP_VALUE0](ns-fwptypes-fwp_value0.md) to which it is being compared. However, this does not mean the data types
necessarily need to be the same. For example, an FWP_V4_ADDR_MASK can be
compared to an FWP_UINT32 containing an IPv4 address. See [FWP_MATCH_TYPE](ne-fwptypes-fwp_match_type.md) for detailed information about **FWP_CONDITION_VALUE0** and **FWP_VALUE0** compatibility rules.

**FWP_CONDITION_VALUE0** is a specific implementation of FWP_CONDITION_VALUE. See [WFP Version-Independent Names and Targeting Specific Versions of Windows](/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows)  for more information.

## -see-also

[FWP_BYTE_ARRAY16](ns-fwptypes-fwp_byte_array16.md)

[FWP_BYTE_ARRAY6](ns-fwptypes-fwp_byte_array6.md)

[FWP_BYTE_BLOB](ns-fwptypes-fwp_byte_blob.md)

[FWP_RANGE0](ns-fwptypes-fwp_range0.md)

[FWP_V4_ADDR_AND_MASK](ns-fwptypes-fwp_v4_addr_and_mask.md)

[FWP_V6_ADDR_AND_MASK](ns-fwptypes-fwp_v6_addr_and_mask.md)

[FWP_VALUE0](ns-fwptypes-fwp_value0.md)

[Windows Filtering Platform API Structures](/windows/desktop/FWP/fwp-structs)
