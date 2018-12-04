---
UID: NF:tlhelp32.Heap32ListFirst
title: Heap32ListFirst function
author: windows-sdk-content
description: Retrieves information about the first heap that has been allocated by a specified process.
old-location: toolhelp\heap32listfirst.htm
tech.root: ToolHelp
ms.assetid: b9a2992b-0dc1-41c3-aa23-796def674831
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Heap32ListFirst, Heap32ListFirst function [ToolHelp], _win32_heap32listfirst, base.heap32listfirst, tlhelp32/Heap32ListFirst, toolhelp.heap32listfirst
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
 - Heap32ListFirst
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Heap32ListFirst function


## -description


Retrieves information about the first heap that has been allocated by a specified process.


## -parameters




### -param hSnapshot [in]

A handle to the snapshot returned from a previous call to the 
<a href="https://msdn.microsoft.com/df643c25-7558-424c-b187-b3f86ba51358">CreateToolhelp32Snapshot</a> function.


### -param lphl [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/61e01d23-9f15-44c5-9f6d-45df4809ccad">HEAPLIST32</a> structure.


## -returns



Returns <b>TRUE</b> if the first entry of the heap list has been copied to the buffer or <b>FALSE</b> otherwise. The <b>ERROR_NO_MORE_FILES</b> error value is returned by the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function when no heap list exists or the snapshot does not contain heap list information.




## -remarks



The calling application must set the <b>dwSize</b> member of 
<a href="https://msdn.microsoft.com/c5f1dc66-d44f-4491-b0b7-961b163d0f1f">HEAPLIST32</a> to the size, in bytes, of the structure. 
<b>Heap32ListFirst</b> changes <b>dwSize</b> to the number of bytes written to the structure. This will never be greater than the initial value of <b>dwSize</b>, but it may be smaller. If the value is smaller, do not rely on the values of any members whose offsets are greater than this value.

To retrieve information about other heaps in the heap list, use the 
<a href="https://msdn.microsoft.com/bb4d573c-a82f-48ac-be22-440d6a1d0c9c">Heap32ListNext</a> function.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/cfa1d2a4-fec0-4089-9351-e0a26f9ecfe3">Traversing the Heap List</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/df643c25-7558-424c-b187-b3f86ba51358">CreateToolhelp32Snapshot</a>



<a href="https://msdn.microsoft.com/61e01d23-9f15-44c5-9f6d-45df4809ccad">HEAPLIST32</a>



<a href="https://msdn.microsoft.com/631096fd-cb2c-4b19-aa71-d47060e2715c">Heap Lists and Heap Walking</a>



<a href="https://msdn.microsoft.com/bb4d573c-a82f-48ac-be22-440d6a1d0c9c">Heap32ListNext</a>



<a href="https://msdn.microsoft.com/83732bd6-f4cf-409d-ad17-86503d408dc3">Tool Help Functions</a>
 

 

