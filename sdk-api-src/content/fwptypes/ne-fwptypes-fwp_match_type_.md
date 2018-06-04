---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# FWP_MATCH_TYPE_ enumeration


## -description


The <b>FWP_MATCH_TYPE</b> enumerated type specifies different match types allowed in filter conditions.


## -enum-fields




### -field FWP_MATCH_EQUAL

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




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

