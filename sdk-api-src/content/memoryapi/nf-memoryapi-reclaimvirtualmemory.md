---
UID: NF:memoryapi.ReclaimVirtualMemory
title: ReclaimVirtualMemory function (memoryapi.h)
description: Reclaims a range of memory pages that were offered to the system with OfferVirtualMemory.
helpviewer_keywords: ["ReclaimVirtualMemory","ReclaimVirtualMemory function","base.reclaimvirtualmemory","winbase/ReclaimVirtualMemory"]
old-location: base\reclaimvirtualmemory.htm
tech.root: base
ms.assetid: bb0ec5aa-b098-8a3f-67df-864a1672ba8f
ms.date: 12/05/2018
ms.keywords: ReclaimVirtualMemory, ReclaimVirtualMemory function, base.reclaimvirtualmemory, winbase/ReclaimVirtualMemory
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
req.lib: onecore.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ReclaimVirtualMemory
 - memoryapi/ReclaimVirtualMemory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-memory-l1-1-9.dll
 - api-ms-win-core-memory-l1-1-8.dll
 - api-ms-win-core-memory-l1-1-7.dll
 - api-ms-win-core-memory-l1-1-6.dll
 - api-ms-win-core-memory-l1-1-5.dll
 - Kernel32.dll
 - API-MS-Win-Core-memory-l1-1-2.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - ReclaimVirtualMemory
---

# ReclaimVirtualMemory function


## -description

Reclaims a range of memory pages that were offered to the system with <a href="/windows/desktop/api/memoryapi/nf-memoryapi-offervirtualmemory">OfferVirtualMemory</a>.

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

Returns a <a href="/windows/desktop/Debug/system-error-codes">System Error Code</a> otherwise.

## -remarks

Reclaimed memory pages can be used by the application, and will be written to the system paging file if paging occurs.

If the function returns ERROR_SUCCESS, the data in the reclaimed pages is valid.
      If the function returns ERROR_BUSY, the data in the reclaimed pages was discarded by the system and is no longer valid.
      For this reason, memory should only be offered to the system if the application does not need or can regenerate the data.

## -see-also

<a href="/windows/desktop/Memory/memory-management-functions">Memory Management Functions</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-offervirtualmemory">OfferVirtualMemory</a>



<a href="/windows/desktop/Memory/virtual-memory-functions">Virtual Memory Functions</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualfree">VirtualFree</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtuallock">VirtualLock</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualquery">VirtualQuery</a>