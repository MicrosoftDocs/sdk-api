---
UID: NF:memoryapi.UnmapViewOfFileEx
title: UnmapViewOfFileEx function (memoryapi.h)
description: This is an extended version of UnmapViewOfFile that takes an additional flags parameter.
helpviewer_keywords: ["MEM_PRESERVE_PLACEHOLDER","MEM_UNMAP_WITH_TRANSIENT_BOOST","UnmapViewOfFileEx","UnmapViewOfFileEx function","base.unmapviewoffileex","winbase/UnmapViewOfFileEx"]
old-location: base\unmapviewoffileex.htm
tech.root: base
ms.assetid: 1C86075D-17B8-481E-BDF0-6E5A8F55C188
ms.date: 12/05/2018
ms.keywords: MEM_PRESERVE_PLACEHOLDER, MEM_UNMAP_WITH_TRANSIENT_BOOST, UnmapViewOfFileEx, UnmapViewOfFileEx function, base.unmapviewoffileex, winbase/UnmapViewOfFileEx
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
req.lib: onecore.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UnmapViewOfFileEx
 - memoryapi/UnmapViewOfFileEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-memory-l1-1-9.dll
 - api-ms-win-core-memory-l1-1-8.dll
 - api-ms-win-core-memory-l1-1-7.dll
 - api-ms-win-core-memory-l1-1-6.dll
 - api-ms-win-core-memory-l1-1-5.dll
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
---

# UnmapViewOfFileEx function


## -description

This is an extended version of <a href="/windows/desktop/api/memoryapi/nf-memoryapi-unmapviewoffile">UnmapViewOfFile</a> that takes an additional flags parameter.

## -parameters

### -param BaseAddress [in]

A pointer to the base address of the mapped view of a file that is to be unmapped. This value must be identical to the value returned by a previous call
to one of the functions in the
<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a> family.

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
                 (with automatic short term decay) because the caller expects that these pages will be accessed again shortly from another thread. For more information about memory priorities, see the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadinformation">SetThreadInformation(ThreadMemoryPriority)</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="MEM_PRESERVE_PLACEHOLDER"></a><a id="mem_preserve_placeholder"></a><dl>
<dt><b>MEM_PRESERVE_PLACEHOLDER</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Unmaps a mapped view back to a placeholder (after you've replaced a placeholder with a mapped view using <a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile3">MapViewOfFile3</a> or <b>MapViewOfFile3FromApp</b>).

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

For more information about the behavior of this function, see the <a href="/windows/desktop/api/memoryapi/nf-memoryapi-unmapviewoffile">UnmapViewOfFile</a> function.