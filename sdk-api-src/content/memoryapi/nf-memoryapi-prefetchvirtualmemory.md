---
UID: NF:memoryapi.PrefetchVirtualMemory
title: PrefetchVirtualMemory function
author: windows-sdk-content
description: Provides an efficient mechanism to bring into memory potentially discontiguous virtual address ranges in a process address space.
old-location: base\prefetchvirtualmemory.htm
tech.root: memory
ms.assetid: a7aeeb66-afd0-4871-81a3-e4619ac84293
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: PrefetchVirtualMemory, PrefetchVirtualMemory function, base.prefetchvirtualmemory, winbase/PrefetchVirtualMemory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-memory-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-2.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - PrefetchVirtualMemory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PrefetchVirtualMemory function


## -description


Provides an efficient mechanism to bring into memory potentially discontiguous virtual address ranges 
    in a process address space.


## -parameters




### -param hProcess [in]

Handle to the process whose virtual address ranges are to be prefetched. Use the 
      <a href="https://msdn.microsoft.com/0471790c-3bb9-4180-8676-941e655b1812">GetCurrentProcess</a> function to use the current 
      process.


### -param NumberOfEntries [in]

Number of entries in the array pointed to by the <i>VirtualAddresses</i> 
      parameter.


### -param VirtualAddresses [in]

Pointer to an array of 
      <a href="https://msdn.microsoft.com/d1372687-c397-4ba8-b0c0-2dcf2ec74fbb">WIN32_MEMORY_RANGE_ENTRY</a> structures which 
      each specify a virtual address range to be prefetched. The virtual address ranges may cover any part of the 
      process address space accessible by the target process.


### -param Flags [in]

Reserved. Must be 0.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is 0 (zero). To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




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
    <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory Management Functions</a>



<a href="https://msdn.microsoft.com/d1372687-c397-4ba8-b0c0-2dcf2ec74fbb">WIN32_MEMORY_RANGE_ENTRY</a>
 

 

