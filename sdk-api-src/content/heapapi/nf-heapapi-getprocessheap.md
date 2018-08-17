---
UID: NF:heapapi.GetProcessHeap
title: GetProcessHeap function
author: windows-sdk-content
description: Retrieves a handle to the default heap of the calling process.
old-location: base\getprocessheap.htm
old-project: memory
ms.assetid: ecd716b2-df48-4914-9de4-47d8ad8ff9a2
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: GetProcessHeap, GetProcessHeap function, _win32_getprocessheap, base.getprocessheap, heapapi/GetProcessHeap, winbase/GetProcessHeap
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: heapapi.h
req.include-header: Windows.h
req.redist: 
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
 - GetProcessHeap
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetProcessHeap function


## -description


Retrieves a handle to the default heap of the calling process. This handle can then be used in subsequent calls to the heap functions.


## -parameters






## -returns



If the function succeeds, the return value is a handle to the calling process's heap.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>GetProcessHeap</b> function obtains a handle to the default heap for the calling process. A process can use this handle to allocate memory from the process heap without having to first create a private heap using the 
<a href="https://msdn.microsoft.com/8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b">HeapCreate</a> function.

<b>Windows Server 2003 and Windows XP:  </b>To enable the low-fragmentation heap for the default heap of the process, call the 
<a href="https://msdn.microsoft.com/33c262ca-5093-4f44-a8c6-09045bc90f60">HeapSetInformation</a> function with the handle returned by <b>GetProcessHeap</b>.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/00f69593-f03b-4f30-aeec-db3fda0ac356">Getting Process Heaps</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">Heap Functions</a>



<a href="https://msdn.microsoft.com/8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b">HeapCreate</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory
		  Management Functions</a>
 

 

