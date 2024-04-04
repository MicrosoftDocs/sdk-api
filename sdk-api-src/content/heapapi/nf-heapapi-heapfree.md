---
UID: NF:heapapi.HeapFree
title: HeapFree function (heapapi.h)
description: Frees a memory block allocated from a heap by the HeapAlloc or HeapReAlloc function.
helpviewer_keywords: ["HEAP_NO_SERIALIZE","HeapFree","HeapFree function","_win32_heapfree","base.heapfree","heapapi/HeapFree","winbase/HeapFree"]
old-location: base\heapfree.htm
tech.root: base
ms.assetid: 6139e55f-9dda-42b5-bc9b-8d9bbfeaa619
ms.date: 02/02/2024
ms.keywords: HEAP_NO_SERIALIZE, HeapFree, HeapFree function, _win32_heapfree, base.heapfree, heapapi/HeapFree, winbase/HeapFree
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
 - HeapFree
 - heapapi/HeapFree
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
 - HeapFree
---

# HeapFree function

## -description

Frees a memory block allocated from a heap by the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a> or <a href="/windows/desktop/api/heapapi/nf-heapapi-heaprealloc">HeapReAlloc</a> function.

## -parameters

### -param hHeap [in]

A handle to the heap whose memory block is to be freed. This handle is returned by either the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapcreate">HeapCreate</a> or <a href="/windows/desktop/api/heapapi/nf-heapapi-getprocessheap">GetProcessHeap</a> function.

### -param dwFlags [in]

The heap free options. Specifying the following value overrides the corresponding value specified in the <i>flOptions</i> parameter when the heap was created by using the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapcreate">HeapCreate</a> function.

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

Do not specify this value when accessing the process heap. The system may create additional threads within the application's process, such as a CTRL+C handler, that simultaneously access the process heap.

</td>
</tr>
</table>

### -param lpMem [in]

A pointer to the memory block to be freed. This pointer is returned by the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a> or <a href="/windows/desktop/api/heapapi/nf-heapapi-heaprealloc">HeapReAlloc</a> function. This pointer can be <b>NULL</b>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. An application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> for extended error information.

## -remarks

You should not refer in any way to memory that has been freed by <b>HeapFree</b>. After that memory is freed, any information that may have been in it is gone forever. If you require information, do not free memory containing the information. Function calls that return information about memory (such as <a href="/windows/desktop/api/heapapi/nf-heapapi-heapsize">HeapSize</a>) may not be used with freed memory, as they may return bogus data. Calling <b>HeapFree</b> twice with the same pointer can cause heap corruption, resulting in subsequent calls to <a href="/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a> returning the same pointer twice.

Serialization ensures mutual exclusion when two or more threads attempt to simultaneously allocate or free blocks from the same heap. There is a small performance cost to serialization, but it must be used whenever multiple threads allocate and free memory from the same heap. Setting the <b>HEAP_NO_SERIALIZE</b> value eliminates mutual exclusion on the heap. Without serialization, two or more threads that use the same heap handle might attempt to allocate or free memory simultaneously, likely causing corruption in the heap. The <b>HEAP_NO_SERIALIZE</b> value can, therefore, be safely used only in the following situations:

- The process has only one thread.
- The process has multiple threads, but only one thread calls the heap functions for a specific heap.
- The process has multiple threads, and the application provides its own mechanism for mutual exclusion to a specific heap.

#### Examples

For an example, see <a href="/windows/desktop/Memory/getting-process-heaps">Getting Process Heaps</a>.

## -see-also

[Heap Functions](/windows/win32/Memory/heap-functions)

[HeapAlloc](nf-heapapi-heapalloc.md)

[HeapReAlloc](nf-heapapi-heaprealloc.md)

[Memory Management Functions](/windows/win32/Memory/memory-management-functions)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
