---
UID: NF:strmif.IAMDevMemoryAllocator.Free
title: IAMDevMemoryAllocator::Free
author: windows-sdk-content
description: Note  The IAMDevMemoryAllocator interface is deprecated. Frees the previously allocated memory.
old-location: dshow\iamdevmemoryallocator_free.htm
tech.root: DirectShow
ms.assetid: d86d3016-bca0-4a0b-946b-f50c49266c67
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: Free, Free method [DirectShow], Free method [DirectShow],IAMDevMemoryAllocator interface, IAMDevMemoryAllocator interface [DirectShow],Free method, IAMDevMemoryAllocator.Free, IAMDevMemoryAllocator::Free, IAMDevMemoryAllocatorFree, dshow.iamdevmemoryallocator_free, strmif/IAMDevMemoryAllocator::Free
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
 - IAMDevMemoryAllocator.Free
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMDevMemoryAllocator::Free


## -description



<div class="alert"><b>Note</b>  The <b>IAMDevMemoryAllocator</b> interface is deprecated.</div>
<div> </div>
Frees the previously allocated memory.




## -parameters




### -param pBuffer [in]

Pointer to the allocated memory.


## -returns



Returns E_INVALIDARG if the specified allocator didn't allocate the memory (that is, <a href="https://msdn.microsoft.com/d51be809-4a97-4098-9ef3-8ed6603f26c0">CheckMemory</a> fails).




## -remarks



This method frees a block of memory from the pool.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/bab1e582-928a-408b-a9c5-8e9827e9928b">IAMDevMemoryAllocator Interface</a>
 

 

