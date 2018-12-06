---
UID: NF:heapapi.HeapCompact
title: HeapCompact function
author: windows-sdk-content
description: Returns the size of the largest committed free block in the specified heap. If the Disable heap coalesce on free global flag is set, this function also coalesces adjacent free blocks of memory in the heap.
old-location: base\heapcompact.htm
tech.root: memory
ms.assetid: 792ec16f-d6b0-4afd-a832-29fe12b25058
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: HEAP_NO_SERIALIZE, HeapCompact, HeapCompact function, _win32_heapcompact, base.heapcompact, heapapi/HeapCompact, winbase/HeapCompact
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
 - HeapCompact
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# HeapCompact function


## -description


Returns  the size of the largest committed free block in the specified heap.   If the <a href="http://go.microsoft.com/fwlink/p/?linkid=160678">Disable heap coalesce on free</a> global flag is set, this function also coalesces adjacent free blocks of memory in the heap.


## -parameters




### -param hHeap [in]

A handle to the heap. This handle is returned by either the 
<a href="https://msdn.microsoft.com/8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b">HeapCreate</a> or 
<a href="https://msdn.microsoft.com/ecd716b2-df48-4914-9de4-47d8ad8ff9a2">GetProcessHeap</a> function.


### -param dwFlags [in]

The heap access options. This parameter can be the following value. 



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
Serialized access will not be used. 


For more information, see Remarks.

To ensure that serialized access is disabled for all calls to this function, specify <b>HEAP_NO_SERIALIZE</b> in the call to <a href="https://msdn.microsoft.com/8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b">HeapCreate</a>. In this case, it is not necessary to additionally specify <b>HEAP_NO_SERIALIZE</b> in this function call.

Do not specify this value when accessing the process heap. The system may create additional threads within the application's process, such as a CTRL+C handler, that simultaneously access the process heap.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is the size of the largest committed free block in the heap, in bytes.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

In the unlikely case that there is absolutely no space available in the heap, the function return value is zero, and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns the value NO_ERROR.




## -remarks



The <b>HeapCompact</b> function is primarily useful for debugging. Ordinarily, the system compacts the heap whenever the <a href="https://msdn.microsoft.com/6139e55f-9dda-42b5-bc9b-8d9bbfeaa619">HeapFree</a> function is called, and the <b>HeapCompact</b> function returns the size of the largest free block in the heap but does not compact the heap any further. If the <a href="http://go.microsoft.com/fwlink/p/?linkid=160678">Disable heap coalesce on free</a> global flag is set during debugging, the system does not compact the heap and calling the <b>HeapCompact</b> function does compact the heap.  For more information about global flags, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=153601">GFlags</a> documentation.

There is no guarantee that an application can successfully allocate a memory block of the size returned by 
<b>HeapCompact</b>. Other threads or the commit threshold might prevent such an allocation.

Serialization ensures mutual exclusion when two or more threads attempt to simultaneously allocate or free blocks from the same heap. There is a small performance cost to serialization, but it must be used whenever multiple threads allocate and free memory from the same heap. Setting the <b>HEAP_NO_SERIALIZE</b> value eliminates mutual exclusion on the heap. Without serialization, two or more threads that use the same heap handle might attempt to allocate or free memory simultaneously, likely causing corruption in the heap. The <b>HEAP_NO_SERIALIZE</b> value can, therefore, be safely used only in the following situations:

<ul>
<li>The process has only one thread.</li>
<li>The process has multiple threads, but only one thread calls the heap functions for a specific heap.</li>
<li>The process has multiple threads, and the application provides its own mechanism for mutual exclusion to a specific heap.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">Heap Functions</a>



<a href="https://msdn.microsoft.com/8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b">HeapCreate</a>



<a href="https://msdn.microsoft.com/036e95ff-f71f-49c3-8321-ed4c4bee5455">HeapValidate</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory
    Management Functions</a>
 

 

