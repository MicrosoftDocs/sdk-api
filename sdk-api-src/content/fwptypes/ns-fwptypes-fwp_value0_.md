---
UID: NS:fwptypes.FWP_VALUE0_
title: FWP_VALUE0_
author: windows-driver-content
description: Defines a data value that can be one of a number of different data types.
old-location: fwp\fwp_value0_struct.htm
old-project: FWP
ms.assetid: d3ffe19b-2c9b-4c7b-82c1-f9b846546212
ms.author: windowsdriverdev
ms.date: 4/12/2018
ms.keywords: FWP_VALUE0, FWP_VALUE0 structure [Filtering], FWP_VALUE0_, fwp.fwp_value0_struct, fwptypes/FWP_VALUE0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: FWP_VALUE0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Fwptypes.h
api_name:
-	FWP_VALUE0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FWP_VALUE0_ structure


## -description


The <b>FWP_VALUE0</b> structure defines a data value that can be one of a number of different data types.


## -struct-fields




### -field type

The type of data for this value. 

See <a href="https://msdn.microsoft.com/library/windows/hardware/ff552431">FWP_DATA_TYPE</a> for more information.


#### - ( unnamed union )

switch_type(FWP_DATA_TYPE), switch_is(type)



#### uint8

case(FWP_UINT8)

An unsigned 8-bit integer.



#### uint16

case(FWP_UINT16)

An unsigned 16-bit integer.



#### uint32

case(FWP_UINT32)

An unsigned 32-bit integer.



#### uint64

case(FWP_UINT64)

A pointer to an unsigned 64-bit integer.



#### int8

case(FWP_INT8)

A signed 8-bit integer.



#### int16

case(FWP_INT16)

A signed 16-bit integer.



#### int32

case(FWP_INT32)

A signed 32-bit integer.



#### int64

case(FWP_INT64)

A pointer to a signed 64-bit integer.



#### float32

case(FWP_FLOAT)

A single-precision floating-point  value.



#### double64

case(FWP_DOUBLE)

A pointer to a double-precision floating-point  value.



#### byteArray16

case(FWP_BYTE_ARRAY16_TYPE)

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff552425">FWP_BYTE_ARRAY16</a>  structure.



#### byteBlob

case(FWP_BYTE_BLOB_TYPE)

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a>  structure.



#### sid

case(FWP_SID)

A pointer to a SID.



#### sd

case(FWP_SECURITY_DESCRIPTOR_TYPE)

A pointer to a security descriptor contained in a <a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a>  structure. The data contained in the blob is a <a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure.



#### tokenInformation

case(FWP_TOKEN_INFORMATION_TYPE)

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552440">FWP_TOKEN_INFORMATION</a>  structure.



#### tokenAccessInformation

case(FWP_TOKEN_ACCESS_INFORMATION_TYPE)

A pointer to token access information contained in a <a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a>  structure. The data contained in the blob is a <a href="https://msdn.microsoft.com/cb727b91-c88f-48f3-8329-020d3f727dc7">TOKEN_ACCESS_INFORMATION</a> structure.



#### unicodeString

case(FWP_UNICODE_STRING_TYPE)

A pointer to a null-terminated unicode string.



#### byteArray6

case(FWP_BYTE_ARRAY6_TYPE)

Reserved.


## -remarks



This is primarily used to supply incoming values to the
filter engine.

When IP addresses are stored in FWP_UINT32 format or when IP port is stored in FWP_UINT16 format, they are stored in host-order not network-order. 

<b>FWP_VALUE0</b> is a specific implementation of FWP_VALUE. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552425">FWP_BYTE_ARRAY16</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552431">FWP_DATA_TYPE</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

