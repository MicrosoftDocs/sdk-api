---
UID: NF:winbase.LocalReAlloc
title: LocalReAlloc function (winbase.h)
description: Changes the size or the attributes of a specified local memory object. The size can increase or decrease.
helpviewer_keywords: ["LMEM_MOVEABLE","LMEM_ZEROINIT","LocalReAlloc","LocalReAlloc function","_win32_localrealloc","base.localrealloc","winbase/LocalReAlloc"]
old-location: base\localrealloc.htm
tech.root: base
ms.assetid: 88527ddd-e0c2-4a41-825e-d3a6df77fd2a
ms.date: 12/05/2018
ms.keywords: LMEM_MOVEABLE, LMEM_ZEROINIT, LocalReAlloc, LocalReAlloc function, _win32_localrealloc, base.localrealloc, winbase/LocalReAlloc
req.header: winbase.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LocalReAlloc
 - winbase/LocalReAlloc
dev_langs:
 - c++
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
 - API-MS-Win-Core-misc-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-Ms-Win-Core-Heap-L2-1-0.dll
api_name:
 - LocalReAlloc
---

# LocalReAlloc function


## -description

Changes the size or the attributes of a specified local memory object. The size can increase or decrease.
<div class="alert"><b>Note</b>  The local functions have greater overhead and provide fewer features than other memory management functions. New applications should use the <a href="/windows/desktop/Memory/heap-functions">heap functions</a> unless documentation states that a local function should be used. For more information, see <a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>.</div><div> </div>

## -parameters

### -param hMem [in]

A handle to the local memory object to be reallocated. This handle is returned by either the 
<a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a> or 
<b>LocalReAlloc</b> function.

### -param uBytes [in]

The new size of the memory block, in bytes. If <i>uFlags</i> specifies <b>LMEM_MODIFY</b>, this parameter is ignored.

### -param uFlags [in]

The reallocation options. If <b>LMEM_MODIFY</b> is specified, the function modifies the attributes of the memory object only (the <i>uBytes</i> parameter is ignored.) Otherwise, the function reallocates the memory object.

You can optionally combine <b>LMEM_MODIFY</b> with the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LMEM_MOVEABLE"></a><a id="lmem_moveable"></a><dl>
<dt><b>LMEM_MOVEABLE</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Allocates fixed or movable memory. 




If the memory is a locked <b>LMEM_MOVEABLE</b> memory block or a <b>LMEM_FIXED</b> memory block and this flag is not specified, the memory can only be reallocated in place.

</td>
</tr>
</table>
 

If this parameter does not specify <b>LMEM_MODIFY</b>, you can use the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LMEM_ZEROINIT"></a><a id="lmem_zeroinit"></a><dl>
<dt><b>LMEM_ZEROINIT</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
Causes the additional memory contents to be initialized to zero if the memory object is growing in size.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is a handle to the reallocated memory object.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If 
<b>LocalReAlloc</b> fails, the original memory is not freed, and the original handle and pointer are still valid.

If 
<b>LocalReAlloc</b> reallocates a fixed object, the value of the handle returned is the address of the first byte of the memory block. To access the memory, a process can simply cast the return value to a pointer.

## -see-also

<a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>



<a href="/windows/desktop/api/winbase/nf-winbase-locallock">LocalLock</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory
    Management Functions</a>