---
UID: NE:fwptypes.FWP_DATA_TYPE_
title: FWP_DATA_TYPE (fwptypes.h)
description: Data types that can be stored in an FWP_VALUE0 or an FWP_CONDITION_VALUE0structure.
helpviewer_keywords: ["FWP_BYTE_ARRAY16_TYPE","FWP_BYTE_ARRAY6_TYPE","FWP_BYTE_BLOB_TYPE","FWP_DATA_TYPE","FWP_DATA_TYPE enumeration [Filtering]","FWP_DATA_TYPE_MAX","FWP_DOUBLE","FWP_EMPTY","FWP_FLOAT","FWP_INT16","FWP_INT32","FWP_INT64","FWP_INT8","FWP_RANGE_TYPE","FWP_SECURITY_DESCRIPTOR_TYPE","FWP_SID","FWP_SINGLE_DATA_TYPE_MAX","FWP_TOKEN_ACCESS_INFORMATION_TYPE","FWP_TOKEN_INFORMATION_TYPE","FWP_UINT16","FWP_UINT32","FWP_UINT64","FWP_UINT8","FWP_UNICODE_STRING_TYPE","FWP_V4_ADDR_MASK","FWP_V6_ADDR_MASK","fwp.fwp_data_type_enum","fwptypes/FWP_BYTE_ARRAY16_TYPE","fwptypes/FWP_BYTE_ARRAY6_TYPE","fwptypes/FWP_BYTE_BLOB_TYPE","fwptypes/FWP_DATA_TYPE","fwptypes/FWP_DATA_TYPE_MAX","fwptypes/FWP_DOUBLE","fwptypes/FWP_EMPTY","fwptypes/FWP_FLOAT","fwptypes/FWP_INT16","fwptypes/FWP_INT32","fwptypes/FWP_INT64","fwptypes/FWP_INT8","fwptypes/FWP_RANGE_TYPE","fwptypes/FWP_SECURITY_DESCRIPTOR_TYPE","fwptypes/FWP_SID","fwptypes/FWP_SINGLE_DATA_TYPE_MAX","fwptypes/FWP_TOKEN_ACCESS_INFORMATION_TYPE","fwptypes/FWP_TOKEN_INFORMATION_TYPE","fwptypes/FWP_UINT16","fwptypes/FWP_UINT32","fwptypes/FWP_UINT64","fwptypes/FWP_UINT8","fwptypes/FWP_UNICODE_STRING_TYPE","fwptypes/FWP_V4_ADDR_MASK","fwptypes/FWP_V6_ADDR_MASK"]
old-location: fwp\fwp_data_type_enum.htm
tech.root: fwp
ms.assetid: db605170-bfe0-4339-8a40-7b1ce435278b
ms.date: 12/05/2018
ms.keywords: FWP_BYTE_ARRAY16_TYPE, FWP_BYTE_ARRAY6_TYPE, FWP_BYTE_BLOB_TYPE, FWP_DATA_TYPE, FWP_DATA_TYPE enumeration [Filtering], FWP_DATA_TYPE_MAX, FWP_DOUBLE, FWP_EMPTY, FWP_FLOAT, FWP_INT16, FWP_INT32, FWP_INT64, FWP_INT8, FWP_RANGE_TYPE, FWP_SECURITY_DESCRIPTOR_TYPE, FWP_SID, FWP_SINGLE_DATA_TYPE_MAX, FWP_TOKEN_ACCESS_INFORMATION_TYPE, FWP_TOKEN_INFORMATION_TYPE, FWP_UINT16, FWP_UINT32, FWP_UINT64, FWP_UINT8, FWP_UNICODE_STRING_TYPE, FWP_V4_ADDR_MASK, FWP_V6_ADDR_MASK, fwp.fwp_data_type_enum, fwptypes/FWP_BYTE_ARRAY16_TYPE, fwptypes/FWP_BYTE_ARRAY6_TYPE, fwptypes/FWP_BYTE_BLOB_TYPE, fwptypes/FWP_DATA_TYPE, fwptypes/FWP_DATA_TYPE_MAX, fwptypes/FWP_DOUBLE, fwptypes/FWP_EMPTY, fwptypes/FWP_FLOAT, fwptypes/FWP_INT16, fwptypes/FWP_INT32, fwptypes/FWP_INT64, fwptypes/FWP_INT8, fwptypes/FWP_RANGE_TYPE, fwptypes/FWP_SECURITY_DESCRIPTOR_TYPE, fwptypes/FWP_SID, fwptypes/FWP_SINGLE_DATA_TYPE_MAX, fwptypes/FWP_TOKEN_ACCESS_INFORMATION_TYPE, fwptypes/FWP_TOKEN_INFORMATION_TYPE, fwptypes/FWP_UINT16, fwptypes/FWP_UINT32, fwptypes/FWP_UINT64, fwptypes/FWP_UINT8, fwptypes/FWP_UNICODE_STRING_TYPE, fwptypes/FWP_V4_ADDR_MASK, fwptypes/FWP_V6_ADDR_MASK
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
req.typenames: FWP_DATA_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWP_DATA_TYPE_
 - fwptypes/FWP_DATA_TYPE_
 - FWP_DATA_TYPE
 - fwptypes/FWP_DATA_TYPE
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
 - FWP_DATA_TYPE
---

# FWP_DATA_TYPE enumeration


## -description

The [FWP_VALUE0](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_value0) or an [FWP_CONDITION_VALUE0](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_condition_value0)structure.

## -enum-fields

### -field FWP_EMPTY:0

Indicates no data.

### -field FWP_UINT8

Indicates an unsigned 8-bit integer value.

### -field FWP_UINT16

Indicates an unsigned 16-bit integer value.

### -field FWP_UINT32

Indicates an unsigned 32-bit integer value.

### -field FWP_UINT64

Indicates an unsigned 64-bit integer value.

### -field FWP_INT8

Indicates a signed 8-bit integer value.

### -field FWP_INT16

Indicates a signed 16-bit integer value.

### -field FWP_INT32

Indicates a signed 32-bit integer value.

### -field FWP_INT64

Indicates a signed 64-bit integer value.

### -field FWP_FLOAT

Indicates a pointer to a single-precision floating-point  value.

### -field FWP_DOUBLE

Indicates a pointer to a double-precision floating-point  value.

### -field FWP_BYTE_ARRAY16_TYPE

Indicates a pointer to an [FWP_BYTE_ARRAY16](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_array16) structure.

### -field FWP_BYTE_BLOB_TYPE

Indicates a pointer to an [FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob) structure.

### -field FWP_SID

Indicates a pointer to a SID.

### -field FWP_SECURITY_DESCRIPTOR_TYPE

Indicates a pointer to an [FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob) structure that describes a security descriptor.

### -field FWP_TOKEN_INFORMATION_TYPE

Indicates a pointer to an [FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob) structure that describes token information.

### -field FWP_TOKEN_ACCESS_INFORMATION_TYPE

Indicates a pointer to an [FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob) structure that describes token access information.

### -field FWP_UNICODE_STRING_TYPE

Indicates a pointer to a null-terminated unicode string.

### -field FWP_BYTE_ARRAY6_TYPE

Reserved.

### -field FWP_BITMAP_INDEX_TYPE

### -field FWP_BITMAP_ARRAY64_TYPE

### -field FWP_SINGLE_DATA_TYPE_MAX:0xff

Reserved for future use.

### -field FWP_V4_ADDR_MASK

Indicates a pointer to an [FWP_V4_ADDR_AND_MASK](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_v4_addr_and_mask) structure.

### -field FWP_V6_ADDR_MASK

Indicates a pointer to an [FWP_V6_ADDR_AND_MASK](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_v6_addr_and_mask) structure.

### -field FWP_RANGE_TYPE

Indicates a pointer to an [FWP_RANGE0](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_range0) structure.

### -field FWP_DATA_TYPE_MAX

Maximum value for testing purposes.

## -remarks

Not all data types are valid for each structure; see the tagged union
in each structure to determine which are allowed.

## -see-also

[FWP_BYTE_ARRAY16](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_array16)



[FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)



[FWP_CONDITION_VALUE0](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_condition_value0)



[FWP_RANGE0](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_range0)



[FWP_V4_ADDR_AND_MASK](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_v4_addr_and_mask)



[FWP_V6_ADDR_AND_MASK](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_v6_addr_and_mask)



[FWP_VALUE0](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_value0)
