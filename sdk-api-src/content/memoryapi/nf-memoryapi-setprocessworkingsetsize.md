---
UID: NF:memoryapi.SetProcessWorkingSetSize
tech.root: backup
title: SetProcessWorkingSetSize
ms.date: 06/02/2021
targetos: Windows
description: Sets the minimum and maximum working set sizes for the specified process. (SetProcessWorkingSetSize)
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Kernel32.dll
req.header: memoryapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: onecore.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - api-ms-win-core-memory-l1-1-9.dll
 - api-ms-win-core-memory-l1-1-8.dll
 - api-ms-win-core-memory-l1-1-7.dll
 - api-ms-win-core-memory-l1-1-6.dll
 - api-ms-win-core-memory-l1-1-4.dll
 - api-ms-win-core-memory-l1-1-3.dll
 - api-ms-win-core-memory-l1-1-2.dll
 - api-ms-win-core-memory-l1-1-1.dll
 - Kernel32.dll
 - api-ms-win-core-memory-l1-1-5.dll
api_name:
 - SetProcessWorkingSetSize
f1_keywords:
 - SetProcessWorkingSetSize
 - memoryapi/SetProcessWorkingSetSize
dev_langs:
 - c++
---

# SetProcessWorkingSetSize function

## -description

Sets the minimum and maximum working set sizes for the specified process.

## -parameters

### -param hProcess [in]

A handle to the process whose working set sizes is to be set. 


The handle must have the <b>PROCESS_SET_QUOTA</b> access right. For more information, see 
<a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

### -param dwMinimumWorkingSetSize [in]

The minimum working set size for the process, in bytes. The virtual memory manager attempts to keep at least this much memory resident in the process whenever the process is active. 

This parameter must be greater than zero but less than or equal to the maximum working set size. The default size is 50 pages (for example, this is 204,800 bytes on systems with a 4K page size). If the value is greater than zero but less than 20 pages, the minimum value is set to 20 pages.

If both <i>dwMinimumWorkingSetSize</i> and <i>dwMaximumWorkingSetSize</i> have the value (<b>SIZE_T</b>)–1, the function removes as many pages as possible from the working set of the specified process.

### -param dwMaximumWorkingSetSize [in]

The maximum working set size for the process, in bytes. The virtual memory manager attempts to keep no more than this much memory resident in the process whenever the process is active and available memory is low. 




This parameter must be greater than or equal to 13 pages (for example, 53,248 on systems with a 4K page size), and less than the system-wide maximum (number of available pages minus 512 pages). The default size is 345 pages (for example, this is 1,413,120 bytes on systems with a 4K page size).

If both <i>dwMinimumWorkingSetSize</i> and <i>dwMaximumWorkingSetSize</i> have the value (<b>SIZE_T</b>)–1, the function removes as many pages as possible from the working set of the specified process.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. Call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to obtain extended error information.

## -remarks

The working set of a process is the set of memory pages in the virtual address space of the process that are currently resident in physical memory. These pages are available for an application to use without triggering a page fault. For more information about page faults, see <a href="/windows/desktop/Memory/working-set">Working Set</a>. The minimum and maximum working set sizes affect the virtual memory paging behavior of a process.

The working set of the specified process can be emptied by specifying the value (<b>SIZE_T</b>)–1 for both the minimum and maximum working set sizes. This removes as many pages as possible from the working set. The <a href="/windows/desktop/api/psapi/nf-psapi-emptyworkingset">EmptyWorkingSet</a> function can also be used for this purpose.

If the values of either <i>dwMinimumWorkingSetSize</i> or <i>dwMaximumWorkingSetSize</i> are greater than the process' current working set sizes, the specified process must have the <b>SE_INC_WORKING_SET_NAME</b> privilege. All users generally have this privilege. For more information about security privileges, see 
<a href="/windows/desktop/SecAuthZ/privileges">Privileges</a>.

<b>Windows Server 2003 and Windows XP:  </b>The specified process must have the <b>SE_INC_BASE_PRIORITY_NAME</b> privilege. Users in the Administrators and Power Users groups generally have this privilege. 

The operating system allocates working set sizes on a first-come, first-served basis. For example, if an application successfully sets 40 megabytes as its minimum working set size on a 64-megabyte system, and a second application requests a 40-megabyte working set size, the operating system denies the second application's request.

Using the <b>SetProcessWorkingSetSize</b> function to set an application's minimum and maximum working set sizes does not guarantee that the requested memory will be reserved, or that it will remain resident at all times. When the application is idle, or a low-memory situation causes a demand for memory, the operating system can reduce the application's working set. An application can use the <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtuallock">VirtualLock</a>function to lock ranges of the application's virtual address space in memory; however, that can potentially degrade the performance of the system.

When you increase the working set size of an application, you are taking away physical memory from the rest of the system. This can degrade the performance of other applications and the system as a whole. It can also lead to failures of operations that require physical memory to be present (for example, creating processes, threads, and kernel pool). Thus, you must use the 
**SetProcessWorkingSetSize** function carefully. You must always consider the performance of the whole system when you are designing an application.

## -see-also

<a href="/windows/win32/api/memoryapi/nf-memoryapi-getprocessworkingsetsize">GetProcessWorkingSetSize</a>



<a href="/windows/desktop/ProcThread/process-working-set">Process Working Set</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/ProcThread/child-processes">Processes</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex">SetProcessWorkingSetSizeEx</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtuallock">VirtualLock</a>
