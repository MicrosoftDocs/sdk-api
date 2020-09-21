---
UID: NF:winbase.LocalLock
title: LocalLock function (winbase.h)
description: Locks a local memory object and returns a pointer to the first byte of the object's memory block.
helpviewer_keywords: ["LocalLock","LocalLock function","_win32_locallock","base.locallock","winbase/LocalLock"]
old-location: base\locallock.htm
tech.root: base
ms.assetid: a9432e28-9fbd-4a7e-8dce-fad3da04804a
ms.date: 12/05/2018
ms.keywords: LocalLock, LocalLock function, _win32_locallock, base.locallock, winbase/LocalLock
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
 - LocalLock
 - winbase/LocalLock
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
 - LocalLock
---

# LocalLock function


## -description

Locks a local memory object and returns a pointer to the first byte of the object's memory block.
<div class="alert"><b>Note</b>  The local functions have greater overhead and provide fewer features than other memory management functions. New applications should use the <a href="/windows/desktop/Memory/heap-functions">heap functions</a> unless documentation states that a local function should be used. For more information, see <a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>.</div><div> </div>

## -parameters

### -param hMem [in]

A handle to the local memory object. This handle is returned by either the 
<a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-localrealloc">LocalReAlloc</a> function.

## -returns

If the function succeeds, the return value is a pointer to the first byte of the memory block.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The internal data structures for each memory object include a lock count that is initially zero. For movable memory objects, 
<b>LocalLock</b> increments the count by one, and the 
<a href="/windows/desktop/api/winbase/nf-winbase-localunlock">LocalUnlock</a> function decrements the count by one. Each successful call that a process makes to 
<b>LocalLock</b> for an object must be matched by a corresponding call to 
<b>LocalUnlock</b>. Locked memory will not be moved or discarded unless the memory object is reallocated by using the 
<a href="/windows/desktop/api/winbase/nf-winbase-localrealloc">LocalReAlloc</a> function. The memory block of a locked memory object remains locked in memory until its lock count is decremented to zero, at which time it can be moved or discarded.

Memory objects allocated with <b>LMEM_FIXED</b> always have a lock count of zero. For these objects, the value of the returned pointer is equal to the value of the specified handle.

If the specified memory block has been discarded or if the memory block has a zero-byte size, this function returns <b>NULL</b>.

Discarded objects always have a lock count of zero.

## -see-also

<a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localflags">LocalFlags</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localrealloc">LocalReAlloc</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localunlock">LocalUnlock</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory
    Management Functions</a>