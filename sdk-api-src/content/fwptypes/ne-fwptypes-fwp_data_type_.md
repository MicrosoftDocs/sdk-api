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

# FWP_DATA_TYPE_ enumeration


## -description



		The <b>FWP_DATA_TYPE</b> enumerated type specifies data types that can be stored in an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552450">FWP_VALUE0</a> or an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552430">FWP_CONDITION_VALUE0</a>
structure.


## -enum-fields




### -field FWP_EMPTY

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

Indicates an signed 8-bit integer value.


### -field FWP_INT16

Indicates an signed 16-bit integer value.


### -field FWP_INT32

Indicates an signed 32-bit integer value.


### -field FWP_INT64

Indicates an signed 64-bit integer value.


### -field FWP_FLOAT

Indicates a pointer to a single-precision floating-point  value.


### -field FWP_DOUBLE

Indicates a pointer to a double-precision floating-point  value.


### -field FWP_BYTE_ARRAY16_TYPE

Indicates a pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552425">FWP_BYTE_ARRAY16</a> structure.


### -field FWP_BYTE_BLOB_TYPE

Indicates a pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a> structure.


### -field FWP_SID

Indicates a pointer to a SID.


### -field FWP_SECURITY_DESCRIPTOR_TYPE

Indicates a pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a> structure that describes a security descriptor.


### -field FWP_TOKEN_INFORMATION_TYPE

Indicates a pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a> structure that describes token information.


### -field FWP_TOKEN_ACCESS_INFORMATION_TYPE

Indicates a pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a> structure that describes token access information.


### -field FWP_UNICODE_STRING_TYPE

Indicates a pointer to a null-terminated unicode string.


### -field FWP_BYTE_ARRAY6_TYPE

Reserved.


### -field FWP_BITMAP_INDEX_TYPE


### -field FWP_BITMAP_ARRAY64_TYPE


### -field FWP_SINGLE_DATA_TYPE_MAX

Reserved for future use.


### -field FWP_V4_ADDR_MASK

Indicates a pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552441">FWP_V4_ADDR_AND_MASK</a> structure. 


### -field FWP_V6_ADDR_MASK

Indicates a pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552446">FWP_V6_ADDR_AND_MASK</a> structure. 


### -field FWP_RANGE_TYPE

Indicates a pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552438">FWP_RANGE0</a> structure.


### -field FWP_DATA_TYPE_MAX

Maximum value for testing purposes.


## -remarks



Not all data types are valid for each structure; see the tagged union
in each structure to determine which are allowed.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552425">FWP_BYTE_ARRAY16</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552430">FWP_CONDITION_VALUE0</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552438">FWP_RANGE0</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552441">FWP_V4_ADDR_AND_MASK</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552446">FWP_V6_ADDR_AND_MASK</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552450">FWP_VALUE0</a>
 

 

