---
UID: NF:heapapi.HeapLock
title: HeapLock function (heapapi.h)
description: Attempts to acquire the critical section object, or lock, that is associated with a specified heap.
helpviewer_keywords: ["HeapLock","HeapLock function","_win32_heaplock","base.heaplock","heapapi/HeapLock","winbase/HeapLock"]
old-location: base\heaplock.htm
tech.root: base
ms.assetid: bc01b82d-ef10-40d7-af82-e599ba825944
ms.date: 02/02/2024
ms.keywords: HeapLock, HeapLock function, _win32_heaplock, base.heaplock, heapapi/HeapLock, winbase/HeapLock
req.header: heapapi.h
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
 - HeapLock
 - heapapi/HeapLock
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-heap-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-heap-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - vertdll.dll
api_name:
 - HeapLock
---

# HeapLock function

## -description

Attempts to acquire the critical section object, or lock, that is associated with a specified heap.

## -parameters

### -param hHeap [in]

A handle to the heap to be locked. This handle is returned by either the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapcreate">HeapCreate</a> or <a href="/windows/desktop/api/heapapi/nf-heapapi-getprocessheap">GetProcessHeap</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the function succeeds, the calling thread owns the heap lock. Only the calling thread will be able to allocate or release memory from the heap. The execution of any other thread of the calling process will be blocked if that thread attempts to allocate or release memory from the heap. Such threads will remain blocked until the thread that owns the heap lock calls the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapunlock">HeapUnlock</a> function.

The <b>HeapLock</b> function is primarily useful for preventing the allocation and release of heap memory by other threads while the calling thread uses the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapwalk">HeapWalk</a> function.

If the <b>HeapLock</b> function is called on a heap created with the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapcreate">HEAP_NO_SERIALIZE</a> flag, the results are undefined.

Each successful call to <b>HeapLock</b> must be matched by a corresponding call to <a href="/windows/desktop/api/heapapi/nf-heapapi-heapunlock">HeapUnlock</a>. Failure to call <b>HeapUnlock</b> will block the execution of any other threads of the calling process that attempt to access the heap.

#### Examples

<a href="/windows/desktop/Memory/enumerating-a-heap">Enumerating a Heap</a>

## -see-also

[Heap Functions](/windows/win32/Memory/heap-functions)

[HeapUnlock](nf-heapapi-heapunlock.md)

[HeapWalk](nf-heapapi-heapwalk.md)

[Memory Management Functions](/windows/win32/Memory/memory-management-functions)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
