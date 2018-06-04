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

# _MINIDUMP_FUNCTION_TABLE_DESCRIPTOR structure


## -description


Represents a function table stream.


## -struct-fields




### -field MinimumAddress

The minimum address of functions described by the table.


### -field MaximumAddress

The maximum address of functions described by the table.


### -field BaseAddress

The base address to use when computing full virtual addresses from relative virtual addresses in function entries.


### -field EntryCount

The number of entries in the function table.


### -field SizeOfAlignPad

The size of alignment padding that follows the function entry data, in bytes. The function entry data in the stream is guaranteed to be aligned appropriately for access to the data members. If a minidump is directly mapped in memory, it is always possible to directly reference structure members in the stream.


## -remarks



The first descriptor in the function table stream follows the header, 
<a href="https://msdn.microsoft.com/b2845799-acc9-4410-9059-45f7a8313e9f">MINIDUMP_FUNCTION_TABLE_STREAM</a>. The generic descriptor is followed by a native system descriptor, then by <b>EntryCount</b> native system function entry structures.




## -see-also




<a href="https://msdn.microsoft.com/b2845799-acc9-4410-9059-45f7a8313e9f">MINIDUMP_FUNCTION_TABLE_STREAM</a>
 

 

