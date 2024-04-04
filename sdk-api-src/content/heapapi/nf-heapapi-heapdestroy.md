---
UID: NF:heapapi.HeapDestroy
title: HeapDestroy function (heapapi.h)
description: Destroys the specified heap object. It decommits and releases all the pages of a private heap object, and it invalidates the handle to the heap.
helpviewer_keywords: ["HeapDestroy","HeapDestroy function","_win32_heapdestroy","base.heapdestroy","heapapi/HeapDestroy","winbase/HeapDestroy"]
old-location: base\heapdestroy.htm
tech.root: base
ms.assetid: 2ad8d15f-de5e-424d-9349-3baccb000a36
ms.date: 02/02/2024
ms.keywords: HeapDestroy, HeapDestroy function, _win32_heapdestroy, base.heapdestroy, heapapi/HeapDestroy, winbase/HeapDestroy
req.header: heapapi.h
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
 - HeapDestroy
 - heapapi/HeapDestroy
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
 - HeapDestroy
---

# HeapDestroy function

## -description

Destroys the specified heap object.

**HeapDestroy** de-commits and releases all the pages of a private heap object, and it invalidates the handle to the heap.

## -parameters

### -param hHeap [in]

A handle to the heap to be destroyed. This handle is returned by the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapcreate">HeapCreate</a> function. Do not use the handle to the process heap returned by the <a href="/windows/desktop/api/heapapi/nf-heapapi-getprocessheap">GetProcessHeap</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Processes can call <b>HeapDestroy</b> without first calling the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapfree">HeapFree</a> function to free memory allocated from the heap.

#### Examples

<a href="/windows/desktop/Memory/enumerating-a-heap">Enumerating a Heap</a>

## -see-also

[Heap Functions](/windows/win32/Memory/heap-functions)

[HeapCreate](nf-heapapi-heapcreate.md)

[Memory Management Functions](/windows/win32/Memory/memory-management-functions)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
