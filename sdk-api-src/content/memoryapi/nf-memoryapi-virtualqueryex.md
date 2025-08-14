---
UID: NF:memoryapi.VirtualQueryEx
title: VirtualQueryEx function (memoryapi.h)
description: Retrieves information about a range of pages within the virtual address space of a specified process.
helpviewer_keywords: ["VirtualQueryEx","VirtualQueryEx function","_win32_virtualqueryex","base.virtualqueryex","winbase/VirtualQueryEx"]
old-location: base\virtualqueryex.htm
tech.root: base
ms.assetid: 19e1d875-f661-47cd-bba7-4327a2bbfacc
ms.date: 12/05/2018
ms.keywords: VirtualQueryEx, VirtualQueryEx function, _win32_virtualqueryex, base.virtualqueryex, winbase/VirtualQueryEx
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
 - VirtualQueryEx
 - memoryapi/VirtualQueryEx
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
 - API-MS-Win-Core-memory-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-1.dll
 - API-MS-Win-Core-memory-l1-1-2.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - VirtualQueryEx
---

# VirtualQueryEx function


## -description

Retrieves information about a range of pages within the virtual address space of a specified process.

## -parameters

### -param hProcess [in]

A handle to the process whose memory information is queried. The handle must have been opened with the <b>PROCESS_QUERY_INFORMATION</b> access right, which enables using the handle to read information from the process object. For more information, see 
<a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

### -param lpAddress [in, optional]

A pointer to the base address of the region of pages to be queried. This value is rounded down to the next page boundary. To determine the size of a page on the host computer, use the 
<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo">GetSystemInfo</a> function.

If <i>lpAddress</i> specifies an address above the highest memory address accessible to the process, the function fails with <b>ERROR_INVALID_PARAMETER</b>.

### -param lpBuffer [out]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-memory_basic_information">MEMORY_BASIC_INFORMATION</a> structure in which information about the specified page range is returned.

### -param dwLength [in]

The size of the buffer pointed to by the <i>lpBuffer</i> parameter, in bytes.

## -returns

The return value is the actual number of bytes returned in the information buffer.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Possible error values include <b>ERROR_INVALID_PARAMETER</b>.

## -remarks

<b>VirtualQueryEx</b> provides information about a region of consecutive pages beginning at a specified address that share the following attributes:

<ul>
<li>The state of all pages is the same (<b>MEM_COMMIT</b>, <b>MEM_RESERVE</b>, <b>MEM_FREE</b>, <b>MEM_PRIVATE</b>, <b>MEM_MAPPED</b>, or <b>MEM_IMAGE</b>).</li>
<li>If the initial page is not free, all pages in the region are part of the same initial allocation of pages created by a single call to <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a>, <a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a>, or one of the following extended versions of these functions: <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualallocex">VirtualAllocEx</a>, <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualallocexnuma">VirtualAllocExNuma</a>, <a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffileex">MapViewOfFileEx</a>, <a href="/windows/desktop/api/winbase/nf-winbase-mapviewoffileexnuma">MapViewOfFileExNuma</a>.</li>
<li>The access granted to all pages is the same (<b>PAGE_READONLY</b>, <b>PAGE_READWRITE</b>, <b>PAGE_NOACCESS</b>, <b>PAGE_WRITECOPY</b>, <b>PAGE_EXECUTE</b>, <b>PAGE_EXECUTE_READ</b>, <b>PAGE_EXECUTE_READWRITE</b>, <b>PAGE_EXECUTE_WRITECOPY</b>, <b>PAGE_GUARD</b>, or <b>PAGE_NOCACHE</b>).</li>
</ul>
The 
<b>VirtualQueryEx</b> function determines the attributes of the first page in the region and then scans subsequent pages until it scans the entire range of pages, or until it encounters a page with a nonmatching set of attributes. The function returns the attributes and the size of the region of pages with matching attributes, in bytes. For example, if there is a 40 megabyte (MB) region of free memory, and 
<b>VirtualQueryEx</b> is called on a page that is 10 MB into the region, the function will obtain a state of <b>MEM_FREE</b> and a size of 30 MB.

If a shared copy-on-write page is modified, it becomes private to the process that modified the page. However, the <b>VirtualQueryEx</b> function will continue to report such pages as <b>MEM_MAPPED</b> (for data views) or <b>MEM_IMAGE</b> (for executable image views) rather than <b>MEM_PRIVATE</b>. To detect whether copy-on-write has occurred for a specific page, either access the page or lock it using the <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtuallock">VirtualLock</a> function to make sure the page is resident in memory, then use the <a href="/windows/desktop/api/psapi/nf-psapi-queryworkingset">QueryWorkingSet</a> or <a href="/windows/desktop/api/psapi/nf-psapi-queryworkingsetex">QueryWorkingSetEx</a> function to check the <b>Shared</b> bit in the extended working set information for the page. If the <b>Shared</b> bit is clear, the page is private.

## -see-also

<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo">GetSystemInfo</a>



<a href="/windows/desktop/api/winnt/ns-winnt-memory_basic_information">MEMORY_BASIC_INFORMATION</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffileex">MapViewOfFileEx</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory
    Management Functions</a>



<a href="/windows/desktop/Memory/virtual-memory-functions">Virtual Memory Functions</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualallocex">VirtualAllocEx</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualprotectex">VirtualProtectEx</a>