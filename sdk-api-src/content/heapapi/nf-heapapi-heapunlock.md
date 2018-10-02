---
UID: NF:heapapi.HeapUnlock
title: HeapUnlock function
author: windows-sdk-content
description: Releases ownership of the critical section object, or lock, that is associated with a specified heap.
old-location: base\heapunlock.htm
tech.root: Memory
ms.assetid: c1a7b2c8-293e-4e07-a654-fd10b2f0ef39
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: HeapUnlock, HeapUnlock function, _win32_heapunlock, base.heapunlock, heapapi/HeapUnlock, winbase/HeapUnlock
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
 - HeapUnlock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# HeapUnlock function


## -description


Releases ownership of the critical section object, or lock, that is associated with a specified heap. It reverses the action of the 
<a href="https://msdn.microsoft.com/bc01b82d-ef10-40d7-af82-e599ba825944">HeapLock</a> function.


## -parameters




### -param hHeap [in]

A handle to the heap to be unlocked. This handle is returned by either the 
<a href="https://msdn.microsoft.com/8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b">HeapCreate</a> or 
<a href="https://msdn.microsoft.com/ecd716b2-df48-4914-9de4-47d8ad8ff9a2">GetProcessHeap</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<a href="https://msdn.microsoft.com/bc01b82d-ef10-40d7-af82-e599ba825944">HeapLock</a> function is primarily useful for preventing the allocation and release of heap memory by other threads while the calling thread uses the 
<a href="https://msdn.microsoft.com/ba4b7372-973b-4dea-9a93-faf847a047e5">HeapWalk</a> function. The 
<b>HeapUnlock</b> function is the inverse of 
<b>HeapLock</b>.

Each call to 
<a href="https://msdn.microsoft.com/bc01b82d-ef10-40d7-af82-e599ba825944">HeapLock</a> must be matched by a corresponding call to the 
<b>HeapUnlock</b> function. Failure to call 
<b>HeapUnlock</b> will block the execution of any other threads of the calling process that attempt to access the heap.

If the <b>HeapUnlock</b> function is called on a heap created with the <a href="https://msdn.microsoft.com/8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b">HEAP_NO_SERIALIZATION</a> flag, the results are undefined.


#### Examples


<a href="https://msdn.microsoft.com/ef37d644-473f-4e51-9785-5b44fe0dce42">Enumerating a Heap</a>


<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">Heap Functions</a>



<a href="https://msdn.microsoft.com/bc01b82d-ef10-40d7-af82-e599ba825944">HeapLock</a>



<a href="https://msdn.microsoft.com/ba4b7372-973b-4dea-9a93-faf847a047e5">HeapWalk</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory
		  Management Functions</a>
 

 

