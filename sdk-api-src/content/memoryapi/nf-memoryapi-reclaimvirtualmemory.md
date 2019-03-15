---
UID: NF:memoryapi.ReclaimVirtualMemory
title: ReclaimVirtualMemory function
author: windows-sdk-content
description: Reclaims a range of memory pages that were offered to the system with OfferVirtualMemory.
old-location: base\reclaimvirtualmemory.htm
tech.root: Memory
ms.assetid: bb0ec5aa-b098-8a3f-67df-864a1672ba8f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ReclaimVirtualMemory, ReclaimVirtualMemory function, base.reclaimvirtualmemory, winbase/ReclaimVirtualMemory
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
 - ReclaimVirtualMemory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ReclaimVirtualMemory function


## -description


Reclaims a range of memory pages that were offered to the system with <a href="https://msdn.microsoft.com/45f8a433-0a9e-31d1-f21d-a17d7247e164">OfferVirtualMemory</a>.

If the offered memory has been discarded, the contents of the memory region is undefined and must be rewritten by the application.
      If the offered memory has not been discarded, it is reclaimed intact.


## -parameters




### -param VirtualAddress [in]

Page-aligned starting address of the memory to reclaim.


### -param Size [in]

Size, in bytes, of the memory region to reclaim.  <i>Size</i> must be an integer multiple of the system page size.


## -returns



Returns ERROR_SUCCESS if successful and the memory was reclaimed intact.

Returns ERROR_BUSY if successful but the memory was discarded and must be rewritten by the application.  In this case, the contents of the memory region is undefined.

Returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Code</a> otherwise.




## -remarks



Reclaimed memory pages can be used by the application, and will be written to the system paging file if paging occurs.

If the function returns ERROR_SUCCESS, the data in the reclaimed pages is valid.
      If the function returns ERROR_BUSY, the data in the reclaimed pages was discarded by the system and is no longer valid.
      For this reason, memory should only be offered to the system if the application does not need or can regenerate the data.




## -see-also




<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory Management Functions</a>



<a href="https://msdn.microsoft.com/45f8a433-0a9e-31d1-f21d-a17d7247e164">OfferVirtualMemory</a>



<a href="https://msdn.microsoft.com/9488a854-1ef0-488f-b3d1-57c1acb82a88">Virtual Memory Functions</a>



<a href="https://msdn.microsoft.com/a720dd89-c47c-4e48-bbc6-f2e02dfc4ed2">VirtualAlloc</a>



<a href="https://msdn.microsoft.com/d6f27be8-8929-4a4d-b52c-fa99044ca243">VirtualFree</a>



<a href="https://msdn.microsoft.com/414c4704-36f2-40f9-a69a-9d53ab354c30">VirtualLock</a>



<a href="https://msdn.microsoft.com/3b1f7d27-1f5d-452e-b58f-560cd9b9cbd3">VirtualQuery</a>
 

 

