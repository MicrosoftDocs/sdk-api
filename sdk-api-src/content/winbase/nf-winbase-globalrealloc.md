---
UID: NF:winbase.GlobalReAlloc
title: GlobalReAlloc function (winbase.h)
description: Changes the size or attributes of a specified global memory object. The size can increase or decrease.
helpviewer_keywords: ["GMEM_MOVEABLE","GMEM_ZEROINIT","GlobalReAlloc","GlobalReAlloc function","_win32_globalrealloc","base.globalrealloc","winbase/GlobalReAlloc"]
old-location: base\globalrealloc.htm
tech.root: base
ms.assetid: 2439b16a-f27d-4e95-bc9e-6f1e563933c9
ms.date: 12/05/2018
ms.keywords: GMEM_MOVEABLE, GMEM_ZEROINIT, GlobalReAlloc, GlobalReAlloc function, _win32_globalrealloc, base.globalrealloc, winbase/GlobalReAlloc
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
 - GlobalReAlloc
 - winbase/GlobalReAlloc
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
api_name:
 - GlobalReAlloc
---

# GlobalReAlloc function


## -description

Changes the size or attributes of a specified global memory object. The size can increase or decrease.
<div class="alert"><b>Note</b>  The global functions have greater overhead and provide fewer features than other memory management functions. New applications should use the <a href="/windows/desktop/Memory/heap-functions">heap functions</a> unless documentation states that a global function should be used. For more information, see <a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>.
</div><div> </div>

## -parameters

### -param hMem [in]

A handle to the global memory object to be reallocated. This handle is returned by either the 
<a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a> or 
<b>GlobalReAlloc</b> function.

### -param dwBytes [in]

The new size of the memory block, in bytes. If <i>uFlags</i> specifies <b>GMEM_MODIFY</b>, this parameter is ignored.

### -param uFlags [in]

The reallocation options. If <b>GMEM_MODIFY</b> is specified, the function modifies the attributes of the memory object only (the <i>dwBytes</i> parameter is ignored.) Otherwise, the function reallocates the memory object.

You can optionally combine <b>GMEM_MODIFY</b> with the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GMEM_MOVEABLE"></a><a id="gmem_moveable"></a><dl>
<dt><b>GMEM_MOVEABLE</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Allocates movable memory.

If the memory is a locked <b>GMEM_MOVEABLE</b> memory block or a <b>GMEM_FIXED</b> memory block and this flag is not specified, the memory can only be reallocated in place.

</td>
</tr>
</table>
 

If this parameter does not specify <b>GMEM_MODIFY</b>, you can use the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GMEM_ZEROINIT"></a><a id="gmem_zeroinit"></a><dl>
<dt><b>GMEM_ZEROINIT</b></dt>
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

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If 
<b>GlobalReAlloc</b> reallocates a movable object, the return value is a handle to the memory object. To convert the handle to a pointer, use the 
<a href="/windows/desktop/api/winbase/nf-winbase-globallock">GlobalLock</a> function.

If 
<b>GlobalReAlloc</b> reallocates a fixed object, the value of the handle returned is the address of the first byte of the memory block. To access the memory, a process can simply cast the return value to a pointer.

If 
<b>GlobalReAlloc</b> fails, the original memory is not freed, and the original handle and pointer are still valid.

## -see-also

<a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globaldiscard">GlobalDiscard</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globallock">GlobalLock</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory
    Management Functions</a>