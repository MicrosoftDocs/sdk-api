---
UID: NF:heapapi.HeapWalk
title: HeapWalk function
author: windows-sdk-content
description: Enumerates the memory blocks in the specified heap.
old-location: base\heapwalk.htm
tech.root: Memory
ms.assetid: ba4b7372-973b-4dea-9a93-faf847a047e5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: HeapWalk, HeapWalk function, _win32_heapwalk, base.heapwalk, heapapi/HeapWalk, winbase/HeapWalk
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
 - HeapWalk
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# HeapWalk function


## -description


Enumerates the memory blocks in the specified heap.


## -parameters




### -param hHeap [in]

A handle to the heap. This handle is returned by either the 
      <a href="https://msdn.microsoft.com/8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b">HeapCreate</a> or 
      <a href="https://msdn.microsoft.com/ecd716b2-df48-4914-9de4-47d8ad8ff9a2">GetProcessHeap</a> function.


### -param lpEntry [in, out]

A pointer to a <a href="https://msdn.microsoft.com/e61b209a-9cc1-4171-9638-5456b0fcf775">PROCESS_HEAP_ENTRY</a> structure 
       that maintains state information for a particular heap enumeration.

If the <b>HeapWalk</b> function succeeds, returning the value 
       <b>TRUE</b>, this structure's members contain information about the next memory block in the 
       heap.

To initiate a heap enumeration, set the <b>lpData</b> field of the 
       <a href="https://msdn.microsoft.com/e61b209a-9cc1-4171-9638-5456b0fcf775">PROCESS_HEAP_ENTRY</a> structure to 
       <b>NULL</b>. To continue a particular heap enumeration, call the 
       <b>HeapWalk</b> function repeatedly, with no changes to 
       <i>hHeap</i>, <i>lpEntry</i>, or any of the members of the 
       <b>PROCESS_HEAP_ENTRY</b> structure.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If the heap enumeration terminates successfully by reaching the end of the heap, the function returns 
       <b>FALSE</b>, and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> 
       returns the error code <b>ERROR_NO_MORE_ITEMS</b>.




## -remarks



The <b>HeapWalk</b> function is primarily useful for debugging 
    because enumerating a heap is a potentially time-consuming operation. Locking the heap during enumeration blocks 
    other threads from accessing the heap and can degrade performance, especially on symmetric multiprocessing (SMP) 
    computers. The side effects can last until the heap is unlocked. Use the 
    <a href="https://msdn.microsoft.com/bc01b82d-ef10-40d7-af82-e599ba825944">HeapLock</a> and 
    <a href="https://msdn.microsoft.com/c1a7b2c8-293e-4e07-a654-fd10b2f0ef39">HeapUnlock</a> functions to control heap locking during heap 
    enumeration.

To initiate a heap enumeration, call <b>HeapWalk</b> with the 
    <b>lpData</b> field of the 
    <a href="https://msdn.microsoft.com/e61b209a-9cc1-4171-9638-5456b0fcf775">PROCESS_HEAP_ENTRY</a> structure pointed to by 
    <i>lpEntry</i> set to <b>NULL</b>.

To continue a heap enumeration, call <b>HeapWalk</b> with the same 
    <i>hHeap</i> and <i>lpEntry</i> values, and with the 
    <a href="https://msdn.microsoft.com/e61b209a-9cc1-4171-9638-5456b0fcf775">PROCESS_HEAP_ENTRY</a> structure unchanged from the 
    preceding call to <b>HeapWalk</b>. Repeat this process until you 
    have no need for further enumeration, or until the function returns <b>FALSE</b> and 
    <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns 
    <b>ERROR_NO_MORE_ITEMS</b>, indicating that all of the heap's memory blocks have been 
    enumerated.

No special call of <b>HeapWalk</b> is needed to terminate the 
    heap enumeration, since no enumeration state data is maintained outside the contents of the 
    <a href="https://msdn.microsoft.com/e61b209a-9cc1-4171-9638-5456b0fcf775">PROCESS_HEAP_ENTRY</a> structure.

<b>HeapWalk</b> can fail in a multithreaded application if the 
    heap is not locked during the heap enumeration.


#### Examples


<a href="https://msdn.microsoft.com/ef37d644-473f-4e51-9785-5b44fe0dce42">Enumerating a Heap</a>


<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">Heap Functions</a>



<a href="https://msdn.microsoft.com/bc01b82d-ef10-40d7-af82-e599ba825944">HeapLock</a>



<a href="https://msdn.microsoft.com/21d711d9-3b16-4537-a830-1a2fa049a471">HeapReAlloc</a>



<a href="https://msdn.microsoft.com/c1a7b2c8-293e-4e07-a654-fd10b2f0ef39">HeapUnlock</a>



<a href="https://msdn.microsoft.com/036e95ff-f71f-49c3-8321-ed4c4bee5455">HeapValidate</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory Management Functions</a>



<a href="https://msdn.microsoft.com/e61b209a-9cc1-4171-9638-5456b0fcf775">PROCESS_HEAP_ENTRY</a>
 

 

