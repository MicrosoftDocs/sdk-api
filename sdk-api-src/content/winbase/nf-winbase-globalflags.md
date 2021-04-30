---
UID: NF:winbase.GlobalFlags
title: GlobalFlags function (winbase.h)
description: Retrieves information about the specified global memory object.
helpviewer_keywords: ["GlobalFlags","GlobalFlags function","_win32_globalflags","base.globalflags","winbase/GlobalFlags"]
old-location: base\globalflags.htm
tech.root: base
ms.assetid: 647fc9a2-0522-42ab-ab8b-43c648f27d90
ms.date: 12/05/2018
ms.keywords: GlobalFlags, GlobalFlags function, _win32_globalflags, base.globalflags, winbase/GlobalFlags
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GlobalFlags
 - winbase/GlobalFlags
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
 - GlobalFlags
---

# GlobalFlags function


## -description

Retrieves information about the specified global memory object.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. New applications should use the  <a href="/windows/desktop/Memory/heap-functions">heap functions</a>. For more information, see Remarks. 
</div><div> </div>

## -parameters

### -param hMem [in]

A handle to the global memory object. This handle is returned by either the 
<a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-globalrealloc">GlobalReAlloc</a> function.

## -returns

If the function succeeds, the return value specifies the allocation values and the lock count for the memory object.

If the function fails, the return value is <b>GMEM_INVALID_HANDLE</b>, indicating that the global handle is not valid. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The low-order byte of the low-order word of the return value contains the lock count of the object. To retrieve the lock count from the return value, use the <b>GMEM_LOCKCOUNT</b> mask with the bitwise AND (&amp;) operator. The lock count of memory objects allocated with <b>GMEM_FIXED</b> is always zero.

The high-order byte of the low-order word of the return value indicates the allocation values of the memory object. It can be zero or <b>GMEM_DISCARDED</b>.

The global functions have greater overhead and provide fewer features than other memory management functions. New applications should use the <a href="/windows/desktop/Memory/heap-functions">heap functions</a> unless documentation states that a global function should be used. For more information, see <a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>.

## -see-also

<a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globaldiscard">GlobalDiscard</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalrealloc">GlobalReAlloc</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory
    Management Functions</a>