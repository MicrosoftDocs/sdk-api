---
UID: NF:winbase.LocalSize
title: LocalSize function
author: windows-sdk-content
description: Retrieves the current size of the specified local memory object, in bytes.
old-location: base\localsize.htm
old-project: Memory
ms.assetid: d1337845-d89c-4cd5-a584-36fe0c682c1a
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: LocalSize, LocalSize function, _win32_localsize, base.localsize, winbase/LocalSize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
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
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Heap-Obsolete-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
api_name:
 - LocalSize
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# LocalSize function


## -description


Retrieves the current size of the specified local memory object, in bytes.
<div class="alert"><b>Note</b>  The local functions have greater overhead and provide fewer features than other memory management functions. New applications should use the <a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">heap functions</a> unless documentation states that a local function should be used. For more information, see <a href="https://msdn.microsoft.com/97707ce7-4c65-4d0e-ba69-47fdaee73a9b">Global and Local Functions</a>.</div><div> </div>

## -parameters




### -param hMem [in]

A handle to the local memory object. This handle is returned by the 
<a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a>, 
<a href="https://msdn.microsoft.com/88527ddd-e0c2-4a41-825e-d3a6df77fd2a">LocalReAlloc</a>, or 
<a href="https://msdn.microsoft.com/2b252f8b-d0a3-4d7f-9e2e-cb80c1512935">LocalHandle</a> function.


## -returns



If the function succeeds, the return value is the size of the specified local memory object, in bytes. If the specified handle is not valid or if the object has been discarded, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The size of a memory block may be larger than the size requested when the memory was allocated.

To verify that the specified object's memory block has not been discarded, call the 
<a href="https://msdn.microsoft.com/4804c8c3-6c0b-4f62-87ab-f64b23fff8b9">LocalFlags</a> function before calling 
<b>LocalSize</b>.




## -see-also




<a href="https://msdn.microsoft.com/97707ce7-4c65-4d0e-ba69-47fdaee73a9b">Global and Local Functions</a>



<a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a>



<a href="https://msdn.microsoft.com/4804c8c3-6c0b-4f62-87ab-f64b23fff8b9">LocalFlags</a>



<a href="https://msdn.microsoft.com/2b252f8b-d0a3-4d7f-9e2e-cb80c1512935">LocalHandle</a>



<a href="https://msdn.microsoft.com/88527ddd-e0c2-4a41-825e-d3a6df77fd2a">LocalReAlloc</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory
		  Management Functions</a>
 

 

