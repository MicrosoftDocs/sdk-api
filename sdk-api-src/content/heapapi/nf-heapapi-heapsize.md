---
UID: NF:heapapi.HeapSize
title: HeapSize function (heapapi.h)
description: Retrieves the size of a memory block allocated from a heap by the HeapAlloc or HeapReAlloc function.
helpviewer_keywords: ["HEAP_NO_SERIALIZE","HeapSize","HeapSize function","_win32_heapsize","base.heapsize","heapapi/HeapSize","winbase/HeapSize"]
old-location: base\heapsize.htm
tech.root: base
ms.assetid: a8fcfd99-7b04-4aa3-8619-272b254551a3
ms.date: 02/02/2024
ms.keywords: HEAP_NO_SERIALIZE, HeapSize, HeapSize function, _win32_heapsize, base.heapsize, heapapi/HeapSize, winbase/HeapSize
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
 - HeapSize
 - heapapi/HeapSize
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
 - HeapSize
---

# HeapSize function

## -description

Retrieves the size of a memory block allocated from a heap by the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a> or <a href="/windows/desktop/api/heapapi/nf-heapapi-heaprealloc">HeapReAlloc</a> function.

## -parameters

### -param hHeap [in]

A handle to the heap in which the memory block resides. This handle is returned by either the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapcreate">HeapCreate</a> or <a href="/windows/desktop/api/heapapi/nf-heapapi-getprocessheap">GetProcessHeap</a> function.

### -param dwFlags [in]

The heap size options. Specifying the following value overrides the corresponding value specified in the <i>flOptions</i> parameter when the heap was created by using the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapcreate">HeapCreate</a> function.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HEAP_NO_SERIALIZE"></a><a id="heap_no_serialize"></a><dl>
<dt><b>HEAP_NO_SERIALIZE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Serialized access will not be used. For more information, see Remarks.

To ensure that serialized access is disabled for all calls to this function, specify <b>HEAP_NO_SERIALIZE</b> in the call to <a href="/windows/desktop/api/heapapi/nf-heapapi-heapcreate">HeapCreate</a>. In this case, it is not necessary to additionally specify <b>HEAP_NO_SERIALIZE</b> in this function call.

This value should not be specified when accessing the process heap. The system may create additional threads within the application's process, such as a CTRL+C handler, that simultaneously access the process heap.

</td>
</tr>
</table>

### -param lpMem [in]

A pointer to the memory block whose size the function will obtain. This is a pointer returned by the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a> or <a href="/windows/desktop/api/heapapi/nf-heapapi-heaprealloc">HeapReAlloc</a> function. The memory block must be from the heap specified by the <i>hHeap</i> parameter.

## -returns

If the function succeeds, the return value is the requested size of the allocated memory block, in bytes.

If the function fails, the return value is <code>(SIZE_T)-1</code>. The function does not call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a>. An application cannot call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> for extended error information.

If the <i>lpMem</i> parameter refers to a heap allocation that is not in the heap specified by the <i>hHeap</i> parameter, the behavior of the <b>HeapSize</b> function is undefined.

## -remarks

Serialization ensures mutual exclusion when two or more threads attempt to simultaneously allocate or free blocks from the same heap. There is a small performance cost to serialization, but it must be used whenever multiple threads allocate and free memory from the same heap. Setting the <b>HEAP_NO_SERIALIZE</b> value eliminates mutual exclusion on the heap. Without serialization, two or more threads that use the same heap handle might attempt to allocate or free memory simultaneously, likely causing corruption in the heap. The <b>HEAP_NO_SERIALIZE</b> value can, therefore, be safely used only in the following situations:

- The process has only one thread.
- The process has multiple threads, but only one thread calls the heap functions for a specific heap.
- The process has multiple threads, and the application provides its own mechanism for mutual exclusion to a specific heap.

## -see-also

[Heap Functions](/windows/win32/Memory/heap-functions)

[HeapAlloc](nf-heapapi-heapalloc.md)

[HeapReAlloc](nf-heapapi-heaprealloc.md)

[Memory Management Functions](/windows/win32/Memory/memory-management-functions)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
