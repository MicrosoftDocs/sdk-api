---
UID: NS:strmif._AllocatorProperties
title: "_AllocatorProperties"
author: windows-sdk-content
description: The ALLOCATOR_PROPERTIES structure describes an allocator's count, size, alignment, and prefix properties.
old-location: dshow\allocator_properties.htm
old-project: DirectShow
ms.assetid: 813e4693-b549-4045-aff5-08f2dd754b6e
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: ALLOCATOR_PROPERTIES, ALLOCATOR_PROPERTIES structure [DirectShow], ALLOCATOR_PROPERTIESStructure, _AllocatorProperties, dshow.allocator_properties, strmif/ALLOCATOR_PROPERTIES
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
tech.root: 
req.typenames: ALLOCATOR_PROPERTIES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - ALLOCATOR_PROPERTIES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP
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
 

 

