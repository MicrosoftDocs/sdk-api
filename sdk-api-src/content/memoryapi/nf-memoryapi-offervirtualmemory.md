---
UID: NF:memoryapi.OfferVirtualMemory
title: OfferVirtualMemory function (memoryapi.h)
description: Indicates that the data contained in a range of memory pages is no longer needed by the application and can be discarded by the system if necessary.
helpviewer_keywords: ["OfferVirtualMemory","OfferVirtualMemory function","VMOfferPriorityBelowNormal","VMOfferPriorityLow","VMOfferPriorityNormal","VMOfferPriorityVeryLow","base.offervirtualmemory","winbase/OfferVirtualMemory"]
old-location: base\offervirtualmemory.htm
tech.root: base
ms.assetid: 45f8a433-0a9e-31d1-f21d-a17d7247e164
ms.date: 12/05/2018
ms.keywords: OfferVirtualMemory, OfferVirtualMemory function, VMOfferPriorityBelowNormal, VMOfferPriorityLow, VMOfferPriorityNormal, VMOfferPriorityVeryLow, base.offervirtualmemory, winbase/OfferVirtualMemory
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
 - OfferVirtualMemory
 - memoryapi/OfferVirtualMemory
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
 - OfferVirtualMemory
---

# OfferVirtualMemory function


## -description

Indicates that the data contained in a range of memory pages is no longer needed by the application and can be discarded by the system if necessary.

The specified pages will be marked as inaccessible, removed from the process working set, and will not be written to the paging file.

To later reclaim offered pages, call <a href="/windows/desktop/api/memoryapi/nf-memoryapi-reclaimvirtualmemory">ReclaimVirtualMemory</a>.

## -parameters

### -param VirtualAddress [in]

Page-aligned starting address of the memory to offer.

### -param Size [in]

Size, in bytes, of the memory region to offer.  <i>Size</i> must be an integer multiple of the system page size.

### -param Priority [in]

<i>Priority</i> indicates how important the offered memory is to the application.
       A higher priority increases the probability that the offered memory can be reclaimed intact when calling <a href="/windows/desktop/api/memoryapi/nf-memoryapi-reclaimvirtualmemory">ReclaimVirtualMemory</a>.
       The system typically discards lower priority memory before discarding higher priority memory.
       <i>Priority</i> must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VMOfferPriorityVeryLow"></a><a id="vmofferpriorityverylow"></a><a id="VMOFFERPRIORITYVERYLOW"></a>
<dl><dt>VMOfferPriorityVeryLow</dt> 0x00000001</dl>
</td>
<td width="60%">
The offered memory is very low priority, and should be the first discarded.
</td>
</tr>

<tr>
<td width="40%"><a id="VMOfferPriorityLow"></a><a id="vmofferprioritylow"></a><a id="VMOFFERPRIORITYLOW"></a>
<dl><dt>VMOfferPriorityLow</dt> 0x00000002</dl>
</td>
<td width="60%">
The offered memory is low priority.
</td>
</tr>

<tr>
<td width="40%"><a id="VMOfferPriorityBelowNormal"></a><a id="vmofferprioritybelownormal"></a><a id="VMOFFERPRIORITYBELOWNORMAL"></a>
<dl><dt>VMOfferPriorityBelowNormal</dt> 0x00000003</dl>
</td>
<td width="60%">
The offered memory is below normal priority.
</td>
</tr>

<tr>
<td width="40%"><a id="VMOfferPriorityNormal"></a><a id="vmofferprioritynormal"></a><a id="VMOFFERPRIORITYNORMAL"></a>
<dl><dt>VMOfferPriorityNormal</dt> 0x00000004</dl>
</td>
<td width="60%">
The offered memory is of normal priority to the application, and should be the last discarded.
</td>
</tr>

</table>

## -returns

ERROR_SUCCESS if successful; a <a href="/windows/desktop/Debug/system-error-codes">System Error Code</a> otherwise.

## -remarks

To reclaim offered pages, call <a href="/windows/desktop/api/memoryapi/nf-memoryapi-reclaimvirtualmemory">ReclaimVirtualMemory</a>.
      The data in reclaimed pages may have been discarded, in which case the contents of the memory region is undefined and must be rewritten by the application.

Do not call <b>OfferVirtualMemory</b> to offer virtual memory that is locked.
      Doing so will unlock the specified range of pages.

Note that offering and reclaiming virtual memory is similar to using the MEM_RESET and MEM_RESET_UNDO memory allocation flags,
      except that <b>OfferVirtualMemory</b> removes the memory from the process working set and restricts access to the offered pages until they are reclaimed.

## -see-also

<a href="/windows/desktop/api/memoryapi/nf-memoryapi-discardvirtualmemory">DiscardVirtualMemory</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory Management Functions</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-reclaimvirtualmemory">ReclaimVirtualMemory</a>



<a href="/windows/desktop/Memory/virtual-memory-functions">Virtual Memory Functions</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualfree">VirtualFree</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtuallock">VirtualLock</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualquery">VirtualQuery</a>
