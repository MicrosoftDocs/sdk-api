---
UID: NF:memoryapi.UnmapViewOfFile2
title: UnmapViewOfFile2 function (memoryapi.h)
author: windows-sdk-content
description: Unmaps a previously mapped view of a file or a pagefile-backed section.
old-location: base\unmapviewoffile2.htm
tech.root: Memory
ms.assetid: 300BA329-1E56-4C0F-81FC-FED42FCE9EB7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MEM_PRESERVE_PLACEHOLDER, MEM_UNMAP_WITH_TRANSIENT_BOOST, UnmapViewOfFile2, UnmapViewOfFile2 function, base.unmapviewoffile2, winbase/UnmapViewOfFile2
ms.topic: function
req.header: memoryapi.h
req.include-header: Windows.h, Memoryapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
api_name:
 - UnmapViewOfFile2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UnmapViewOfFile2 function


## -description


Unmaps a previously mapped view of a file or a
    pagefile-backed section.


## -parameters




### -param Process [in]

A <b>HANDLE</b> to the process from which the section
                    will be unmapped.


### -param BaseAddress [in]

The base address of a previously mapped
                  view that is to be unmapped.  This value must be
                  identical to the value returned by a previous call
                  to <a href="https://msdn.microsoft.com/D97138F0-2FB3-488A-91AC-A654B22FE9AD">MapViewOfFile2</a>.


### -param UnmapFlags [in]

This parameter can be zero (0) or one of the following values.

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
Unmaps a mapped view back to a placeholder (after you've replaced a placeholder with a mapped view using <a href="https://msdn.microsoft.com/D97138F0-2FB3-488A-91AC-A654B22FE9AD">MapViewOfFile2</a> or <b>MapViewOfFile2FromApp</b>).

</td>
</tr>
</table>
 


## -returns



Returns <b>TRUE</b> if sucessful. Otherwise, returns <b>FALSE</b> and extended error status is available
            using <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/D97138F0-2FB3-488A-91AC-A654B22FE9AD">MapViewOfFile2</a>



<a href="https://msdn.microsoft.com/2e9c3174-af48-4fa3-9f6a-fb62b23ed994">UnmapViewOfFile</a>



<a href="https://msdn.microsoft.com/1C86075D-17B8-481E-BDF0-6E5A8F55C188">UnmapViewOfFileEx</a>
 

 

