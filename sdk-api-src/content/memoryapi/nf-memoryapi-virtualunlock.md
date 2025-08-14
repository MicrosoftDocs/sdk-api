---
UID: NF:memoryapi.VirtualUnlock
title: VirtualUnlock function (memoryapi.h)
description: Unlocks a specified range of pages in the virtual address space of a process, enabling the system to swap the pages out to the paging file if necessary.
helpviewer_keywords: ["VirtualUnlock","VirtualUnlock function","_win32_virtualunlock","base.virtualunlock","winbase/VirtualUnlock"]
old-location: base\virtualunlock.htm
tech.root: base
ms.assetid: cb868c8a-ac0d-42ad-bf72-2ae617bc0427
ms.date: 12/05/2018
ms.keywords: VirtualUnlock, VirtualUnlock function, _win32_virtualunlock, base.virtualunlock, winbase/VirtualUnlock
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
 - VirtualUnlock
 - memoryapi/VirtualUnlock
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
 - VirtualUnlock
---

# VirtualUnlock function


## -description

Unlocks a specified range of pages in the virtual address space of a process, enabling the system to swap the pages out to the paging file if necessary.

## -parameters

### -param lpAddress [in]

A pointer to the base address of the region of pages to be unlocked.

### -param dwSize [in]

The size of the region being unlocked, in bytes. The region of affected pages includes all pages containing one or more bytes in the range from the <i>lpAddress</i> parameter to <code>(lpAddress+dwSize)</code>. This means that a 2-byte range straddling a page boundary causes both pages to be unlocked.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

For the function to succeed, the range specified need not match a range passed to a previous call to the 
<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtuallock">VirtualLock</a> function, but all pages in the range must be locked. If any of the pages in the specified range are not locked, <b>VirtualUnlock</b> removes such pages from the working set, sets last error to <b>ERROR_NOT_LOCKED</b>, and returns <b>FALSE</b>.

Calling 
<b>VirtualUnlock</b> on a range of memory that is not locked releases the pages from the process's working set.

## -see-also

<a href="/windows/desktop/Memory/memory-management-functions">Memory Management Functions</a>



<a href="/windows/desktop/Memory/virtual-memory-functions">Virtual Memory Functions</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtuallock">VirtualLock</a>