---
UID: NF:strmif.IAMDevMemoryAllocator.Alloc
title: IAMDevMemoryAllocator::Alloc
author: windows-sdk-content
description: Note  The IAMDevMemoryAllocator interface is deprecated. Allocates a memory buffer.
old-location: dshow\iamdevmemoryallocator_alloc.htm
tech.root: DirectShow
ms.assetid: de5f7755-fd96-4016-9cab-b98721080e14
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: Alloc, Alloc method [DirectShow], Alloc method [DirectShow],IAMDevMemoryAllocator interface, IAMDevMemoryAllocator interface [DirectShow],Alloc method, IAMDevMemoryAllocator.Alloc, IAMDevMemoryAllocator::Alloc, IAMDevMemoryAllocatorAlloc, dshow.iamdevmemoryallocator_alloc, strmif/IAMDevMemoryAllocator::Alloc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IAMDevMemoryAllocator.Alloc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMDevMemoryAllocator::Alloc


## -description



<div class="alert"><b>Note</b>  The <b>IAMDevMemoryAllocator</b> interface is deprecated.</div>
<div> </div>
Allocates a memory buffer.




## -parameters




### -param ppBuffer [out]

Pointer that will receive the address of the allocated memory buffer.


### -param pdwcbBuffer [in, out]

Pointer to a <b>DWORD</b> whose input value is the number of bytes to allocate and whose output value is the actual number of bytes allocated.


## -returns



Returns S_OK if the desired quantity of memory was allocated, S_FALSE if memory was unavailable.




## -remarks



Call this method to allocate a block of memory from the available pool.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/bab1e582-928a-408b-a9c5-8e9827e9928b">IAMDevMemoryAllocator Interface</a>



<a href="https://msdn.microsoft.com/d86d3016-bca0-4a0b-946b-f50c49266c67">IAMDevMemoryAllocator::Free</a>
 

 

