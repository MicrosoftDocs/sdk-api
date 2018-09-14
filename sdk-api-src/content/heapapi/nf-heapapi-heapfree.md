---
UID: NF:heapapi.HeapFree
title: HeapFree function
author: windows-sdk-content
description: Frees a memory block allocated from a heap by the HeapAlloc or HeapReAlloc function.
old-location: base\heapfree.htm
tech.root: Memory
ms.assetid: 6139e55f-9dda-42b5-bc9b-8d9bbfeaa619
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: HEAP_NO_SERIALIZE, HeapFree, HeapFree function, _win32_heapfree, base.heapfree, heapapi/HeapFree, winbase/HeapFree
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - HeapFree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# HeapFree function


## -description


Frees a memory block allocated from a heap by the 
<a href="https://msdn.microsoft.com/9a176312-0312-4cc1-baf5-949b346d983e">HeapAlloc</a> or 
<a href="https://msdn.microsoft.com/21d711d9-3b16-4537-a830-1a2fa049a471">HeapReAlloc</a> function.


## -parameters




### -param hHeap [in]

A handle to the heap whose memory block is to be freed. This handle is returned by either the 
<a href="https://msdn.microsoft.com/8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b">HeapCreate</a> or 
<a href="https://msdn.microsoft.com/ecd716b2-df48-4914-9de4-47d8ad8ff9a2">GetProcessHeap</a> function.


### -param dwFlags [in]

The heap free options. Specifying the following value overrides the corresponding value specified in the <i>flOptions</i> parameter when the heap was created by using the 
<a href="https://msdn.microsoft.com/8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b">HeapCreate</a> function. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HEAP_NO_SERIALIZE"></a><a id="heap_no_serialize"></a><dl>
<dt><b>HEAP_NO_SERIALIZE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Serialized access will not be used. For more information, see Remarks.

To ensure that serialized access is disabled for all calls to this function, specify <b>HEAP_NO_SERIALIZE</b> in the call to <a href="https://msdn.microsoft.com/8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b">HeapCreate</a>. In this case, it is not necessary to additionally specify <b>HEAP_NO_SERIALIZE</b> in this function call.

Do not specify this value when accessing the process heap. The system may create additional threads within the application's process, such as a CTRL+C handler, that simultaneously access the process heap.

</td>
</tr>
</table>
 


### -param lpMem [in]

A pointer to the memory block to be freed. This pointer is returned by the 
<a href="https://msdn.microsoft.com/9a176312-0312-4cc1-baf5-949b346d983e">HeapAlloc</a> or 
<a href="https://msdn.microsoft.com/21d711d9-3b16-4537-a830-1a2fa049a471">HeapReAlloc</a> function. If this pointer is <b>NULL</b>, the behavior is undefined.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. An application can call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> for extended error information.




## -remarks



You should not refer in any way to memory that has been freed by 
<b>HeapFree</b>. After that memory is freed, any information that may have been in it is gone forever. If you require information, do not free memory containing the information. Function calls that return information about memory (such as 
<a href="https://msdn.microsoft.com/a8fcfd99-7b04-4aa3-8619-272b254551a3">HeapSize</a>) may not be used with freed memory, as they may return bogus data. Calling <b>HeapFree</b> twice with the same pointer can cause heap corruption, resulting in subsequent calls to <a href="https://msdn.microsoft.com/9a176312-0312-4cc1-baf5-949b346d983e">HeapAlloc</a> returning the same pointer twice.

Serialization ensures mutual exclusion when two or more threads attempt to simultaneously allocate or free blocks from the same heap. There is a small performance cost to serialization, but it must be used whenever multiple threads allocate and free memory from the same heap. Setting the <b>HEAP_NO_SERIALIZE</b> value eliminates mutual exclusion on the heap. Without serialization, two or more threads that use the same heap handle might attempt to allocate or free memory simultaneously, likely causing corruption in the heap. The <b>HEAP_NO_SERIALIZE</b> value can, therefore, be safely used only in the following situations:

<ul>
<li>The process has only one thread.</li>
<li>The process has multiple threads, but only one thread calls the heap functions for a specific heap.</li>
<li>The process has multiple threads, and the application provides its own mechanism for mutual exclusion to a specific heap.</li>
</ul>

#### Examples

For an example, see <a href="https://msdn.microsoft.com/00f69593-f03b-4f30-aeec-db3fda0ac356">Getting Process Heaps</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">Heap Functions</a>



<a href="https://msdn.microsoft.com/9a176312-0312-4cc1-baf5-949b346d983e">HeapAlloc</a>



<a href="https://msdn.microsoft.com/21d711d9-3b16-4537-a830-1a2fa049a471">HeapReAlloc</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory
    Management Functions</a>
 

 

