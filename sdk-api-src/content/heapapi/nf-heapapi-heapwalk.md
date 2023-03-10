---
UID: NF:heapapi.HeapWalk
title: HeapWalk function (heapapi.h)
description: Enumerates the memory blocks in the specified heap.
helpviewer_keywords: ["HeapWalk","HeapWalk function","_win32_heapwalk","base.heapwalk","heapapi/HeapWalk","winbase/HeapWalk"]
old-location: base\heapwalk.htm
tech.root: base
ms.assetid: ba4b7372-973b-4dea-9a93-faf847a047e5
ms.date: 12/05/2018
ms.keywords: HeapWalk, HeapWalk function, _win32_heapwalk, base.heapwalk, heapapi/HeapWalk, winbase/HeapWalk
req.header: heapapi.h
req.include-header: Windows.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HeapWalk
 - heapapi/HeapWalk
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-heap-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-heap-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - HeapWalk
---

# HeapWalk function


## -description

Enumerates the memory blocks in the specified heap.

## -parameters

### -param hHeap [in]

A handle to the heap. This handle is returned by either the 
      <a href="/windows/desktop/api/heapapi/nf-heapapi-heapcreate">HeapCreate</a> or 
      <a href="/windows/desktop/api/heapapi/nf-heapapi-getprocessheap">GetProcessHeap</a> function.

### -param lpEntry [in, out]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-process_heap_entry">PROCESS_HEAP_ENTRY</a> structure 
       that maintains state information for a particular heap enumeration.

If the <b>HeapWalk</b> function succeeds, returning the value 
       <b>TRUE</b>, this structure's members contain information about the next memory block in the 
       heap.

To initiate a heap enumeration, set the <b>lpData</b> field of the 
       <a href="/windows/desktop/api/minwinbase/ns-minwinbase-process_heap_entry">PROCESS_HEAP_ENTRY</a> structure to 
       <b>NULL</b>. To continue a particular heap enumeration, call the 
       <b>HeapWalk</b> function repeatedly, with no changes to 
       <i>hHeap</i>, <i>lpEntry</i>, or any of the members of the 
       <b>PROCESS_HEAP_ENTRY</b> structure.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If the heap enumeration terminates successfully by reaching the end of the heap, the function returns 
       <b>FALSE</b>, and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> 
       returns the error code <b>ERROR_NO_MORE_ITEMS</b>.

## -remarks

The <b>HeapWalk</b> function is primarily useful for debugging 
    because enumerating a heap is a potentially time-consuming operation. Locking the heap during enumeration blocks 
    other threads from accessing the heap and can degrade performance, especially on symmetric multiprocessing (SMP) 
    computers. The side effects can last until the heap is unlocked. Use the 
    <a href="/windows/desktop/api/heapapi/nf-heapapi-heaplock">HeapLock</a> and 
    <a href="/windows/desktop/api/heapapi/nf-heapapi-heapunlock">HeapUnlock</a> functions to control heap locking during heap 
    enumeration.

To initiate a heap enumeration, call <b>HeapWalk</b> with the 
    <b>lpData</b> field of the 
    <a href="/windows/desktop/api/minwinbase/ns-minwinbase-process_heap_entry">PROCESS_HEAP_ENTRY</a> structure pointed to by 
    <i>lpEntry</i> set to <b>NULL</b>.

To continue a heap enumeration, call <b>HeapWalk</b> with the same 
    <i>hHeap</i> and <i>lpEntry</i> values, and with the 
    <a href="/windows/desktop/api/minwinbase/ns-minwinbase-process_heap_entry">PROCESS_HEAP_ENTRY</a> structure unchanged from the 
    preceding call to <b>HeapWalk</b>. Repeat this process until you 
    have no need for further enumeration, or until the function returns <b>FALSE</b> and 
    <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns 
    <b>ERROR_NO_MORE_ITEMS</b>, indicating that all of the heap's memory blocks have been 
    enumerated.

No special call of <b>HeapWalk</b> is needed to terminate the 
    heap enumeration, since no enumeration state data is maintained outside the contents of the 
    <a href="/windows/desktop/api/minwinbase/ns-minwinbase-process_heap_entry">PROCESS_HEAP_ENTRY</a> structure.

<b>HeapWalk</b> can fail in a multithreaded application if the 
    heap is not locked during the heap enumeration.


#### Examples


<a href="/windows/desktop/Memory/enumerating-a-heap">Enumerating a Heap</a>


<div class="code"></div>

## -see-also

<a href="/windows/desktop/Memory/heap-functions">Heap Functions</a>



<a href="/windows/desktop/api/heapapi/nf-heapapi-heaplock">HeapLock</a>



<a href="/windows/desktop/api/heapapi/nf-heapapi-heaprealloc">HeapReAlloc</a>



<a href="/windows/desktop/api/heapapi/nf-heapapi-heapunlock">HeapUnlock</a>



<a href="/windows/desktop/api/heapapi/nf-heapapi-heapvalidate">HeapValidate</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory Management Functions</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-process_heap_entry">PROCESS_HEAP_ENTRY</a>