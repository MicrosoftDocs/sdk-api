---
UID: NF:winbase.GlobalUnlock
title: GlobalUnlock function (winbase.h)
description: Decrements the lock count associated with a memory object that was allocated with GMEM_MOVEABLE.
helpviewer_keywords: ["GlobalUnlock","GlobalUnlock function","_win32_globalunlock","base.globalunlock","winbase/GlobalUnlock"]
old-location: base\globalunlock.htm
tech.root: base
ms.assetid: 580a2873-7f06-47a1-acf5-c2b3c96e15e7
ms.date: 12/05/2018
ms.keywords: GlobalUnlock, GlobalUnlock function, _win32_globalunlock, base.globalunlock, winbase/GlobalUnlock
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
 - GlobalUnlock
 - winbase/GlobalUnlock
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
 - GlobalUnlock
---

# GlobalUnlock function


## -description

Decrements the lock count associated with a memory object that was allocated with <b>GMEM_MOVEABLE</b>. This function has no effect on memory objects allocated with <b>GMEM_FIXED</b>.
<div class="alert"><b>Note</b>  The global functions have greater overhead and provide fewer features than other memory management functions. New applications should use the <a href="/windows/desktop/Memory/heap-functions">heap functions</a> unless documentation states that a global function should be used. For more information, see <a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>.
</div><div> </div>

## -parameters

### -param hMem [in]

A handle to the global memory object. This handle is returned by either the 
<a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-globalrealloc">GlobalReAlloc</a> function.

## -returns

If the memory object is still locked after decrementing the lock count, the return value is a nonzero value. If the memory object is unlocked after decrementing the lock count, the function returns zero and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>NO_ERROR</b>.

If the function fails, the return value is zero and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns a value other than <b>NO_ERROR</b>.

## -remarks

The internal data structures for each memory object include a lock count that is initially zero. For movable memory objects, the 
<a href="/windows/desktop/api/winbase/nf-winbase-globallock">GlobalLock</a> function increments the count by one, and 
<b>GlobalUnlock</b> decrements the count by one. For each call that a process makes to 
<b>GlobalLock</b> for an object, it must eventually call 
<b>GlobalUnlock</b>. Locked memory will not be moved or discarded, unless the memory object is reallocated by using the 
<a href="/windows/desktop/api/winbase/nf-winbase-globalrealloc">GlobalReAlloc</a> function. The memory block of a locked memory object remains locked until its lock count is decremented to zero, at which time it can be moved or discarded.

Memory objects allocated with <b>GMEM_FIXED</b> always have a lock count of zero. If the specified memory block is fixed memory, this function returns <b>TRUE</b>.

If the memory object is already unlocked, 
<b>GlobalUnlock</b> returns <b>FALSE</b> and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> reports <b>ERROR_NOT_LOCKED</b>.

A process should not rely on the return value to determine the number of times it must subsequently call 
<b>GlobalUnlock</b> for a memory object.

## -see-also

<a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globallock">GlobalLock</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalrealloc">GlobalReAlloc</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory
    Management Functions</a>