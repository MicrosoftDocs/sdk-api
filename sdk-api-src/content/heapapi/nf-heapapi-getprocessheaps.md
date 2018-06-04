---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

