---
UID: NF:winbase.GlobalSize
title: GlobalSize function (winbase.h)
description: Retrieves the current size of the specified global memory object, in bytes.
helpviewer_keywords: ["GlobalSize","GlobalSize function","_win32_globalsize","base.globalsize","winbase/GlobalSize"]
old-location: base\globalsize.htm
tech.root: base
ms.assetid: 9fd01460-d6fc-41f4-9e0c-209a3d1844c1
ms.date: 12/05/2018
ms.keywords: GlobalSize, GlobalSize function, _win32_globalsize, base.globalsize, winbase/GlobalSize
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
 - GlobalSize
 - winbase/GlobalSize
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
 - GlobalSize
---

# GlobalSize function


## -description

Retrieves the current size of the specified global memory object, in bytes.
<div class="alert"><b>Note</b>  The global functions have greater overhead and provide fewer features than other memory management functions. New applications should use the <a href="/windows/desktop/Memory/heap-functions">heap functions</a> unless documentation states that a global function should be used. For more information, see <a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>.
</div><div> </div>

## -parameters

### -param hMem [in]

Type: **HGLOBAL**

A handle to the global memory object. This handle is returned by either the 
<a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-globalrealloc">GlobalReAlloc</a> function.

## -returns

Type: **SIZE_T**

If the function succeeds, the return value is the size of the specified global memory object, in bytes.

If the specified handle is not valid or if the object has been discarded, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The size of a memory block may be larger than the size requested when the memory was allocated.

To verify that the specified object's memory block has not been discarded, use the 
<a href="/windows/desktop/api/winbase/nf-winbase-globalflags">GlobalFlags</a> function before calling 
<b>GlobalSize</b>.

## -see-also

<a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalflags">GlobalFlags</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalrealloc">GlobalReAlloc</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory
		  Management Functions</a>
