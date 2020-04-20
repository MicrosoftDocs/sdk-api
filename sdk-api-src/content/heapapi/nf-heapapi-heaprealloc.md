---
UID: NF:heapapi.HeapReAlloc
title: HeapReAlloc function (heapapi.h)
description: Reallocates a block of memory from a heap. This function enables you to resize a memory block and change other memory block properties.helpviewer_keywords: ["HEAP_GENERATE_EXCEPTIONS","HEAP_NO_SERIALIZE","HEAP_REALLOC_IN_PLACE_ONLY","HEAP_ZERO_MEMORY","HeapReAlloc","HeapReAlloc function","_win32_heaprealloc","base.heaprealloc","heapapi/HeapReAlloc","winbase/HeapReAlloc"]
old-location: base\heaprealloc.htm
tech.root: Memory
ms.assetid: 21d711d9-3b16-4537-a830-1a2fa049a471
ms.date: 12/05/2018
ms.keywords: HEAP_GENERATE_EXCEPTIONS, HEAP_NO_SERIALIZE, HEAP_REALLOC_IN_PLACE_ONLY, HEAP_ZERO_MEMORY, HeapReAlloc, HeapReAlloc function, _win32_heaprealloc, base.heaprealloc, heapapi/HeapReAlloc, winbase/HeapReAlloc
f1_keywords:
- heapapi/HeapReAlloc
dev_langs:
- c++
req.header: heapapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
- API-MS-Win-Core-heap-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-heap-l1-2-0.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
api_name:
- HeapReAlloc
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# HeapReAlloc function


## -description


Reallocates a block of memory from a heap. This function enables you to resize a memory block and change other memory block properties. The allocated memory is not movable.
   
  


## -parameters




### -param hHeap [in]

A handle to the heap from which the memory is to be reallocated. This handle is a returned by either the 
<a href="https://docs.microsoft.com/windows/desktop/api/heapapi/nf-heapapi-heapcreate">HeapCreate</a> or 
<a href="https://docs.microsoft.com/windows/desktop/api/heapapi/nf-heapapi-getprocessheap">GetProcessHeap</a> function.


### -param dwFlags [in]

The heap reallocation options. Specifying a value overrides the corresponding value specified in the <i>flOptions</i> parameter when the heap was created by using the 
<a href="https://docs.microsoft.com/windows/desktop/api/heapapi/nf-heapapi-heapcreate">HeapCreate</a> function. This parameter can be one or more of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HEAP_GENERATE_EXCEPTIONS"></a><a id="heap_generate_exceptions"></a><dl>
<dt><b>HEAP_GENERATE_EXCEPTIONS</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The operating-system raises an exception to indicate a function failure, such as an out-of-memory condition, instead of returning <b>NULL</b>.

To ensure that exceptions are generated for all calls to this function, specify <b>HEAP_GENERATE_EXCEPTIONS</b> in the call to <a href="https://docs.microsoft.com/windows/desktop/api/heapapi/nf-heapapi-heapcreate">HeapCreate</a>. In this case, it is not necessary to additionally specify <b>HEAP_GENERATE_EXCEPTIONS</b> in this function call.

</td>
</tr>
<tr>
<td width="40%"><a id="HEAP_NO_SERIALIZE"></a><a id="heap_no_serialize"></a><dl>
<dt><b>HEAP_NO_SERIALIZE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Serialized access will not be used. For more information, see Remarks.

To ensure that serialized access is disabled for all calls to this function, specify <b>HEAP_NO_SERIALIZE</b> in the call to <a href="https://docs.microsoft.com/windows/desktop/api/heapapi/nf-heapapi-heapcreate">HeapCreate</a>. In this case, it is not necessary to additionally specify <b>HEAP_NO_SERIALIZE</b> in this function call.

This value should not be specified when accessing the process heap. The system may create additional threads within the application's process, such as a CTRL+C handler, that simultaneously access the process heap.

</td>
</tr>
<tr>
<td width="40%"><a id="HEAP_REALLOC_IN_PLACE_ONLY"></a><a id="heap_realloc_in_place_only"></a><dl>
<dt><b>HEAP_REALLOC_IN_PLACE_ONLY</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
There can be no movement when reallocating a memory block. If this value is not specified, the function may move the block to a new location. If this value is specified and the block cannot be resized without moving, the function fails, leaving the original memory block unchanged.

</td>
</tr>
<tr>
<td width="40%"><a id="HEAP_ZERO_MEMORY"></a><a id="heap_zero_memory"></a><dl>
<dt><b>HEAP_ZERO_MEMORY</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
If the reallocation request is for a larger size, the additional region of memory beyond the original size be initialized to zero. The contents of the memory block up to its original size are unaffected.

</td>
</tr>
</table>
 


### -param lpMem [in]

A pointer to the block of memory that the function reallocates. This pointer is returned by an earlier call to the 
<a href="https://docs.microsoft.com/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a> or 
<b>HeapReAlloc</b> function.


### -param dwBytes [in]

The new size of the memory block, in bytes. A memory block's size can be increased or decreased by using this function.

If the heap specified by the <i>hHeap</i> parameter is a "non-growable" heap, <i>dwBytes</i> must be less than 0x7FFF8. You create a non-growable heap by calling the 
<a href="https://docs.microsoft.com/windows/desktop/api/heapapi/nf-heapapi-heapcreate">HeapCreate</a> function with a nonzero value.


## -returns



If the function succeeds, the return value is a pointer to the reallocated memory block.

If the function fails and you have not specified <b>HEAP_GENERATE_EXCEPTIONS</b>, the return value is <b>NULL</b>. 

If the function fails and you have specified <b>HEAP_GENERATE_EXCEPTIONS</b>, the function may generate either of the exceptions listed in the following table. For more information, see <a href="https://docs.microsoft.com/windows/desktop/Debug/getexceptioncode">GetExceptionCode</a>.

<table>
<tr>
<th>Exception code</th>
<th>Description</th>
</tr>
<tr>
<td><b>STATUS_NO_MEMORY</b></td>
<td>The allocation attempt failed because of a lack of available memory or heap corruption.</td>
</tr>
<tr>
<td><b>STATUS_ACCESS_VIOLATION</b></td>
<td>The allocation attempt failed because of heap corruption or improper function parameters.</td>
</tr>
</table>
 

If the function fails, it does not call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a>. An application cannot call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> for extended error information.




## -remarks



If 
<b>HeapReAlloc</b> succeeds, it allocates at least the amount of memory requested. 

If 
<b>HeapReAlloc</b> fails, the original memory is not freed, and the original handle and pointer are still valid.

<b>HeapReAlloc</b> is guaranteed to preserve the content of the memory being reallocated, even if the new memory is allocated at a different location. The process of preserving the memory content involves a memory copy operation that is potentially very time-consuming. 

To free a block of memory allocated by 
<b>HeapReAlloc</b>, use the 
<a href="https://docs.microsoft.com/windows/desktop/api/heapapi/nf-heapapi-heapfree">HeapFree</a> function.

Serialization ensures mutual exclusion when two or more threads attempt to simultaneously allocate or free blocks from the same heap. There is a small performance cost to serialization, but it must be used whenever multiple threads allocate and free memory from the same heap. Setting the <b>HEAP_NO_SERIALIZE</b> value eliminates mutual exclusion on the heap. Without serialization, two or more threads that use the same heap handle might attempt to allocate or free memory simultaneously, likely causing corruption in the heap. The <b>HEAP_NO_SERIALIZE</b> value can, therefore, be safely used only in the following situations:

<ul>
<li>The process has only one thread.</li>
<li>The process has multiple threads, but only one thread calls the heap functions for a specific heap.</li>
<li>The process has multiple threads, and the application provides its own mechanism for mutual exclusion to a specific heap.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Memory/heap-functions">Heap Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a>



<a href="https://docs.microsoft.com/windows/desktop/api/heapapi/nf-heapapi-heapfree">HeapFree</a>



<a href="https://docs.microsoft.com/windows/desktop/Memory/memory-management-functions">Memory
    Management Functions</a>
 

 

