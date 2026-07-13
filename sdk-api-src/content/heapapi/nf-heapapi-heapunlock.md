---
UID: NF:heapapi.HeapUnlock
title: HeapUnlock function (heapapi.h)
description: Releases ownership of the critical section object, or lock, that is associated with a specified heap.
helpviewer_keywords: ["HeapUnlock","HeapUnlock function","_win32_heapunlock","base.heapunlock","heapapi/HeapUnlock","winbase/HeapUnlock"]
old-location: base\heapunlock.htm
tech.root: base
ms.assetid: c1a7b2c8-293e-4e07-a654-fd10b2f0ef39
ms.date: 02/02/2024
ms.keywords: HeapUnlock, HeapUnlock function, _win32_heapunlock, base.heapunlock, heapapi/HeapUnlock, winbase/HeapUnlock
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
 - HeapUnlock
 - heapapi/HeapUnlock
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
 - HeapUnlock
---

# HeapUnlock function

## -description

Releases ownership of the critical section object, or lock, that is associated with a specified heap. It reverses the action of the <a href="/windows/desktop/api/heapapi/nf-heapapi-heaplock">HeapLock</a> function.

## -parameters

### -param hHeap [in]

A handle to the heap to be unlocked. This handle is returned by either the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapcreate">HeapCreate</a> or <a href="/windows/desktop/api/heapapi/nf-heapapi-getprocessheap">GetProcessHeap</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <a href="/windows/desktop/api/heapapi/nf-heapapi-heaplock">HeapLock</a> function is primarily useful for preventing the allocation and release of heap memory by other threads while the calling thread uses the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapwalk">HeapWalk</a> function. The <b>HeapUnlock</b> function is the inverse of <b>HeapLock</b>.

Each call to <a href="/windows/desktop/api/heapapi/nf-heapapi-heaplock">HeapLock</a> must be matched by a corresponding call to the <b>HeapUnlock</b> function. Failure to call <b>HeapUnlock</b> will block the execution of any other threads of the calling process that attempt to access the heap.

If the <b>HeapUnlock</b> function is called on a heap created with the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapcreate">HEAP_NO_SERIALIZATION</a> flag, the results are undefined.

#### Examples

<a href="/windows/desktop/Memory/enumerating-a-heap">Enumerating a Heap</a>

## -see-also

[Heap Functions](/windows/win32/Memory/heap-functions)

[HeapLock](nf-heapapi-heaplock.md)

[HeapWalk](nf-heapapi-heapwalk.md)

[Memory Management Functions](/windows/win32/Memory/memory-management-functions)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
