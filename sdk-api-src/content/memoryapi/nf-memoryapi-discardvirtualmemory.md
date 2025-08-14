---
UID: NF:memoryapi.DiscardVirtualMemory
title: DiscardVirtualMemory function (memoryapi.h)
description: Discards the memory contents of a range of memory pages, without decommitting the memory. The contents of discarded memory is undefined and must be rewritten by the application.
helpviewer_keywords: ["DiscardVirtualMemory","DiscardVirtualMemory function","base.discardvirtualmemory","winbase/DiscardVirtualMemory"]
old-location: base\discardvirtualmemory.htm
tech.root: base
ms.assetid: 942e80cb-5a68-24fa-5d5d-fe3741bee2dc
ms.date: 12/05/2018
ms.keywords: DiscardVirtualMemory, DiscardVirtualMemory function, base.discardvirtualmemory, winbase/DiscardVirtualMemory
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
 - DiscardVirtualMemory
 - memoryapi/DiscardVirtualMemory
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
 - DiscardVirtualMemory
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

ERROR_SUCCESS if successful; a <a href="/windows/desktop/Debug/system-error-codes">System Error Code</a> otherwise.

## -remarks

If <b>DiscardVirtualMemory</b> fails, the contents of the region is not altered.

Use this function to discard memory contents that are no longer needed, while keeping the memory region itself committed.
      Discarding memory may give physical RAM back to the system.
      When the region of memory is again accessed by the application, the backing RAM is restored, and the contents of the memory is undefined.

<div class="alert"><b>Important</b>  Calls to <b>DiscardVirtualMemory</b> will fail if the memory protection is not <b>PAGE_READWRITE</b>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Memory/memory-management-functions">Memory Management Functions</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-offervirtualmemory">OfferVirtualMemory</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-reclaimvirtualmemory">ReclaimVirtualMemory</a>



<a href="/windows/desktop/Memory/virtual-memory-functions">Virtual Memory Functions</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualfree">VirtualFree</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtuallock">VirtualLock</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualquery">VirtualQuery</a>