---
UID: NF:memoryapi.OfferVirtualMemory
title: OfferVirtualMemory function
author: windows-sdk-content
description: Indicates that the data contained in a range of memory pages is no longer needed by the application and can be discarded by the system if necessary.
old-location: base\offervirtualmemory.htm
tech.root: memory
ms.assetid: 45f8a433-0a9e-31d1-f21d-a17d7247e164
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: OfferVirtualMemory, OfferVirtualMemory function, VMOfferPriorityBelowNormal, VMOfferPriorityLow, VMOfferPriorityNormal, VMOfferPriorityVeryLow, base.offervirtualmemory, winbase/OfferVirtualMemory
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - OfferVirtualMemory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OfferVirtualMemory function


## -description


Indicates that the data contained in a range of memory pages is no longer needed by the application and can be discarded by the system if necessary.

The specified pages will be marked as inaccessible, removed from the process working set, and will not be written to the paging file.

To later reclaim offered pages, call <a href="https://msdn.microsoft.com/bb0ec5aa-b098-8a3f-67df-864a1672ba8f">ReclaimVirtualMemory</a>.


## -parameters




### -param VirtualAddress [in]

Page-aligned starting address of the memory to offer.


### -param Size [in]

Size, in bytes, of the memory region to offer.  <i>Size</i> must be an integer multiple of the system page size.


### -param Priority [in]

<i>Priority</i> indicates how important the offered memory is to the application.
       A higher priority increases the probability that the offered memory can be reclaimed intact when calling <a href="https://msdn.microsoft.com/bb0ec5aa-b098-8a3f-67df-864a1672ba8f">ReclaimVirtualMemory</a>.
       The system typically discards lower priority memory before discarding higher priority memory.
       <i>Priority</i> must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VMOfferPriorityVeryLow"></a><a id="vmofferpriorityverylow"></a><a id="VMOFFERPRIORITYVERYLOW"></a><dl>
<dt><b>VMOfferPriorityVeryLow</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
The offered memory is very low priority, and should be the first discarded.

</td>
</tr>
<tr>
<td width="40%"><a id="VMOfferPriorityLow"></a><a id="vmofferprioritylow"></a><a id="VMOFFERPRIORITYLOW"></a><dl>
<dt><b>VMOfferPriorityLow</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
The offered memory is low priority.

</td>
</tr>
<tr>
<td width="40%"><a id="VMOfferPriorityBelowNormal"></a><a id="vmofferprioritybelownormal"></a><a id="VMOFFERPRIORITYBELOWNORMAL"></a><dl>
<dt><b>VMOfferPriorityBelowNormal</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
The offered memory is below normal priority.

</td>
</tr>
<tr>
<td width="40%"><a id="VMOfferPriorityNormal"></a><a id="vmofferprioritynormal"></a><a id="VMOFFERPRIORITYNORMAL"></a><dl>
<dt><b>VMOfferPriorityNormal</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
The offered memory is of normal priority to the application, and should be the last discarded.

</td>
</tr>
</table>
 


## -returns



ERROR_SUCCESS if successful; a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Code</a> otherwise.




## -remarks



To reclaim offered pages, call <a href="https://msdn.microsoft.com/bb0ec5aa-b098-8a3f-67df-864a1672ba8f">ReclaimVirtualMemory</a>.
      The data in reclaimed pages may have been discarded, in which case the contents of the memory region is undefined and must be rewritten by the application.

Do not call <b>OfferVirtualMemory</b> to offer virtual memory that is locked.
      Doing so will unlock the specified range of pages.

Note that offering and reclaiming virtual memory is similar to using the MEM_RESET and MEM_RESET_UNDO memory allocation flags,
      except that <b>OfferVirtualMemory</b> removes the memory from the process working set and restricts access to the offered pages until they are reclaimed.




## -see-also




<a href="https://msdn.microsoft.com/942e80cb-5a68-24fa-5d5d-fe3741bee2dc">DiscardVirtualMemory</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory Management Functions</a>



<a href="https://msdn.microsoft.com/bb0ec5aa-b098-8a3f-67df-864a1672ba8f">ReclaimVirtualMemory</a>



<a href="https://msdn.microsoft.com/9488a854-1ef0-488f-b3d1-57c1acb82a88">Virtual Memory Functions</a>



<a href="https://msdn.microsoft.com/a720dd89-c47c-4e48-bbc6-f2e02dfc4ed2">VirtualAlloc</a>



<a href="https://msdn.microsoft.com/d6f27be8-8929-4a4d-b52c-fa99044ca243">VirtualFree</a>



<a href="https://msdn.microsoft.com/414c4704-36f2-40f9-a69a-9d53ab354c30">VirtualLock</a>



<a href="https://msdn.microsoft.com/3b1f7d27-1f5d-452e-b58f-560cd9b9cbd3">VirtualQuery</a>
 

 

