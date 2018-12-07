---
UID: NF:heapapi.GetProcessHeaps
title: GetProcessHeaps function
author: windows-sdk-content
description: Returns the number of active heaps and retrieves handles to all of the active heaps for the calling process.
old-location: base\getprocessheaps.htm
tech.root: memory
ms.assetid: 6287c74d-5987-44ec-8b6f-2d5a08338877
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetProcessHeaps, GetProcessHeaps function, _win32_getprocessheaps, base.getprocessheaps, heapapi/GetProcessHeaps, winbase/GetProcessHeaps
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
 - GetProcessHeaps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetProcessHeaps function


## -description


Returns the number of active heaps and retrieves handles to all of the active heaps for the calling process.


## -parameters




### -param NumberOfHeaps [in]

The maximum number of heap handles that can be stored into the buffer pointed to by <i>ProcessHeaps</i>.


### -param ProcessHeaps [out]

A pointer to a buffer that receives an array of heap handles.


## -returns



The return value is the number of handles to heaps that are active for the calling process.

If the return value is less than or equal to <i>NumberOfHeaps</i>, the function has stored that number of heap handles in the buffer pointed to by <i>ProcessHeaps</i>.

If the return value is greater than <i>NumberOfHeaps</i>, the buffer pointed to by <i>ProcessHeaps</i> is too small to hold all the heap handles for the calling process, and the function stores <i>NumberOfHeaps</i> handles in the buffer. Use the return value to allocate a buffer that is large enough to receive all of the handles, and call the function again.

If the return value is zero, the function has failed because every process has at least one active heap, the default heap for the  process. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>GetProcessHeaps</b> function obtains a handle to the default heap of the calling process, plus handles to any additional private heaps  created by calling the 
<a href="https://msdn.microsoft.com/8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b">HeapCreate</a> function on any thread in the process. 

The <b>GetProcessHeaps</b> function is primarily useful for debugging, because some of the private heaps retrieved by the function may have been created by other code running in the process and may be destroyed after <b>GetProcessHeaps</b> returns. Destroying a heap invalidates the handle to the heap, and continued use of such handles can cause undefined behavior in the application. Heap functions should be called only on the default heap of the calling process and on private heaps that the process creates and manages. 

To obtain a handle to the process heap of the calling process, use the 
<a href="https://msdn.microsoft.com/ecd716b2-df48-4914-9de4-47d8ad8ff9a2">GetProcessHeap</a> function.  


#### Examples

For an example, see <a href="https://msdn.microsoft.com/00f69593-f03b-4f30-aeec-db3fda0ac356">Getting Process Heaps</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/ecd716b2-df48-4914-9de4-47d8ad8ff9a2">GetProcessHeap</a>



<a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">Heap Functions</a>



<a href="https://msdn.microsoft.com/8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b">HeapCreate</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory
		  Management Functions</a>
 

 

