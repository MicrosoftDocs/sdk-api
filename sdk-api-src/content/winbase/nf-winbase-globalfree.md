---
UID: NF:winbase.GlobalFree
title: GlobalFree function (winbase.h)
description: Frees the specified global memory object and invalidates its handle.
helpviewer_keywords: ["GlobalFree","GlobalFree function","_win32_globalfree","base.globalfree","winbase/GlobalFree"]
old-location: base\globalfree.htm
tech.root: base
ms.assetid: 5fe910ac-f857-45ca-9c0f-4f9ba3c5e61b
ms.date: 12/05/2018
ms.keywords: GlobalFree, GlobalFree function, _win32_globalfree, base.globalfree, winbase/GlobalFree
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
 - GlobalFree
 - winbase/GlobalFree
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
 - GlobalFree
---

# GlobalFree function


## -description

Frees the specified global memory object and invalidates its handle.
<div class="alert"><b>Note</b>  The global functions have greater overhead and provide fewer features than other memory management functions. New applications should use the <a href="/windows/desktop/Memory/heap-functions">heap functions</a> unless documentation states that a global function should be used. For more information, see <a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>.
</div><div> </div>

## -parameters

### -param hMem [in]

A handle to the global memory object. This handle is returned by either the 
<a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-globalrealloc">GlobalReAlloc</a> function. It is not safe to free memory allocated with <a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a>.

## -returns

If the function succeeds, the return value is <b>NULL</b>.

If the function fails, the return value is equal to a handle to the global memory object. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the process examines or modifies the memory after it has been freed, heap corruption may occur or an access violation exception (EXCEPTION_ACCESS_VIOLATION) may be generated.

The 
<b>GlobalFree</b> function will free a locked memory object. A locked memory object has a lock count greater than zero. The 
<a href="/windows/desktop/api/winbase/nf-winbase-globallock">GlobalLock</a> function locks a global memory object and increments the lock count by one. The 
<a href="/windows/desktop/api/winbase/nf-winbase-globalunlock">GlobalUnlock</a> function unlocks it and decrements the lock count by one. To get the lock count of a global memory object, use the 
<a href="/windows/desktop/api/winbase/nf-winbase-globalflags">GlobalFlags</a> function.

If an application is running under a debug version of the system, 
<b>GlobalFree</b> will issue a message that tells you that a locked object is being freed. If you are debugging the application, 
<b>GlobalFree</b> will enter a breakpoint just before freeing a locked object. This allows you to verify the intended behavior, then continue execution.


#### Examples

For an example, see 
<a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalflags">GlobalFlags</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globallock">GlobalLock</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalrealloc">GlobalReAlloc</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalunlock">GlobalUnlock</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory
		  Management Functions</a>