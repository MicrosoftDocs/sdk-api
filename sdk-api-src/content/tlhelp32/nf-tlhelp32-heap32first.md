---
UID: NF:tlhelp32.Heap32First
title: Heap32First function
author: windows-sdk-content
description: Retrieves information about the first block of a heap that has been allocated by a process.
old-location: toolhelp\heap32first.htm
tech.root: ToolHelp
ms.assetid: 79d01e3a-b11b-46b5-99d0-b445000288a7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Heap32First, Heap32First function [ToolHelp], _win32_heap32first, base.heap32first, tlhelp32/Heap32First, toolhelp.heap32first
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: tlhelp32.h
req.include-header: 
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
 - API-MS-Win-Core-ToolHelp-L1-1-1.dll
 - Kernel32Legacy.dll
api_name:
 - Heap32First
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Heap32First function


## -description


Retrieves information about the first block of a heap that has been allocated by a process.


## -parameters




### -param lphe [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/c5f1dc66-d44f-4491-b0b7-961b163d0f1f">HEAPENTRY32</a> structure.


### -param th32ProcessID [in]

The identifier of the process context that owns the heap.


### -param th32HeapID [in]

The identifier of the heap to be enumerated.


## -returns



Returns <b>TRUE</b> if information for the first heap block has been copied to the buffer or <b>FALSE</b> otherwise. The <b>ERROR_NO_MORE_FILES</b> error value is returned by the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function if the heap is invalid or empty.




## -remarks



The calling application must set the <b>dwSize</b> member of 
<a href="https://msdn.microsoft.com/c5f1dc66-d44f-4491-b0b7-961b163d0f1f">HEAPENTRY32</a> to the size, in bytes, of the structure. 
<b>Heap32First</b> changes <b>dwSize</b> to the number of bytes written to the structure. This will never be greater than the initial value of <b>dwSize</b>, but it may be smaller. If the value is smaller, do not rely on the values of any members whose offsets are greater than this value.

To access subsequent blocks of the same heap, use the 
<a href="https://msdn.microsoft.com/cc3becd0-edba-47cf-ac2d-26a5d98390e7">Heap32Next</a> function.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/cfa1d2a4-fec0-4089-9351-e0a26f9ecfe3">Traversing the Heap List</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/c5f1dc66-d44f-4491-b0b7-961b163d0f1f">HEAPENTRY32</a>



<a href="https://msdn.microsoft.com/631096fd-cb2c-4b19-aa71-d47060e2715c">Heap Lists and Heap Walking</a>



<a href="https://msdn.microsoft.com/cc3becd0-edba-47cf-ac2d-26a5d98390e7">Heap32Next</a>



<a href="https://msdn.microsoft.com/83732bd6-f4cf-409d-ad17-86503d408dc3">Tool Help Functions</a>
 

 

