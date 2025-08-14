---
UID: NF:memoryapi.PrefetchVirtualMemory
title: PrefetchVirtualMemory function (memoryapi.h)
description: Provides an efficient mechanism to bring into memory potentially discontiguous virtual address ranges in a process address space.
helpviewer_keywords: ["PrefetchVirtualMemory","PrefetchVirtualMemory function","base.prefetchvirtualmemory","winbase/PrefetchVirtualMemory"]
old-location: base\prefetchvirtualmemory.htm
tech.root: base
ms.assetid: a7aeeb66-afd0-4871-81a3-e4619ac84293
ms.date: 12/05/2018
ms.keywords: PrefetchVirtualMemory, PrefetchVirtualMemory function, base.prefetchvirtualmemory, winbase/PrefetchVirtualMemory
req.header: memoryapi.h
req.include-header: Windows.h, Memoryapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - PrefetchVirtualMemory
 - memoryapi/PrefetchVirtualMemory
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
 - API-MS-Win-Core-memory-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-2.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - PrefetchVirtualMemory
---

# PrefetchVirtualMemory function


## -description

Provides an efficient mechanism to bring into memory potentially discontiguous virtual address ranges 
    in a process address space.

## -parameters

### -param hProcess [in]

Handle to the process whose virtual address ranges are to be prefetched. Use the 
      <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess">GetCurrentProcess</a> function to use the current 
      process.

### -param NumberOfEntries [in]

Number of entries in the array pointed to by the <i>VirtualAddresses</i> 
      parameter.

### -param VirtualAddresses [in]

Pointer to an array of 
      <a href="/windows/desktop/api/memoryapi/ns-memoryapi-win32_memory_range_entry">WIN32_MEMORY_RANGE_ENTRY</a> structures which 
      each specify a virtual address range to be prefetched. The virtual address ranges may cover any part of the 
      process address space accessible by the target process.

### -param Flags [in]

Reserved. Must be 0.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is 0 (zero). To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>PrefetchVirtualMemory</b> function is 
     targeted at applications that know with reasonable confidence the set of addresses they will be accessing. If 
     it's likely that these addresses are no longer resident in memory (i.e. they have been paged out to disk), 
     calling the <b>PrefetchVirtualMemory</b> function on 
     those address ranges before access will reduce the overall latency because the API will efficiently bring in 
     those address ranges from disk using large, concurrent I/O requests where possible.

The <b>PrefetchVirtualMemory</b> function allows 
     applications to make efficient use of disk hardware by issuing large, concurrent I/Os where possible when the 
     application provides a list of process address ranges that are going to be accessed. Even for a single address 
     range (e.g. a file mapping), the 
     <b>PrefetchVirtualMemory</b> function can provide 
     performance improvements by issuing a single large I/O rather than the many smaller I/Os that would be issued via 
     page faulting.

The <b>PrefetchVirtualMemory</b> function is purely 
     a performance optimization: prefetching is not necessary for accessing the target address ranges. The prefetched 
     memory is not added to the target process' working set; it is cached in physical memory. When the prefetched 
     address ranges are accessed by the target process, they will be added to the working set.

Since the <b>PrefetchVirtualMemory</b> function can 
     never be necessary for correct operation of applications, it is treated as a strong hint by the system and is 
     subject to usual physical memory constraints where it can completely or partially fail under low-memory 
     conditions. It can also create memory pressure if called with large address ranges, so applications should only 
     prefetch address ranges they will actually use.

To compile an application that calls this function, define <b>_WIN32_WINNT</b> as 
    <b>_WIN32_WINNT_WIN8</b> or higher. For more information, see 
    <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/Memory/memory-management-functions">Memory Management Functions</a>



<a href="/windows/desktop/api/memoryapi/ns-memoryapi-win32_memory_range_entry">WIN32_MEMORY_RANGE_ENTRY</a>