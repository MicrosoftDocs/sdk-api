---
UID: NF:heapapi.GetProcessHeap
title: GetProcessHeap function (heapapi.h)
description: Retrieves a handle to the default heap of the calling process.helpviewer_keywords: ["GetProcessHeap","GetProcessHeap function","_win32_getprocessheap","base.getprocessheap","heapapi/GetProcessHeap","winbase/GetProcessHeap"]
old-location: base\getprocessheap.htm
tech.root: Memory
ms.assetid: ecd716b2-df48-4914-9de4-47d8ad8ff9a2
ms.date: 12/05/2018
ms.keywords: GetProcessHeap, GetProcessHeap function, _win32_getprocessheap, base.getprocessheap, heapapi/GetProcessHeap, winbase/GetProcessHeap
f1_keywords:
- heapapi/GetProcessHeap
dev_langs:
- c++
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
- vertdll.dll
api_name:
- GetProcessHeap
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetProcessHeap function


## -description


Retrieves a handle to the default heap of the calling process. This handle can then be used in subsequent calls to the heap functions.


## -parameters






## -returns



If the function succeeds, the return value is a handle to the calling process's heap.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The 
<b>GetProcessHeap</b> function obtains a handle to the default heap for the calling process. A process can use this handle to allocate memory from the process heap without having to first create a private heap using the 
<a href="https://docs.microsoft.com/windows/desktop/api/heapapi/nf-heapapi-heapcreate">HeapCreate</a> function.

<b>Windows Server 2003 and Windows XP:  </b>To enable the low-fragmentation heap for the default heap of the process, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/heapapi/nf-heapapi-heapsetinformation">HeapSetInformation</a> function with the handle returned by <b>GetProcessHeap</b>.


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/Memory/getting-process-heaps">Getting Process Heaps</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Memory/heap-functions">Heap Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/heapapi/nf-heapapi-heapcreate">HeapCreate</a>



<a href="https://docs.microsoft.com/windows/desktop/Memory/memory-management-functions">Memory
		  Management Functions</a>
 

 

