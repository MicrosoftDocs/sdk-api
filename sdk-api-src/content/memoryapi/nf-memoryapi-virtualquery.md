---
UID: NF:memoryapi.VirtualQuery
title: VirtualQuery function (memoryapi.h)
description: Retrieves information about a range of pages in the virtual address space of the calling process.
helpviewer_keywords: ["VirtualQuery","VirtualQuery function","_win32_virtualquery","base.virtualquery","winbase/VirtualQuery"]
old-location: base\virtualquery.htm
tech.root: base
ms.assetid: 3b1f7d27-1f5d-452e-b58f-560cd9b9cbd3
ms.date: 02/05/2024
ms.keywords: VirtualQuery, VirtualQuery function, _win32_virtualquery, base.virtualquery, winbase/VirtualQuery
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
 - VirtualQuery
 - memoryapi/VirtualQuery
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
 - vertdll.dll
api_name:
 - VirtualQuery
---

# VirtualQuery function

## -description

Retrieves information about a range of pages in the virtual address space of the calling process.

To retrieve information about a range of pages in the address space of another process, use the [VirtualQueryEx](nf-memoryapi-virtualqueryex.md) function.

## -parameters

### -param lpAddress [in, optional]

A pointer to the base address of the region of pages to be queried. This value is rounded down to the next page boundary. To determine the size of a page on the host computer, use the [GetSystemInfo](../sysinfoapi/nf-sysinfoapi-getsysteminfo.md) function.

If *lpAddress* specifies an address above the highest memory address accessible to the process, the function fails with **ERROR_INVALID_PARAMETER**.

### -param lpBuffer [out]

A pointer to a [MEMORY_BASIC_INFORMATION](../winnt/ns-winnt-memory_basic_information.md) structure in which information about the specified page range is returned.

### -param dwLength [in]

The size of the buffer pointed to by the *lpBuffer* parameter, in bytes.

## -returns

The return value is the actual number of bytes returned in the information buffer.

If the function fails, the return value is zero. To get extended error information, call [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md). Possible error values include **ERROR_INVALID_PARAMETER**.

## -remarks

**VirtualQuery** provides information about a region of consecutive pages beginning at a specified address that share the following attributes:

- The state of all pages is the same (**MEM_COMMIT**, **MEM_RESERVE**, **MEM_FREE**, **MEM_PRIVATE**, **MEM_MAPPED**, or **MEM_IMAGE**).
- If the initial page is not free, all pages in the region are part of the same initial allocation of pages created by a single call to [VirtualAlloc](nf-memoryapi-virtualalloc.md), [MapViewOfFile](nf-memoryapi-mapviewoffile.md), or one of the following extended versions of these functions: [VirtualAllocEx](nf-memoryapi-virtualallocex.md), [VirtualAllocExNuma](nf-memoryapi-virtualallocexnuma.md), [MapViewOfFileEx](nf-memoryapi-mapviewoffileex.md), [MapViewOfFileExNuma](../winbase/nf-winbase-mapviewoffileexnuma.md).
- The access granted to all pages is the same (**PAGE_READONLY**, **PAGE_READWRITE**, **PAGE_NOACCESS**, **PAGE_WRITECOPY**, **PAGE_EXECUTE**, **PAGE_EXECUTE_READ**, **PAGE_EXECUTE_READWRITE**, **PAGE_EXECUTE_WRITECOPY**, **PAGE_GUARD**, or **PAGE_NOCACHE**).

The function determines the attributes of the first page in the region and then scans subsequent pages until it scans the entire range of pages or until it encounters a page with a non-matching set of attributes. The function returns the attributes and the size of the region of pages with matching attributes, in bytes. For example, if there is a 40 megabyte (MB) region of free memory, and **VirtualQuery** is called on a page that is 10 MB into the region, the function will obtain a state of **MEM_FREE** and a size of 30 MB.

If a shared copy-on-write page is modified, it becomes private to the process that modified the page. However, the **VirtualQuery** function will continue to report such pages as **MEM_MAPPED** (for data views) or **MEM_IMAGE** (for executable image views) rather than **MEM_PRIVATE**. To detect whether copy-on-write has occurred for a specific page, either access the page or lock it using the [VirtualLock](nf-memoryapi-virtuallock.md) function to make sure the page is resident in memory, then use the [QueryWorkingSetEx](../psapi/nf-psapi-queryworkingsetex.md) function to check the **Shared** bit in the extended working set information for the page. If the **Shared** bit is clear, the page is private.

This function reports on a region of pages in the memory of the calling process, and the [VirtualQueryEx](nf-memoryapi-virtualqueryex.md) function reports on a region of pages in the memory of a specified process.

## -see-also

[GetSystemInfo](../sysinfoapi/nf-sysinfoapi-getsysteminfo.md)

[MEMORY_BASIC_INFORMATION](../winnt/ns-winnt-memory_basic_information.md)

[MapViewOfFile](nf-memoryapi-mapviewoffile.md)

[Memory Management Functions](/windows/win32/Memory/memory-management-functions)

[Virtual Memory Functions](/windows/win32/Memory/virtual-memory-functions)

[VirtualQueryEx](nf-memoryapi-virtualqueryex.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
