---
UID: NF:heapapi.HeapDestroy
title: HeapDestroy function
author: windows-sdk-content
description: Destroys the specified heap object. It decommits and releases all the pages of a private heap object, and it invalidates the handle to the heap.
old-location: base\heapdestroy.htm
old-project: memory
ms.assetid: 2ad8d15f-de5e-424d-9349-3baccb000a36
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: HeapDestroy, HeapDestroy function, _win32_heapdestroy, base.heapdestroy, heapapi/HeapDestroy, winbase/HeapDestroy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: heapapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: GPMStarterGPOType
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
 - HeapDestroy
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: GDI+ 1.1
---

# HeapDestroy function


## -description


Destroys the specified heap object. 
It decommits and releases all the pages of a private heap object, and it invalidates the handle to the heap.


## -parameters




### -param hHeap [in]

A handle to the heap to be destroyed. This handle is returned by the 
<a href="https://msdn.microsoft.com/8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b">HeapCreate</a> function. Do not use the handle to the process heap returned by the 
<a href="https://msdn.microsoft.com/ecd716b2-df48-4914-9de4-47d8ad8ff9a2">GetProcessHeap</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Processes can call 
<b>HeapDestroy</b> without first calling the 
<a href="https://msdn.microsoft.com/6139e55f-9dda-42b5-bc9b-8d9bbfeaa619">HeapFree</a> function to free memory allocated from the heap.


#### Examples


<a href="https://msdn.microsoft.com/ef37d644-473f-4e51-9785-5b44fe0dce42">Enumerating a Heap</a>


<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">Heap Functions</a>



<a href="https://msdn.microsoft.com/8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b">HeapCreate</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory
		  Management Functions</a>
 

 

