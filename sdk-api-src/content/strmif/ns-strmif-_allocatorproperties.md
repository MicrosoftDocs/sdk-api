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

# _AllocatorProperties structure


## -description



The ALLOCATOR_PROPERTIES structure describes an allocator's count, size, alignment, and prefix properties.




## -struct-fields




### -field cBuffers

Number of buffers created by the allocator.


### -field cbBuffer

Size of each buffer in bytes, excluding any prefix.


### -field cbAlign

Alignment of the buffer; buffer start will be aligned on a multiple of this value.


### -field cbPrefix

Each buffer is preceded by a prefix of this many bytes.


## -remarks



The <a href="https://msdn.microsoft.com/a3c69dfb-6ee4-401b-8dcb-4e42a8cd8156">IMediaSample::GetPointer</a> method returns a pointer to the beginning of the buffer, not including the prefix bytes designated by <i>cbPrefix</i>.

The alignment is applied to the prefix data, if any. If a nonzero prefix is used, the beginning of the prefix is aligned according to <i>cbAlign</i>.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

