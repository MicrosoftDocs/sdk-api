---
UID: NF:strmif.IAMDevMemoryAllocator.CheckMemory
title: IAMDevMemoryAllocator::CheckMemory
author: windows-sdk-content
description: Note  The IAMDevMemoryAllocator interface is deprecated. Tests whether the specific instance (device) of the allocator allocated a memory pointer.
old-location: dshow\iamdevmemoryallocator_checkmemory.htm
tech.root: DirectShow
ms.assetid: d51be809-4a97-4098-9ef3-8ed6603f26c0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CheckMemory, CheckMemory method [DirectShow], CheckMemory method [DirectShow],IAMDevMemoryAllocator interface, IAMDevMemoryAllocator interface [DirectShow],CheckMemory method, IAMDevMemoryAllocator.CheckMemory, IAMDevMemoryAllocator::CheckMemory, IAMDevMemoryAllocatorCheckMemory, dshow.iamdevmemoryallocator_checkmemory, strmif/IAMDevMemoryAllocator::CheckMemory
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
 - IAMDevMemoryAllocator.CheckMemory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMDevMemoryAllocator::CheckMemory


## -description



<div class="alert"><b>Note</b>  The <b>IAMDevMemoryAllocator</b> interface is deprecated.</div>
<div> </div>
Tests whether the specific instance (device) of the allocator allocated a memory pointer.




## -parameters




### -param pBuffer [in]

Pointer to the allocated memory buffer's address.


## -returns



Returns S_OK if the on-board allocator allocated the memory, or S_FALSE if not. Memory that is on the particular device but not allocated will also return S_FALSE.




## -remarks



The hardware filter typically uses this method to test whether the pointer actually points to on-board memory.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/bab1e582-928a-408b-a9c5-8e9827e9928b">IAMDevMemoryAllocator Interface</a>
 

 

