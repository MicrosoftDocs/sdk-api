---
UID: NF:memoryapi.QueryVirtualMemoryInformation
title: QueryVirtualMemoryInformation function
author: windows-sdk-content
description: The QueryVirtualMemoryInformation function returns information about a page or a set of pages within the virtual address space of the specified process.
old-location: base\queryvirtualmemoryinformation.htm
tech.root: memory
ms.assetid: D887FB6E-2594-4822-BA5E-803F9B12DCBC
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: QueryVirtualMemoryInformation, QueryVirtualMemoryInformation function, base.queryvirtualmemoryinformation, memoryapi/QueryVirtualMemoryInformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-memory-l1-1-4.dll
api_name:
 - QueryVirtualMemoryInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- QueryVirtualMemoryInformation
: 
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

If the <i>MemoryInformationClass</i> parameter has a value of  <b>MemoryRegionInfo</b>, this parameter must point to a <a href="https://msdn.microsoft.com/en-us/library/Mt845762(v=VS.85).aspx">WIN32_MEMORY_REGION_INFORMATION</a> structure.


### -param MemoryInformationSize [in]

Specifies the length in bytes of the memory information buffer.


### -param ReturnSize [out, optional]

An optional pointer which, if specified, receives the number of bytes placed in the memory information buffer.


## -returns



Returns <b>TRUE</b> on success. Returns <b>FALSE</b> for failure. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the <i>MemoryInformationClass</i> parameter has a value of <b>MemoryRegionInfo</b>, the <i>MemoryInformation</i> parameter must point to a <a href="https://msdn.microsoft.com/en-us/library/Mt845762(v=VS.85).aspx">WIN32_MEMORY_REGION_INFORMATION</a> structure. The <i>VirtualAddress</i> parameter must point to an address within a valid memory allocation. If the <i>VirtualAddress</i> parameter points to an unallocated memory region, the function fails.




## -see-also




<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>



<a href="https://msdn.microsoft.com/dc3fa48e-0986-49cc-88a9-ff8179fbe5f0">MEMORY_BASIC_INFORMATION</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt845762(v=VS.85).aspx">WIN32_MEMORY_REGION_INFORMATION</a>
 

 

