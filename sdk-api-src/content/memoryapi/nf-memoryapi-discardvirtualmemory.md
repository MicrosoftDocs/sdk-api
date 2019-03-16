---
UID: NF:memoryapi.DiscardVirtualMemory
title: DiscardVirtualMemory function
author: windows-sdk-content
description: Discards the memory contents of a range of memory pages, without decommitting the memory. The contents of discarded memory is undefined and must be rewritten by the application.
old-location: base\discardvirtualmemory.htm
tech.root: Memory
ms.assetid: 942e80cb-5a68-24fa-5d5d-fe3741bee2dc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DiscardVirtualMemory, DiscardVirtualMemory function, base.discardvirtualmemory, winbase/DiscardVirtualMemory
ms.topic: function
req.header: memoryapi.h
req.include-header: Windows.h, Memoryapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 Update [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 Update [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-memory-l1-1-2.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - DiscardVirtualMemory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DiscardVirtualMemory function


## -description


Discards the memory contents of a range of memory pages, without decommitting the memory.
        The contents of discarded memory is undefined and must be rewritten by the application.
      


## -parameters




### -param VirtualAddress [in]

Page-aligned starting address of the memory to discard.


### -param Size [in]

Size, in bytes, of the memory region to discard.  <i>Size</i> must be an integer multiple of the system page size.


## -returns



ERROR_SUCCESS if successful; a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Code</a> otherwise.




## -remarks



If <b>DiscardVirtualMemory</b> fails, the contents of the region is not altered.

Use this function to discard memory contents that are no longer needed, while keeping the memory region itself committed.
      Discarding memory may give physical RAM back to the system.
      When the region of memory is again accessed by the application, the backing RAM is restored, and the contents of the memory is undefined.

<div class="alert"><b>Important</b>  Calls to <b>DiscardVirtualMemory</b> will fail if the memory protection is not <b>PAGE_READWRITE</b>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory Management Functions</a>



<a href="https://msdn.microsoft.com/45f8a433-0a9e-31d1-f21d-a17d7247e164">OfferVirtualMemory</a>



<a href="https://msdn.microsoft.com/bb0ec5aa-b098-8a3f-67df-864a1672ba8f">ReclaimVirtualMemory</a>



<a href="https://msdn.microsoft.com/9488a854-1ef0-488f-b3d1-57c1acb82a88">Virtual Memory Functions</a>



<a href="https://msdn.microsoft.com/a720dd89-c47c-4e48-bbc6-f2e02dfc4ed2">VirtualAlloc</a>



<a href="https://msdn.microsoft.com/d6f27be8-8929-4a4d-b52c-fa99044ca243">VirtualFree</a>



<a href="https://msdn.microsoft.com/414c4704-36f2-40f9-a69a-9d53ab354c30">VirtualLock</a>



<a href="https://msdn.microsoft.com/3b1f7d27-1f5d-452e-b58f-560cd9b9cbd3">VirtualQuery</a>
 

 

