---
UID: NF:memoryapi.VirtualLock
title: VirtualLock function (memoryapi.h)
description: Locks the specified region of the process's virtual address space into physical memory, ensuring that subsequent access to the region will not incur a page fault.
helpviewer_keywords: ["VirtualLock","VirtualLock function","_win32_virtuallock","base.virtuallock","winbase/VirtualLock"]
old-location: base\virtuallock.htm
tech.root: base
ms.assetid: 414c4704-36f2-40f9-a69a-9d53ab354c30
ms.date: 12/05/2018
ms.keywords: VirtualLock, VirtualLock function, _win32_virtuallock, base.virtuallock, winbase/VirtualLock
req.header: memoryapi.h
req.include-header: Windows.h, Memoryapi.h
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
req.lib: onecore.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VirtualLock
 - memoryapi/VirtualLock
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-memory-l1-1-9.dll
 - api-ms-win-core-memory-l1-1-8.dll
 - api-ms-win-core-memory-l1-1-7.dll
 - api-ms-win-core-memory-l1-1-6.dll
 - api-ms-win-core-memory-l1-1-5.dll
 - Kernel32.dll
 - API-MS-Win-Core-memory-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-2.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - VirtualLock
---

# VirtualLock function


## -description

Locks the specified region of the process's virtual address space into physical memory, ensuring that subsequent access to the region will not incur a page fault.

## -parameters

### -param lpAddress [in]

A pointer to the base address of the region of pages to be locked.

### -param dwSize [in]

The size of the region to be locked, in bytes. The region of affected pages includes all pages that contain one or more bytes in the range from the <i>lpAddress</i> parameter to <code>(lpAddress+dwSize)</code>. This means that a 2-byte range straddling a page boundary causes both pages to be locked.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All pages in the specified region must be committed. Memory protected with <b>PAGE_NOACCESS</b> cannot be locked.

Locking pages into memory may degrade the performance of the system by reducing the available RAM and forcing the system to swap out other critical pages to the paging file. Each version of Windows has a limit on the maximum number of pages a process can lock. This limit is intentionally small to avoid severe performance degradation. Applications that need to lock larger numbers of pages must first call the 
<a href="/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsize">SetProcessWorkingSetSize</a> function to increase their minimum and maximum working set sizes. The maximum number of pages that a process can lock is equal to the number of pages in its minimum working set minus a small overhead.

Pages that a process has locked remain in physical memory until the process unlocks them or terminates. These pages are guaranteed not to be written to the pagefile while they are locked.

To unlock a region of locked pages, use the 
<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualunlock">VirtualUnlock</a> function. Locked pages are automatically unlocked when the process terminates.

This function is not like the 
<a href="/windows/desktop/api/winbase/nf-winbase-globallock">GlobalLock</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-locallock">LocalLock</a> function in that it does not increment a lock count and translate a handle into a pointer. There is no lock count for virtual pages, so multiple calls to the 
<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualunlock">VirtualUnlock</a> function are never required to unlock a region of pages.


#### Examples

For an example, see 
<a href="/windows/desktop/Memory/creating-guard-pages">Creating Guard Pages</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Memory/memory-management-functions">Memory
    Management Functions</a>



<a href="/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsize">SetProcessWorkingSetSize</a>



<a href="/windows/desktop/Memory/virtual-memory-functions">Virtual Memory Functions</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualunlock">VirtualUnlock</a>
