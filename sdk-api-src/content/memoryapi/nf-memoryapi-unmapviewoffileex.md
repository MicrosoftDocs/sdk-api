---
UID: NF:memoryapi.UnmapViewOfFileEx
title: UnmapViewOfFileEx function
author: windows-sdk-content
description: This is an extended version of UnmapViewOfFile that takes an additional flags parameter.
old-location: base\unmapviewoffileex.htm
tech.root: Memory
ms.assetid: 1C86075D-17B8-481E-BDF0-6E5A8F55C188
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: MEM_PRESERVE_PLACEHOLDER, MEM_UNMAP_WITH_TRANSIENT_BOOST, UnmapViewOfFileEx, UnmapViewOfFileEx function, base.unmapviewoffileex, winbase/UnmapViewOfFileEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: memoryapi.h
req.include-header: Windows.h, Memoryapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - API-MS-Win-Core-memory-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-1.dll
 - API-MS-Win-Core-memory-l1-1-2.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - UnmapViewOfFileEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- UnmapViewOfFileEx
: 
---

# UnmapViewOfFileEx function


## -description


This is an extended version of <a href="https://msdn.microsoft.com/2e9c3174-af48-4fa3-9f6a-fb62b23ed994">UnmapViewOfFile</a> that takes an additional flags parameter.


## -parameters




### -param BaseAddress [in]

A pointer to the base address of the mapped view of a file that is to be unmapped. This value must be identical to the value returned by a previous call to the 
<a href="https://msdn.microsoft.com/df9f54cd-b2de-4107-a1c5-d5a07045851e">MapViewOfFile</a> or 
<a href="https://msdn.microsoft.com/2ac8a7d6-5c52-41de-acb9-d7f975fd2a94">MapViewOfFileEx</a> function.


### -param UnmapFlags [in]

This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MEM_UNMAP_WITH_TRANSIENT_BOOST"></a><a id="mem_unmap_with_transient_boost"></a><dl>
<dt><b>MEM_UNMAP_WITH_TRANSIENT_BOOST</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Specifies that the priority of the pages being unmapped should be temporarily boosted
                 (with automatic short term decay) because the caller expects that these pages will be accessed again shortly from another thread. For more information about memory priorities, see the <a href="https://msdn.microsoft.com/c0159bea-870a-46b7-a350-91fe52efae49">SetThreadInformation(ThreadMemoryPriority)</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="MEM_PRESERVE_PLACEHOLDER"></a><a id="mem_preserve_placeholder"></a><dl>
<dt><b>MEM_PRESERVE_PLACEHOLDER</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Unmaps a mapped view back to a placeholder (after you've replaced a placeholder with a mapped view using <a href="https://msdn.microsoft.com/D97138F0-2FB3-488A-91AC-A654B22FE9AD">MapViewOfFile2</a> or <a href="base.mapviewoffile2fromapp">MapViewOfFile2FromApp</a>).

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



For more information about the behavior of this function, see the <a href="https://msdn.microsoft.com/2e9c3174-af48-4fa3-9f6a-fb62b23ed994">UnmapViewOfFile</a> function.



