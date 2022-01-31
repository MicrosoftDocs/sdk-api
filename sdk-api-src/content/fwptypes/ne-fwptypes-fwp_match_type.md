---
UID: NE:fwptypes.FWP_MATCH_TYPE_
title: FWP_MATCH_TYPE (fwptypes.h)
description: Different match types allowed in filter conditions.
helpviewer_keywords: ["FWP_MATCH_EQUAL","FWP_MATCH_EQUAL_CASE_INSENSITIVE","FWP_MATCH_FLAGS_ALL_SET","FWP_MATCH_FLAGS_ANY_SET","FWP_MATCH_FLAGS_NONE_SET","FWP_MATCH_GREATER","FWP_MATCH_GREATER_OR_EQUAL","FWP_MATCH_LESS","FWP_MATCH_LESS_OR_EQUAL","FWP_MATCH_NOT_EQUAL","FWP_MATCH_RANGE","FWP_MATCH_TYPE","FWP_MATCH_TYPE enumeration [Filtering]","FWP_MATCH_TYPE_MAX","fwp.fwp_match_type_enum","fwptypes/FWP_MATCH_EQUAL","fwptypes/FWP_MATCH_EQUAL_CASE_INSENSITIVE","fwptypes/FWP_MATCH_FLAGS_ALL_SET","fwptypes/FWP_MATCH_FLAGS_ANY_SET","fwptypes/FWP_MATCH_FLAGS_NONE_SET","fwptypes/FWP_MATCH_GREATER","fwptypes/FWP_MATCH_GREATER_OR_EQUAL","fwptypes/FWP_MATCH_LESS","fwptypes/FWP_MATCH_LESS_OR_EQUAL","fwptypes/FWP_MATCH_NOT_EQUAL","fwptypes/FWP_MATCH_RANGE","fwptypes/FWP_MATCH_TYPE","fwptypes/FWP_MATCH_TYPE_MAX"]
old-location: fwp\fwp_match_type_enum.htm
tech.root: fwp
ms.assetid: a49efb25-990c-459d-90bc-758337c351d5
ms.date: 12/05/2018
ms.keywords: FWP_MATCH_EQUAL, FWP_MATCH_EQUAL_CASE_INSENSITIVE, FWP_MATCH_FLAGS_ALL_SET, FWP_MATCH_FLAGS_ANY_SET, FWP_MATCH_FLAGS_NONE_SET, FWP_MATCH_GREATER, FWP_MATCH_GREATER_OR_EQUAL, FWP_MATCH_LESS, FWP_MATCH_LESS_OR_EQUAL, FWP_MATCH_NOT_EQUAL, FWP_MATCH_RANGE, FWP_MATCH_TYPE, FWP_MATCH_TYPE enumeration [Filtering], FWP_MATCH_TYPE_MAX, fwp.fwp_match_type_enum, fwptypes/FWP_MATCH_EQUAL, fwptypes/FWP_MATCH_EQUAL_CASE_INSENSITIVE, fwptypes/FWP_MATCH_FLAGS_ALL_SET, fwptypes/FWP_MATCH_FLAGS_ANY_SET, fwptypes/FWP_MATCH_FLAGS_NONE_SET, fwptypes/FWP_MATCH_GREATER, fwptypes/FWP_MATCH_GREATER_OR_EQUAL, fwptypes/FWP_MATCH_LESS, fwptypes/FWP_MATCH_LESS_OR_EQUAL, fwptypes/FWP_MATCH_NOT_EQUAL, fwptypes/FWP_MATCH_RANGE, fwptypes/FWP_MATCH_TYPE, fwptypes/FWP_MATCH_TYPE_MAX
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
req.typenames: FWP_MATCH_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWP_MATCH_TYPE_
 - fwptypes/FWP_MATCH_TYPE_
 - FWP_MATCH_TYPE
 - fwptypes/FWP_MATCH_TYPE
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
 - FWP_MATCH_TYPE
---

# FWP_MATCH_TYPE enumeration


## -description

The <b>FWP_MATCH_TYPE</b> enumerated type specifies different match types allowed in filter conditions.

## -enum-fields

### -field FWP_MATCH_EQUAL:0

Tests whether the value is equal to the condition value. 

All data types support <b>FWP_MATCH_EQUAL</b>.

### -field FWP_MATCH_GREATER

Tests whether the value is greater than the condition value.

Only sortable data types support <b>FWP_MATCH_GREATER</b>. Sortable data types consist of all integer types, FWP_BYTE_ARRAY16_TYPE, FWP_BYTE_BLOB_TYPE, and FWP_UNICODE_STRING_TYPE.

### -field FWP_MATCH_LESS

Tests whether the value is less than the condition value.

Only sortable data types support <b>FWP_MATCH_LESS</b>.

### -field FWP_MATCH_GREATER_OR_EQUAL

Tests whether the value is greater than or equal to the condition value.

Only sortable data types support <b>FWP_MATCH_GREATER_OR_EQUAL</b>.

### -field FWP_MATCH_LESS_OR_EQUAL

Tests whether the value is less than or equal to the condition value.

Only sortable data types support <b>FWP_MATCH_LESS_OR_EQUAL</b>.

### -field FWP_MATCH_RANGE

Tests whether the value is within a given range of condition values.

Only sortable data types support <b>FWP_MATCH_RANGE</b>.

### -field FWP_MATCH_FLAGS_ALL_SET

Tests whether all flags are set.

Only unsigned integer data types support <b>FWP_MATCH_FLAGS_ALL_SET</b>.

### -field FWP_MATCH_FLAGS_ANY_SET

Tests whether any flags are set.

Only unsigned integer data types support <b>FWP_MATCH_FLAGS_ANY_SET</b>.

### -field FWP_MATCH_FLAGS_NONE_SET

Tests whether no flags are set.

Only unsigned integer data types support <b>FWP_MATCH_FLAGS_NONE_SET</b>.

### -field FWP_MATCH_EQUAL_CASE_INSENSITIVE

Tests whether the value is equal to the condition value. The test is case insensitive.

Only the FWP_UNICODE_STRING_TYPE data type supports <b>FWP_MATCH_EQUAL_CASE_INSENSITIVE</b>.

### -field FWP_MATCH_NOT_EQUAL

Tests whether the value is not equal to the condition value.

Only sortable data types support <b>FWP_MATCH_NOT_EQUAL</b>.<div class="alert"><b>Note</b>  Available only in Windows 7 and Windows Server 2008 R2.</div>
<div> </div>

### -field FWP_MATCH_PREFIX

### -field FWP_MATCH_NOT_PREFIX

### -field FWP_MATCH_TYPE_MAX

Maximum value for testing purposes.

## -remarks

In general, the value data type and the filter condition data type must be the same. The Base Filtering Engine (BFE) does not perform any data conversion. For example, an FWP_UINT32 value cannot be compared with an FWP_UINT16 value.


Exceptions to this rule are as follows.

<ul>
<li>An FWP_UINT32 field that contains an IPv4 address can be compared with an FWP_V4_ADDR_MASK value.</li>
<li>An FWP_BYTE_ARRAY16_TYPE field that contains an IPv6 address can be compared with an FWP_V6_ADDR_MASK value.</li>
<li>An FWP_TOKEN_INFORMATION_TYPE field can be compared with an FWP_SECURITY_DESCRIPTOR_TYPE value when adding filters.</li>
<li>An FWP_TOKEN_ACCESS_INFORMATION_TYPE field can be compared with an FWP_SECURITY_DESCRIPTOR_TYPE value when adding filters.</li>
<li>An FWP_TOKEN_INFORMATION_TYPE field can be compared with an FWP_SID value when enumerating.</li>
<li>An FWP_TOKEN_ACCESS_INFORMATION_TYPE field can be compared with an FWP_SID value when enumerating.</li>
</ul>

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
