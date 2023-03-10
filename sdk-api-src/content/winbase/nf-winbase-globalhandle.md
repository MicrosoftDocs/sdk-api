---
UID: NF:winbase.GlobalHandle
title: GlobalHandle function (winbase.h)
description: Retrieves the handle associated with the specified pointer to a global memory block.
helpviewer_keywords: ["GlobalHandle","GlobalHandle function","_win32_globalhandle","base.globalhandle","winbase/GlobalHandle"]
old-location: base\globalhandle.htm
tech.root: base
ms.assetid: 18ed3446-060a-4874-8187-5c54fb936da9
ms.date: 12/05/2018
ms.keywords: GlobalHandle, GlobalHandle function, _win32_globalhandle, base.globalhandle, winbase/GlobalHandle
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
 - GlobalHandle
 - winbase/GlobalHandle
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
 - GlobalHandle
---

# GlobalHandle function


## -description

Retrieves the handle associated with the specified pointer to a global memory block.
<div class="alert"><b>Note</b>  The global functions have greater overhead and provide fewer features than other memory management functions. New applications should use the <a href="/windows/desktop/Memory/heap-functions">heap functions</a> unless documentation states that a global function should be used. For more information, see <a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>.
</div><div> </div>

## -parameters

### -param pMem [in]

A pointer to the first byte of the global memory block. This pointer is returned by the 
<a href="/windows/desktop/api/winbase/nf-winbase-globallock">GlobalLock</a> function.

## -returns

If the function succeeds, the return value is a handle to the specified global memory object.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

When the 
<a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a> function allocates a memory object with <b>GMEM_MOVEABLE</b>, it returns a handle to the object. The 
<a href="/windows/desktop/api/winbase/nf-winbase-globallock">GlobalLock</a> function converts this handle into a pointer to the memory block, and 
<b>GlobalHandle</b> converts the pointer back into a handle.

## -see-also

<a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globallock">GlobalLock</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory
    Management Functions</a>