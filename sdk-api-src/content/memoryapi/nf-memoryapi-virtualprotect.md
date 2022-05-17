---
UID: NF:memoryapi.VirtualProtect
title: VirtualProtect function (memoryapi.h)
description: Changes the protection on a region of committed pages in the virtual address space of the calling process.
helpviewer_keywords: ["VirtualProtect","VirtualProtect function","_win32_virtualprotect","base.virtualprotect","winbase/VirtualProtect"]
old-location: base\virtualprotect.htm
tech.root: base
ms.assetid: a0018bba-226b-4c18-8ea4-15e69524db11
ms.date: 12/05/2018
ms.keywords: VirtualProtect, VirtualProtect function, _win32_virtualprotect, base.virtualprotect, winbase/VirtualProtect
req.header: memoryapi.h
req.include-header: Windows.h, Memoryapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - VirtualProtect
 - memoryapi/VirtualProtect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-memory-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-1.dll
 - API-MS-Win-Core-memory-l1-1-2.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - VirtualProtect
---

# VirtualProtect function


## -description

Changes the protection on a region of committed pages in the virtual address space of the calling 
    process.

To change the access protection of any process, use the 
    <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualprotectex">VirtualProtectEx</a> function.

## -parameters

### -param lpAddress [in]

The address of the starting page of the region of pages whose access protection attributes are to be changed.

All pages in the specified region must be within the same reserved region allocated when calling the 
       <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a> or 
       <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualallocex">VirtualAllocEx</a> function using 
       <b>MEM_RESERVE</b>. The pages cannot span adjacent reserved regions that were allocated by 
       separate calls to <b>VirtualAlloc</b> or 
       <b>VirtualAllocEx</b> using 
       <b>MEM_RESERVE</b>.

### -param dwSize [in]

The size of the region whose access protection attributes are to be changed, in bytes. The region of 
      affected pages includes all pages containing one or more bytes in the range from the 
      <i>lpAddress</i> parameter to 
      <code>(lpAddress+dwSize)</code>. This means that a 2-byte range 
      straddling a page boundary causes the protection attributes of both pages to be changed.

### -param flNewProtect [in]

The memory protection option. This parameter can be one of the 
       <a href="/windows/desktop/Memory/memory-protection-constants">memory protection constants</a>.

For mapped views, this value must be compatible with the access protection specified when the view was 
       mapped (see <a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a>, 
       <a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffileex">MapViewOfFileEx</a>, and 
       <a href="/windows/desktop/api/winbase/nf-winbase-mapviewoffileexnuma">MapViewOfFileExNuma</a>).

### -param lpflOldProtect [out]

A pointer to a variable that receives the previous access protection value of the first page in the 
      specified region of pages. If this parameter is <b>NULL</b> or does not point to a valid 
      variable, the function fails.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

You can set the access protection value on committed pages only. If the state of any page in the specified 
   region is not committed, the function fails and returns without modifying the access protection of any pages in the 
   specified region.

The <b>PAGE_GUARD</b> protection modifier establishes guard pages. Guard pages act as 
   one-shot access alarms. For more information, see 
   <a href="/windows/desktop/Memory/creating-guard-pages">Creating Guard Pages</a>.

It is best to avoid using <b>VirtualProtect</b> to change 
   page protections on memory blocks allocated by <a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a>, 
   <a href="/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a>, or 
   <a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a>, because multiple memory blocks can exist on a 
   single page. The heap manager assumes that all pages in the heap grant at least read and write access.

When protecting a region that will be executable, the calling program bears responsibility for ensuring cache 
   coherency via an appropriate call to 
   <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-flushinstructioncache">FlushInstructionCache</a> once the code has been set 
   in place.  Otherwise attempts to execute code out of the newly executable region may produce unpredictable 
   results.

## -see-also

<a href="/windows/desktop/Memory/memory-management-functions">Memory Management Functions</a>



<a href="/windows/desktop/Memory/virtual-memory-functions">Virtual Memory Functions</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualprotectex">VirtualProtectEx</a>
