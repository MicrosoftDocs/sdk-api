---
UID: NF:heapapi.HeapValidate
title: HeapValidate function
author: windows-driver-content
description: Validates the specified heap. The function scans all the memory blocks in the heap and verifies that the heap control structures maintained by the heap manager are in a consistent state.
old-location: base\heapvalidate.htm
old-project: Memory
ms.assetid: 036e95ff-f71f-49c3-8321-ed4c4bee5455
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: HEAP_NO_SERIALIZE, HeapValidate, HeapValidate function, _win32_heapvalidate, base.heapvalidate, heapapi/HeapValidate, winbase/HeapValidate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: GPMStarterGPOType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-heap-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-heap-l1-2-0.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	MinKernelBase.dll
api_name:
-	HeapValidate
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: GDI+ 1.1
---

# HeapValidate function


## -description


Validates the specified heap. The function scans all the memory blocks in the heap and verifies that the heap control structures maintained by the heap manager are in a consistent state. You can also use the 
<b>HeapValidate</b> function to validate a single memory block within a specified heap without checking the validity of the entire heap.


## -parameters




### -param hHeap [in]

A handle to the heap to be validated. This handle is returned by either the 
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
Serialized access will not be used. For more information, see Remarks.

To ensure that serialized access is disabled for all calls to this function, specify <b>HEAP_NO_SERIALIZE</b> in the call to <a href="https://msdn.microsoft.com/8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b">HeapCreate</a>. In this case, it is not necessary to additionally specify <b>HEAP_NO_SERIALIZE</b> in this function call.

This value should not be specified when accessing the process default heap. The system may create additional threads within the application's process, such as a CTRL+C handler, that simultaneously access the process default heap.

</td>
</tr>
</table>
 


### -param lpMem [in, optional]

A pointer to a memory block within the specified heap. This parameter may be <b>NULL</b>. 




If this parameter is <b>NULL</b>, the function attempts to validate the entire heap specified by <i>hHeap</i>.

If this parameter is not <b>NULL</b>, the function attempts to validate the memory block pointed to by <i>lpMem</i>. It does not attempt to validate the rest of the heap.


## -returns



If the specified heap or memory block is valid, the return value is nonzero.

If the specified heap or memory block is invalid, the return value is zero. On a system set up for debugging, the 
<b>HeapValidate</b> function then displays debugging messages that describe the part of the heap or memory block that is invalid, and stops at a hard-coded breakpoint so that you can examine the system to determine the source of the invalidity. The 
<b>HeapValidate</b> function does not set the thread's last error value. There is no extended error information for this function; do not call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>HeapValidate</b> function is primarily useful for debugging because validation is potentially time-consuming. Validating a heap can block other threads from accessing the heap and can degrade performance, especially on symmetric multiprocessing (SMP) computers. These side effects can last until <b>HeapValidate</b> returns. 

There are heap control structures for each memory block in a heap, and for the heap as a whole. When you use the 
<b>HeapValidate</b> function to validate a complete heap, it checks all of these control structures for consistency.

When you use 
<b>HeapValidate</b> to validate a single memory block within a heap, it checks only the control structures pertaining to that element. 
<b>HeapValidate</b> can only validate allocated memory blocks. Calling 
<b>HeapValidate</b> on a freed memory block will return <b>FALSE</b> because there are no control structures to validate.

If you want to validate the heap elements enumerated by the 
<a href="https://msdn.microsoft.com/ba4b7372-973b-4dea-9a93-faf847a047e5">HeapWalk</a> function, you should only call 
<b>HeapValidate</b> on the elements that have <b>PROCESS_HEAP_ENTRY_BUSY</b> in the <b>wFlags</b> member of the 
<a href="https://msdn.microsoft.com/e61b209a-9cc1-4171-9638-5456b0fcf775">PROCESS_HEAP_ENTRY</a> structure. 
<b>HeapValidate</b> returns <b>FALSE</b> for all heap elements that do not have this bit set.

Serialization ensures mutual exclusion when two or more threads attempt to simultaneously allocate or free blocks from the same heap. There is a small performance cost to serialization, but it must be used whenever multiple threads allocate and free memory from the same heap. Setting the <b>HEAP_NO_SERIALIZE</b> value eliminates mutual exclusion on the heap. Without serialization, two or more threads that use the same heap handle might attempt to allocate or free memory simultaneously, likely causing corruption in the heap. The <b>HEAP_NO_SERIALIZE</b> value can, therefore, be safely used only in the following situations:

<ul>
<li>The process has only one thread.</li>
<li>The process has multiple threads, but only one thread calls the heap functions for a specific heap.</li>
<li>The process has multiple threads, and the application provides its own mechanism for mutual exclusion to a specific heap.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">Heap Functions</a>



<a href="https://msdn.microsoft.com/8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b">HeapCreate</a>



<a href="https://msdn.microsoft.com/ba4b7372-973b-4dea-9a93-faf847a047e5">HeapWalk</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory
    Management Functions</a>



<a href="https://msdn.microsoft.com/e61b209a-9cc1-4171-9638-5456b0fcf775">PROCESS_HEAP_ENTRY</a>
 

 

