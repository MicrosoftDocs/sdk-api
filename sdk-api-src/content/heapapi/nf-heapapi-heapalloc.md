---
UID: NF:heapapi.HeapAlloc
title: HeapAlloc function
author: windows-sdk-content
description: Allocates a block of memory from a heap. The allocated memory is not movable.
old-location: base\heapalloc.htm
tech.root: memory
ms.assetid: 9a176312-0312-4cc1-baf5-949b346d983e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: HEAP_GENERATE_EXCEPTIONS, HEAP_NO_SERIALIZE, HEAP_ZERO_MEMORY, HeapAlloc, HeapAlloc function, _win32_heapalloc, base.heapalloc, heapapi/HeapAlloc, winbase/HeapAlloc
ms.topic: function
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
 - HeapAlloc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# HeapAlloc function


## -description


Allocates a block of memory from a heap. The allocated memory is not movable.


## -parameters




### -param hHeap [in]

A handle to the heap from which the memory will be allocated. This handle is returned by the 
<a href="https://msdn.microsoft.com/8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b">HeapCreate</a> or 
<a href="https://msdn.microsoft.com/ecd716b2-df48-4914-9de4-47d8ad8ff9a2">GetProcessHeap</a> function.


### -param dwFlags [in]

The heap allocation options. Specifying any of these values will override the corresponding value specified when the heap was created with 
<a href="https://msdn.microsoft.com/8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b">HeapCreate</a>. This parameter can be one or more of the following values. 



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
The system will raise an exception to indicate a function failure, such as an out-of-memory condition, instead of returning <b>NULL</b>.

To ensure that exceptions are generated for all calls to this function, specify <b>HEAP_GENERATE_EXCEPTIONS</b> in the call to <a href="https://msdn.microsoft.com/8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b">HeapCreate</a>. In this case, it is not necessary to additionally specify <b>HEAP_GENERATE_EXCEPTIONS</b> in this function call.

</td>
</tr>
<tr>
<td width="40%"><a id="HEAP_NO_SERIALIZE"></a><a id="heap_no_serialize"></a><dl>
<dt><b>HEAP_NO_SERIALIZE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Serialized access will not be used for this allocation. 


For more information, see Remarks.

To ensure that serialized access is disabled for all calls to this function, specify <b>HEAP_NO_SERIALIZE</b> in the call to <a href="https://msdn.microsoft.com/8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b">HeapCreate</a>. In this case, it is not necessary to additionally specify <b>HEAP_NO_SERIALIZE</b> in this function call.

This value should not be specified when accessing the process's default heap. The system may create additional threads within the application's process, such as a CTRL+C handler, that simultaneously access the process's default heap.

</td>
</tr>
<tr>
<td width="40%"><a id="HEAP_ZERO_MEMORY"></a><a id="heap_zero_memory"></a><dl>
<dt><b>HEAP_ZERO_MEMORY</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The allocated memory will be initialized to zero. Otherwise, the memory is not initialized to zero.

</td>
</tr>
</table>
 


### -param dwBytes [in]

The number of bytes to be allocated.

If the heap specified by the <i>hHeap</i> parameter is a "non-growable" heap, <i>dwBytes</i> must be less than 0x7FFF8. You create a non-growable heap by calling the <a href="https://msdn.microsoft.com/8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b">HeapCreate</a> function with a nonzero value.


## -returns



If the function succeeds, the return value is a pointer to the allocated memory block.

If the function fails and you have not specified <b>HEAP_GENERATE_EXCEPTIONS</b>, the return value is <b>NULL</b>.

If the function fails and you have specified <b>HEAP_GENERATE_EXCEPTIONS</b>, the function may generate either of the exceptions listed in the following table. The particular exception depends upon the nature of the heap corruption. For more information, see <a href="https://msdn.microsoft.com/f3c4a9f3-c9ae-4d20-85a7-787cb32278d1">GetExceptionCode</a>.

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
 

If the function fails, it does not call <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a>. An application cannot call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> for extended error information.




## -remarks



If 
the <b>HeapAlloc</b> function succeeds, it allocates at least the amount of memory requested. 

To allocate memory from the process's default heap, use  <b>HeapAlloc</b> with the handle returned by the <a href="https://msdn.microsoft.com/ecd716b2-df48-4914-9de4-47d8ad8ff9a2">GetProcessHeap</a> function.

To free a block of memory allocated by 
<b>HeapAlloc</b>, use the 
<a href="https://msdn.microsoft.com/6139e55f-9dda-42b5-bc9b-8d9bbfeaa619">HeapFree</a> function.

Memory allocated by 
<b>HeapAlloc</b> is not movable. The address returned by 
<b>HeapAlloc</b> is valid until the memory block is freed or reallocated; the memory block does not need to be locked. Because the system cannot compact a private heap, it can become fragmented.

Applications that allocate large amounts of memory in various allocation sizes can use the 
<a href="https://msdn.microsoft.com/d10abf82-423c-4942-b05e-55de3a5c4219">low-fragmentation heap</a> to reduce heap fragmentation.

Serialization ensures mutual exclusion when two or more threads attempt to simultaneously allocate or free blocks from the same heap. There is a small performance cost to serialization, but it must be used whenever multiple threads allocate and free memory from the same heap. Setting the <b>HEAP_NO_SERIALIZE</b> value eliminates mutual exclusion on the heap. Without serialization, two or more threads that use the same heap handle might attempt to allocate or free memory simultaneously, likely causing corruption in the heap. The <b>HEAP_NO_SERIALIZE</b> value can, therefore, be safely used only in the following situations:

<ul>
<li>The process has only one thread.</li>
<li>The process has multiple threads, but only one thread calls the heap functions for a specific heap.</li>
<li>The process has multiple threads, and the application provides its own mechanism for mutual exclusion to a specific heap.</li>
</ul>

#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/1a67bd2f-afc0-48f4-91f2-34fd2b94910d">AWE Example</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">Heap Functions</a>



<a href="https://msdn.microsoft.com/6139e55f-9dda-42b5-bc9b-8d9bbfeaa619">HeapFree</a>



<a href="https://msdn.microsoft.com/21d711d9-3b16-4537-a830-1a2fa049a471">HeapReAlloc</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory
    Management Functions</a>
 

 

