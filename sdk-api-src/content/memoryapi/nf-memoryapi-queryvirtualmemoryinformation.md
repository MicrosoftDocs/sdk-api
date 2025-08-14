---
UID: NF:memoryapi.QueryVirtualMemoryInformation
title: QueryVirtualMemoryInformation function (memoryapi.h)
description: The QueryVirtualMemoryInformation function returns information about a page or a set of pages within the virtual address space of the specified process.
helpviewer_keywords: ["QueryVirtualMemoryInformation","QueryVirtualMemoryInformation function","base.queryvirtualmemoryinformation","memoryapi/QueryVirtualMemoryInformation"]
old-location: base\queryvirtualmemoryinformation.htm
tech.root: base
ms.assetid: D887FB6E-2594-4822-BA5E-803F9B12DCBC
ms.date: 12/05/2018
ms.keywords: QueryVirtualMemoryInformation, QueryVirtualMemoryInformation function, base.queryvirtualmemoryinformation, memoryapi/QueryVirtualMemoryInformation
req.header: memoryapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Onecore.lib
req.dll: Api-ms-win-core-memory-l1-1-4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - QueryVirtualMemoryInformation
 - memoryapi/QueryVirtualMemoryInformation
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
 - api-ms-win-core-memory-l1-1-4.dll
api_name:
 - QueryVirtualMemoryInformation
---

# QueryVirtualMemoryInformation function


## -description

The <b>QueryVirtualMemoryInformation</b> function returns information about a page or a set of pages within the virtual address space of the specified process.

## -parameters

### -param Process [in]

A handle for the process in whose context the pages to be queried reside.

### -param VirtualAddress [in]

The address of the region of pages to be queried. This value is rounded down to the next host-page-address boundary.

### -param MemoryInformationClass [in]

The memory information class about which to retrieve information. The only supported value is <b>MemoryRegionInfo</b>.

### -param MemoryInformation [out]

A pointer to a buffer that receives the specified information.

If the <i>MemoryInformationClass</i> parameter has a value of  <b>MemoryRegionInfo</b>, this parameter must point to a <a href="/windows/desktop/api/memoryapi/ns-memoryapi-win32_memory_region_information">WIN32_MEMORY_REGION_INFORMATION</a> structure.

### -param MemoryInformationSize [in]

Specifies the length in bytes of the memory information buffer.

### -param ReturnSize [out, optional]

An optional pointer which, if specified, receives the number of bytes placed in the memory information buffer.

## -returns

Returns <b>TRUE</b> on success. Returns <b>FALSE</b> for failure. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the <i>MemoryInformationClass</i> parameter has a value of <b>MemoryRegionInfo</b>, the <i>MemoryInformation</i> parameter must point to a <a href="/windows/desktop/api/memoryapi/ns-memoryapi-win32_memory_region_information">WIN32_MEMORY_REGION_INFORMATION</a> structure. The <i>VirtualAddress</i> parameter must point to an address within a valid memory allocation. If the <i>VirtualAddress</i> parameter points to an unallocated memory region, the function fails.

## -see-also

<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="/windows/desktop/api/winnt/ns-winnt-memory_basic_information">MEMORY_BASIC_INFORMATION</a>



<a href="/windows/desktop/api/memoryapi/ns-memoryapi-win32_memory_region_information">WIN32_MEMORY_REGION_INFORMATION</a>