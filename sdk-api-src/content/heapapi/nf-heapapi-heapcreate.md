---
UID: NF:heapapi.HeapCreate
title: HeapCreate function (heapapi.h)
description: Creates a private heap object that can be used by the calling process. The function reserves space in the virtual address space of the process and allocates physical storage for a specified initial portion of this block.
helpviewer_keywords: ["HEAP_CREATE_ENABLE_EXECUTE","HEAP_GENERATE_EXCEPTIONS","HEAP_NO_SERIALIZE","HeapCreate","HeapCreate function","_win32_heapcreate","base.heapcreate","heapapi/HeapCreate","winbase/HeapCreate"]
old-location: base\heapcreate.htm
tech.root: base
ms.assetid: 8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b
ms.date: 02/02/2024
ms.keywords: HEAP_CREATE_ENABLE_EXECUTE, HEAP_GENERATE_EXCEPTIONS, HEAP_NO_SERIALIZE, HeapCreate, HeapCreate function, _win32_heapcreate, base.heapcreate, heapapi/HeapCreate, winbase/HeapCreate
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
 - HeapCreate
 - heapapi/HeapCreate
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
 - HeapCreate
---

# HeapCreate function

## -description

Creates a private heap object that can be used by the calling process. The function reserves space in the virtual address space of the process and allocates physical storage for a specified initial portion of this block.

## -parameters

### -param flOptions [in]

The heap allocation options. These options affect subsequent access to the new heap through calls to the heap functions. This parameter can be 0 or one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HEAP_CREATE_ENABLE_EXECUTE"></a><a id="heap_create_enable_execute"></a><dl>
<dt><b>HEAP_CREATE_ENABLE_EXECUTE</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
All memory blocks that are allocated from this heap allow code execution, if the hardware enforces <a href="/windows/desktop/Memory/data-execution-prevention">data execution prevention</a>. Use this flag heap in applications that run code from the heap. If <b>HEAP_CREATE_ENABLE_EXECUTE</b> is not specified and an application attempts to run code from a protected page, the application receives an exception with the status code <b>STATUS_ACCESS_VIOLATION</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="HEAP_GENERATE_EXCEPTIONS"></a><a id="heap_generate_exceptions"></a><dl>
<dt><b>HEAP_GENERATE_EXCEPTIONS</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The system raises an exception to indicate failure (for example,  an out-of-memory condition) for calls to <a href="/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a> and <a href="/windows/desktop/api/heapapi/nf-heapapi-heaprealloc">HeapReAlloc</a> instead of returning <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="HEAP_NO_SERIALIZE"></a><a id="heap_no_serialize"></a><dl>
<dt><b>HEAP_NO_SERIALIZE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Serialized access is not used when the heap functions access this heap. This option applies to all subsequent heap function calls. Alternatively, you can specify this option on individual heap function calls.

The low-fragmentation heap (LFH) cannot be enabled for a heap created with this option.

 A heap created with this option cannot be locked.

For more information about serialized access, see the  Remarks section of this topic.

</td>
</tr>
</table>

### -param dwInitialSize [in]

The initial size of the heap, in bytes. This value determines the initial amount of memory that is committed for the heap. The value is rounded up to a multiple of the system page size. The value must be smaller than <i>dwMaximumSize</i>.

If this parameter is 0, the function commits one page. To determine the size of a page on the host computer, use the <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo">GetSystemInfo</a> function.

### -param dwMaximumSize [in]

The maximum size of the heap, in bytes. The <b>HeapCreate</b> function rounds <i>dwMaximumSize</i> up to a multiple of the system page size and then reserves a block of that size in the process's virtual address space for the heap. If allocation requests made by the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a> or <a href="/windows/desktop/api/heapapi/nf-heapapi-heaprealloc">HeapReAlloc</a> functions exceed the size specified by <i>dwInitialSize</i>, the system commits additional pages of memory for the heap, up to the heap's maximum size.

If <i>dwMaximumSize</i> is not zero, the heap size is fixed and cannot grow beyond the maximum size. Also, the largest memory block that can be allocated from the heap is slightly less than 512 KB for a 32-bit process and slightly less than 1,024 KB for a 64-bit process. Requests to allocate larger blocks fail, even if the maximum size of the heap is large enough to contain the block.

If <i>dwMaximumSize</i> is 0, the heap can grow in size. The heap's size is limited only by the available memory. Requests to allocate memory blocks larger than the limit for a fixed-size heap do not automatically fail; instead, the system calls the <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a> function to obtain the memory that is needed for large blocks. Applications that need to allocate large memory blocks should set <i>dwMaximumSize</i> to 0.

## -returns

If the function succeeds, the return value is a handle to the newly created heap.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>HeapCreate</b> function creates a private heap object from which the calling process can allocate memory blocks by using the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a> function. The initial size determines the number of committed pages that are allocated initially for the heap. The maximum size determines the total number of reserved pages. These pages create a block in the process's virtual address space into which the heap can grow. If requests by <b>HeapAlloc</b> exceed the current size of committed pages, additional pages are automatically committed from this reserved space, if the physical storage is available.

<b>Windows Server 2003 and Windows XP:  </b>By default, the newly created private heap is a standard heap. To enable the low-fragmentation heap, call the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapsetinformation">HeapSetInformation</a> function with a handle to the private heap.

The memory of a private heap object is accessible only to the process that created it. If a dynamic-link library (DLL) creates a private heap, the heap is created in the address space of the process that calls the DLL, and it is accessible only to that process.

The system uses memory from the private heap to store heap support structures, so not all of the specified heap size is available to the process. For example, if the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a> function requests 64 kilobytes (K) from a heap with a maximum size of 64K, the request may fail because of system overhead.

If <b>HEAP_NO_SERIALIZE</b> is not specified (the simple default), the heap serializes access within the calling process. Serialization ensures mutual exclusion when two or more threads attempt simultaneously to allocate or free blocks from the same heap. There is a small performance cost to serialization, but it must be used whenever multiple threads allocate and free memory from the same heap. The <a href="/windows/desktop/api/heapapi/nf-heapapi-heaplock">HeapLock</a> and <a href="/windows/desktop/api/heapapi/nf-heapapi-heapunlock">HeapUnlock</a> functions can be used to block and permit access to a serialized heap.

Setting <b>HEAP_NO_SERIALIZE</b> eliminates mutual exclusion on the heap. Without serialization, two or more threads that use the same heap handle might attempt to allocate or free memory simultaneously, which may cause corruption in the heap. Therefore, <b>HEAP_NO_SERIALIZE</b> can safely be used only in the following situations:

<ul>
<li>The process has only one thread.</li>
<li>The process has multiple threads, but only one thread calls the heap functions for a specific heap.</li>
<li>The process has multiple threads, and the application provides its own mechanism for mutual exclusion to a specific heap.</li>
</ul>

If the <a href="/windows/desktop/api/heapapi/nf-heapapi-heaplock">HeapLock</a> and <a href="/windows/desktop/api/heapapi/nf-heapapi-heapunlock">HeapUnlock</a> functions are called on a heap created with the <b>HEAP_NO_SERIALIZE</b> flag, the results are undefined.

To obtain a handle to the default heap for a process, use the <a href="/windows/desktop/api/heapapi/nf-heapapi-getprocessheap">GetProcessHeap</a> function. To obtain handles to the default heap and private heaps that are active for the calling process, use the <a href="/windows/desktop/api/heapapi/nf-heapapi-getprocessheaps">GetProcessHeaps</a> function.

#### Examples

<a href="/windows/desktop/Memory/enumerating-a-heap">Enumerating a Heap</a>

## -see-also

[Heap Functions](/windows/win32/Memory/heap-functions)

[HeapAlloc](nf-heapapi-heapalloc.md)

[HeapDestroy](nf-heapapi-heapdestroy.md)

[HeapValidate](nf-heapapi-heapvalidate.md)

[Memory Management Functions](/windows/win32/Memory/memory-management-functions)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
