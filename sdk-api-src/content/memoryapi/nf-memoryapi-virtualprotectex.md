---
UID: NF:memoryapi.VirtualProtectEx
title: VirtualProtectEx function (memoryapi.h)
description: Changes the protection on a region of committed pages in the virtual address space of a specified process.
helpviewer_keywords: ["VirtualProtectEx","VirtualProtectEx function","_win32_virtualprotectex","base.virtualprotectex","winbase/VirtualProtectEx"]
old-location: base\virtualprotectex.htm
tech.root: base
ms.assetid: 6afd7ae6-e4c5-483c-a638-c85781674c7b
ms.date: 5/18/2022
ms.keywords: VirtualProtectEx, VirtualProtectEx function, _win32_virtualprotectex, base.virtualprotectex, winbase/VirtualProtectEx
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
 - VirtualProtectEx
 - memoryapi/VirtualProtectEx
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
 - VirtualProtectEx
---

# VirtualProtectEx function

## -description

Changes the protection on a region of committed pages in the virtual address space of a specified process.

## -parameters

### -param hProcess [in]

A handle to the process whose memory protection is to be changed. The handle must have the **PROCESS_VM_OPERATION** access right. For more information, see [Process Security and Access Rights](/windows/win32/ProcThread/process-security-and-access-rights).

### -param lpAddress [in]

A pointer to the base address of the region of pages whose access protection attributes are to be changed.

All pages in the specified region must be within the same reserved region allocated when calling the [VirtualAlloc](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) or [VirtualAllocEx](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) function using **MEM_RESERVE**. The pages cannot span adjacent reserved regions that were allocated by separate calls to **VirtualAlloc** or **VirtualAllocEx** using **MEM_RESERVE**.

### -param dwSize [in]

The size of the region whose access protection attributes are changed, in bytes. The region of affected pages includes all pages containing one or more bytes in the range from the _lpAddress_ parameter to `(lpAddress+dwSize)`. This means that a 2-byte range straddling a page boundary causes the protection attributes of both pages to be changed.

### -param flNewProtect [in]

The memory protection option. This parameter can be one of the [memory protection constants](/windows/win32/Memory/memory-protection-constants).

For mapped views, this value must be compatible with the access protection specified when the view was mapped (see [MapViewOfFile](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile), [MapViewOfFileEx](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex), and [MapViewOfFileExNuma](/windows/win32/api/winbase/nf-winbase-mapviewoffileexnuma)).

### -param lpflOldProtect [out]

A pointer to a variable that receives the previous access protection of the first page in the specified region of pages. If this parameter is **NULL** or does not point to a valid variable, the function fails.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

The access protection value can be set only on committed pages. If the state of any page in the specified region is not committed, the function fails and returns without modifying the access protection of any pages in the specified region.

The **PAGE_GUARD** protection modifier establishes guard pages. Guard pages act as one-shot access alarms. For more information, see [Creating Guard Pages](/windows/win32/Memory/creating-guard-pages).

It is best to avoid using **VirtualProtectEx** to change page protections on memory blocks allocated by [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc), [HeapAlloc](/windows/win32/api/heapapi/nf-heapapi-heapalloc), or [LocalAlloc](/windows/win32/api/winbase/nf-winbase-localalloc), because multiple memory blocks can exist on a single page. The heap manager assumes that all pages in the heap grant at least read and write access.

When protecting a region that will be executable, the calling program bears responsibility for ensuring cache coherency via an appropriate call to [FlushInstructionCache](/windows/win32/api/processthreadsapi/nf-processthreadsapi-flushinstructioncache) once the code has been set in place. Otherwise attempts to execute code out of the newly executable region may produce unpredictable results.

## -see-also

[Memory Management Functions](/windows/win32/Memory/memory-management-functions)

[Memory Protection Constants](/windows/win32/Memory/memory-protection-constants)

[Virtual Memory Functions](/windows/win32/Memory/virtual-memory-functions)

[VirtualAlloc](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)

[VirtualProtect](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect)

[VirtualQueryEx](/windows/win32/api/memoryapi/nf-memoryapi-virtualqueryex)
