---
UID: NF:winbase.LocalUnlock
title: LocalUnlock function (winbase.h)
description: Decrements the lock count associated with a memory object that was allocated with LMEM_MOVEABLE.
helpviewer_keywords: ["LocalUnlock","LocalUnlock function","_win32_localunlock","base.localunlock","winbase/LocalUnlock"]
old-location: base\localunlock.htm
tech.root: base
ms.assetid: eac40b69-5fb6-4523-826d-a012f6f4e5ce
ms.date: 12/05/2018
ms.keywords: LocalUnlock, LocalUnlock function, _win32_localunlock, base.localunlock, winbase/LocalUnlock
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
 - LocalUnlock
 - winbase/LocalUnlock
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
 - LocalUnlock
---

# LocalUnlock function


## -description

Decrements the lock count associated with a memory object that was allocated with <b>LMEM_MOVEABLE</b>. This function has no effect on memory objects allocated with <b>LMEM_FIXED</b>.
<div class="alert"><b>Note</b>  The local functions have greater overhead and provide fewer features than other memory management functions. New applications should use the <a href="/windows/desktop/Memory/heap-functions">heap functions</a> unless documentation states that a local function should be used. For more information, see <a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>.</div><div> </div>

## -parameters

### -param hMem [in]

A handle to the local memory object. This handle is returned by either the 
<a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-localrealloc">LocalReAlloc</a> function.

## -returns

If the memory object is still locked after decrementing the lock count, the return value is nonzero. If the memory object is unlocked after decrementing the lock count, the function returns zero and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>NO_ERROR</b>.

If the function fails, the return value is zero and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns a value other than <b>NO_ERROR</b>.

## -remarks

The internal data structures for each memory object include a lock count that is initially zero. For movable memory objects, the 
<a href="/windows/desktop/api/winbase/nf-winbase-locallock">LocalLock</a> function increments the count by one, and 
<b>LocalUnlock</b> decrements the count by one. For each call that a process makes to 
<b>LocalLock</b> for an object, it must eventually call 
<b>LocalUnlock</b>. Locked memory will not be moved or discarded unless the memory object is reallocated by using the 
<a href="/windows/desktop/api/winbase/nf-winbase-localrealloc">LocalReAlloc</a> function. The memory block of a locked memory object remains locked until its lock count is decremented to zero, at which time it can be moved or discarded.

If the memory object is already unlocked, 
<b>LocalUnlock</b> returns <b>FALSE</b> and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> reports <b>ERROR_NOT_LOCKED</b>. Memory objects allocated with <b>LMEM_FIXED</b> always have a lock count of zero and cause the <b>ERROR_NOT_LOCKED</b> error.

A process should not rely on the return value to determine the number of times it must subsequently call 
<b>LocalUnlock</b> for the memory block.

## -see-also

<a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localflags">LocalFlags</a>



<a href="/windows/desktop/api/winbase/nf-winbase-locallock">LocalLock</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localrealloc">LocalReAlloc</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory
    Management Functions</a>