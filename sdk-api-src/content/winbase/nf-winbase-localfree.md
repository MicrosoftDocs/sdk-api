---
UID: NF:winbase.LocalFree
title: LocalFree function (winbase.h)
description: Frees the specified local memory object and invalidates its handle.
helpviewer_keywords: ["LocalFree","LocalFree function","_win32_localfree","base.localfree","winbase/LocalFree"]
old-location: base\localfree.htm
tech.root: base
ms.assetid: a0393983-cb43-4dfa-91a6-d82a5fb8de12
ms.date: 12/05/2018
ms.keywords: LocalFree, LocalFree function, _win32_localfree, base.localfree, winbase/LocalFree
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
 - LocalFree
 - winbase/LocalFree
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
 - API-MS-Win-Core-Heap-l2-1-0.dll
api_name:
 - LocalFree
---

# LocalFree function


## -description

Frees the specified local memory object and invalidates its handle.
<div class="alert"><b>Note</b>  The local functions have greater overhead and provide fewer features than other memory management functions. New applications should use the <a href="/windows/desktop/Memory/heap-functions">heap functions</a> unless documentation states that a local function should be used. For more information, see <a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>.</div><div> </div>

## -parameters

### -param hMem [in]

A handle to the local memory object. This handle is returned by either the 
<a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-localrealloc">LocalReAlloc</a> function. It is not safe to free memory allocated with <a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a>.

## -returns

If the function succeeds, the return value is <b>NULL</b>.

If the function fails, the return value is equal to a handle to the local memory object. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the process tries to examine or modify the memory after it has been freed, heap corruption may occur or an access violation exception (EXCEPTION_ACCESS_VIOLATION) may be generated.

If the <i>hMem</i> parameter is <b>NULL</b>, 
<b>LocalFree</b> ignores the parameter and returns <b>NULL</b>.

The 
<b>LocalFree</b> function will free a locked memory object. A locked memory object has a lock count greater than zero. The 
<a href="/windows/desktop/api/winbase/nf-winbase-locallock">LocalLock</a> function locks a local memory object and increments the lock count by one. The 
<a href="/windows/desktop/api/winbase/nf-winbase-localunlock">LocalUnlock</a> function unlocks it and decrements the lock count by one. To get the lock count of a local memory object, use the 
<a href="/windows/desktop/api/winbase/nf-winbase-localflags">LocalFlags</a> function.

If an application is running under a debug version of the system, 
<b>LocalFree</b> will issue a message that tells you that a locked object is being freed. If you are debugging the application, 
<b>LocalFree</b> will enter a breakpoint just before freeing a locked object. This allows you to verify the intended behavior, then continue execution.


#### Examples

For an example, see 
<a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalfree">GlobalFree</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localflags">LocalFlags</a>



<a href="/windows/desktop/api/winbase/nf-winbase-locallock">LocalLock</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localrealloc">LocalReAlloc</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localunlock">LocalUnlock</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory
		  Management Functions</a>