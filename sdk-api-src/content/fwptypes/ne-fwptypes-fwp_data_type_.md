---
UID: NE:fwptypes.FWP_DATA_TYPE_
title: FWP_DATA_TYPE_
author: windows-sdk-content
description: Data types that can be stored in an FWP_VALUE0 or an FWP_CONDITION_VALUE0structure.
old-location: fwp\fwp_data_type_enum.htm
tech.root: FWP
ms.assetid: db605170-bfe0-4339-8a40-7b1ce435278b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FWP_BYTE_ARRAY16_TYPE, FWP_BYTE_ARRAY6_TYPE, FWP_BYTE_BLOB_TYPE, FWP_DATA_TYPE, FWP_DATA_TYPE enumeration [Filtering], FWP_DATA_TYPE_, FWP_DATA_TYPE_MAX, FWP_DOUBLE, FWP_EMPTY, FWP_FLOAT, FWP_INT16, FWP_INT32, FWP_INT64, FWP_INT8, FWP_RANGE_TYPE, FWP_SECURITY_DESCRIPTOR_TYPE, FWP_SID, FWP_SINGLE_DATA_TYPE_MAX, FWP_TOKEN_ACCESS_INFORMATION_TYPE, FWP_TOKEN_INFORMATION_TYPE, FWP_UINT16, FWP_UINT32, FWP_UINT64, FWP_UINT8, FWP_UNICODE_STRING_TYPE, FWP_V4_ADDR_MASK, FWP_V6_ADDR_MASK, fwp.fwp_data_type_enum, fwptypes/FWP_BYTE_ARRAY16_TYPE, fwptypes/FWP_BYTE_ARRAY6_TYPE, fwptypes/FWP_BYTE_BLOB_TYPE, fwptypes/FWP_DATA_TYPE, fwptypes/FWP_DATA_TYPE_MAX, fwptypes/FWP_DOUBLE, fwptypes/FWP_EMPTY, fwptypes/FWP_FLOAT, fwptypes/FWP_INT16, fwptypes/FWP_INT32, fwptypes/FWP_INT64, fwptypes/FWP_INT8, fwptypes/FWP_RANGE_TYPE, fwptypes/FWP_SECURITY_DESCRIPTOR_TYPE, fwptypes/FWP_SID, fwptypes/FWP_SINGLE_DATA_TYPE_MAX, fwptypes/FWP_TOKEN_ACCESS_INFORMATION_TYPE, fwptypes/FWP_TOKEN_INFORMATION_TYPE, fwptypes/FWP_UINT16, fwptypes/FWP_UINT32, fwptypes/FWP_UINT64, fwptypes/FWP_UINT8, fwptypes/FWP_UNICODE_STRING_TYPE, fwptypes/FWP_V4_ADDR_MASK, fwptypes/FWP_V6_ADDR_MASK
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - FWP_DATA_TYPE
product: Windows
targetos: Windows
req.typenames: FWP_DATA_TYPE
req.redist: 
---

# FWP_DATA_TYPE_ enumeration


## -description


The <b>FWP_DATA_TYPE</b> enumerated type specifies data types that can be stored in an <a href="https://msdn.microsoft.com/d3ffe19b-2c9b-4c7b-82c1-f9b846546212">FWP_VALUE0</a> or an <a href="https://msdn.microsoft.com/edc34005-dbc1-45a4-b6c7-fbb8b13fa388">FWP_CONDITION_VALUE0</a>structure.


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

Indicates a pointer to an <a href="https://msdn.microsoft.com/254ee02f-747d-46e4-9851-141db57e1aa7">FWP_BYTE_ARRAY16</a> structure.


### -field FWP_BYTE_BLOB_TYPE

Indicates a pointer to an <a href="https://msdn.microsoft.com/85f360bf-5ee4-4980-b4ce-15ff310d8fbe">FWP_BYTE_BLOB</a> structure.


### -field FWP_SID

Indicates a pointer to a SID.


### -field FWP_SECURITY_DESCRIPTOR_TYPE

Indicates a pointer to an <a href="https://msdn.microsoft.com/85f360bf-5ee4-4980-b4ce-15ff310d8fbe">FWP_BYTE_BLOB</a> structure that describes a security descriptor.


### -field FWP_TOKEN_INFORMATION_TYPE

Indicates a pointer to an <a href="https://msdn.microsoft.com/85f360bf-5ee4-4980-b4ce-15ff310d8fbe">FWP_BYTE_BLOB</a> structure that describes token information.


### -field FWP_TOKEN_ACCESS_INFORMATION_TYPE

Indicates a pointer to an <a href="https://msdn.microsoft.com/85f360bf-5ee4-4980-b4ce-15ff310d8fbe">FWP_BYTE_BLOB</a> structure that describes token access information.


### -field FWP_UNICODE_STRING_TYPE

Indicates a pointer to a null-terminated unicode string.


### -field FWP_BYTE_ARRAY6_TYPE

Reserved.


### -field FWP_BITMAP_INDEX_TYPE


### -field FWP_BITMAP_ARRAY64_TYPE


### -field FWP_SINGLE_DATA_TYPE_MAX

Reserved for future use.


### -field FWP_V4_ADDR_MASK

Indicates a pointer to an <a href="https://msdn.microsoft.com/da6315af-264e-4dcb-b5eb-ac308128a511">FWP_V4_ADDR_AND_MASK</a> structure. 


### -field FWP_V6_ADDR_MASK

Indicates a pointer to an <a href="https://msdn.microsoft.com/d8566d41-677a-424f-89f3-e333a0520288">FWP_V6_ADDR_AND_MASK</a> structure. 


### -field FWP_RANGE_TYPE

Indicates a pointer to an <a href="https://msdn.microsoft.com/191ec0e4-2489-4f6f-80c5-8feec83d69c2">FWP_RANGE0</a> structure.


### -field FWP_DATA_TYPE_MAX

Maximum value for testing purposes.


## -remarks



Not all data types are valid for each structure; see the tagged union
in each structure to determine which are allowed.




## -see-also




<a href="https://msdn.microsoft.com/254ee02f-747d-46e4-9851-141db57e1aa7">FWP_BYTE_ARRAY16</a>



<a href="https://msdn.microsoft.com/85f360bf-5ee4-4980-b4ce-15ff310d8fbe">FWP_BYTE_BLOB</a>



<a href="https://msdn.microsoft.com/edc34005-dbc1-45a4-b6c7-fbb8b13fa388">FWP_CONDITION_VALUE0</a>



<a href="https://msdn.microsoft.com/191ec0e4-2489-4f6f-80c5-8feec83d69c2">FWP_RANGE0</a>



<a href="https://msdn.microsoft.com/da6315af-264e-4dcb-b5eb-ac308128a511">FWP_V4_ADDR_AND_MASK</a>



<a href="https://msdn.microsoft.com/d8566d41-677a-424f-89f3-e333a0520288">FWP_V6_ADDR_AND_MASK</a>



<a href="https://msdn.microsoft.com/d3ffe19b-2c9b-4c7b-82c1-f9b846546212">FWP_VALUE0</a>
 

 

