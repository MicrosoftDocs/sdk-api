---
UID: NS:fwptypes.FWP_CONDITION_VALUE0_
title: FWP_CONDITION_VALUE0 (fwptypes.h)

description: Contains values that are used in filter conditions when testing for matching filters.
old-location: fwp\fwp_condition_value0.htm
tech.root: fwp
ms.assetid: edc34005-dbc1-45a4-b6c7-fbb8b13fa388

ms.date: 12/05/2018
ms.keywords: FWP_CONDITION_VALUE0, FWP_CONDITION_VALUE0 structure [Filtering], fwp.fwp_condition_value0, fwptypes/FWP_CONDITION_VALUE0
ms.topic: struct
f1_keywords: 
 - "fwptypes/FWP_CONDITION_VALUE0"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwptypes.h
api_name:
 - FWP_CONDITION_VALUE0
targetos: Windows
req.typenames: FWP_CONDITION_VALUE0
req.redist: 
ms.custom: 19H1
---

# FWP_CONDITION_VALUE0 structure


## -description


The <b>FWP_CONDITION_VALUE0</b> structure contains values that are used in filter conditions when testing for matching filters.


## -struct-fields




### -field type

Specifies the data type of the condition value.

See [FWP_DATA_TYPE](https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_data_type)a> for more information.


### -field uint8

Available when <b>type</b> is FWP_UINT8.

An unsigned 8-bit integer.


### -field uint16

Available when <b>type</b> is FWP_UINT16.

An unsigned 16-bit integer.


### -field uint32

Available when <b>type</b> is FWP_UINT32.

An unsigned 32-bit integer.


### -field uint64

Available when <b>type</b> is FWP_UINT64.

A pointer to an unsigned 64-bit integer.

<div class="alert"><b>Note</b>  This value cannot be null.</div>
<div> </div>

### -field int8

Available when <b>type</b> is FWP_INT8.

A signed 8-bit integer.


### -field int16

Available when <b>type</b> is FWP_INT16.

A signed 16-bit integer.


### -field int32

Available when <b>type</b> is FWP_INT32.

A signed 32-bit integer.


### -field int64

Available when <b>type</b> is FWP_INT64.

A pointer to a signed 64-bit integer.

<div class="alert"><b>Note</b>  This value cannot be null.</div>
<div> </div>

### -field float32

Available when <b>type</b> is FWP_FLOAT.

A single-precision floating-point  value.


### -field double64

Available when <b>type</b> is FWP_DOUBLE.

A pointer to a double-precision floating-point  value.

<div class="alert"><b>Note</b>  This value cannot be null.</div>
<div> </div>

### -field byteArray16

Available when <b>type</b> is FWP_BYTE_ARRAY16_TYPE.

A pointer to a [FWP_BYTE_ARRAY16](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_array16)a>  structure.

<div class="alert"><b>Note</b>  This value cannot be null.</div>
<div> </div>

### -field byteBlob

Available when <b>type</b> is FWP_BYTE_BLOB_TYPE.

A pointer to a [FWP_BYTE_BLOB](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)a>  structure.

[FWP_BYTE_BLOB](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)a> structure cannot be null.</div>
<div> </div>

### -field sid

Available when <b>type</b> is FWP_SID.

A pointer to a security identifier (SID) structure.

<div class="alert"><b>Note</b>  The security identifier cannot be null.</div>
<div> </div>

### -field sd

Available when <b>type</b> is FWP_SECURITY_DESCRIPTOR_TYPE.

A pointer to a security descriptor contained in a [FWP_BYTE_BLOB](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)a>  structure.

<div class="alert"><b>Note</b>  Security descriptors cannot be null when used in filter conditions. Moreover, they need to be in self-relative format.</div>
<div> </div>

### -field tokenInformation

Available when <b>type</b> is FWP_TOKEN_INFORMATION_TYPE.

A pointer to token information contained in a [FWP_TOKEN_INFORMATION](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_token_information)a>  structure.


### -field tokenAccessInformation

Available when <b>type</b> is FWP_TOKEN_ACCESS_INFORMATION_TYPE.

A pointer to token access information contained in a [FWP_BYTE_BLOB](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)a>  structure.

[FWP_BYTE_BLOB](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)a> structure cannot be null.</div>
<div> </div>

### -field unicodeString

Available when <b>type</b> is FWP_UNICODE_STRING_TYPE.

A pointer to a null-terminated unicode string.

<div class="alert"><b>Note</b>  This value cannot be null.</div>
<div> </div>

### -field byteArray6

Available when <b>type</b> is FWP_BYTE_ARRAY6_TYPE.

A pointer to a [FWP_BYTE_ARRAY6](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_array6)a>  structure.

<div class="alert"><b>Note</b>  This value cannot be null.</div>
<div> </div>
<div class="alert"><b>Note</b>  Available only in Windows 7 and Windows Server 2008 R2.</div>
<div> </div>

### -field bitmapArray64

 


### -field v4AddrMask

Available when <b>type</b> is FWP_V4_ADDR_MASK.

A pointer to an IPv4 address contained in  an [FWP_V4_ADDR_AND_MASK](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_v4_addr_and_mask)a>  structure.


### -field v6AddrMask

Available when <b>type</b> is FWP_V6_ADDR_MASK.

A pointer to an IPv6 address contained in  an [FWP_V6_ADDR_AND_MASK](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_v6_addr_and_mask)a>  structure.


### -field rangeValue

Available when <b>type</b> is FWP_RANGE_TYPE.

A pointer to a range contained in  an [FWP_RANGE0](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_range0)a>  structure.


## -remarks



The data type of 
<b>FWP_CONDITION_VALUE0</b> must be compatible with the data type of the
[FWP_VALUE0](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_value0)a> to which it is being compared. However, this does not mean the data types
necessarily need to be the same. For example, an FWP_V4_ADDR_MASK can be
compared to an FWP_UINT32 containing an IPv4 address. See [FWP_MATCH_TYPE](https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_match_type)a> for detailed information about <b>FWP_CONDITION_VALUE0</b> and <b>FWP_VALUE0</b> compatibility rules.

<b>FWP_CONDITION_VALUE0</b> is a specific implementation of FWP_CONDITION_VALUE. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




[FWP_BYTE_ARRAY16](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_array16)a>



[FWP_BYTE_ARRAY6](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_array6)a>



[FWP_BYTE_BLOB](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)a>



[FWP_RANGE0](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_range0)a>



[FWP_V4_ADDR_AND_MASK](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_v4_addr_and_mask)a>



[FWP_V6_ADDR_AND_MASK](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_v6_addr_and_mask)a>



[FWP_VALUE0](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_value0)a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

