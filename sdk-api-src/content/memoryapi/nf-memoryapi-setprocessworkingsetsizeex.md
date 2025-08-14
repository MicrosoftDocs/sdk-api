---
UID: NF:memoryapi.SetProcessWorkingSetSizeEx
title: SetProcessWorkingSetSizeEx function (memoryapi.h)
description: Sets the minimum and maximum working set sizes for the specified process. (SetProcessWorkingSetSizeEx)
helpviewer_keywords: ["QUOTA_LIMITS_HARDWS_MAX_DISABLE","QUOTA_LIMITS_HARDWS_MAX_ENABLE","QUOTA_LIMITS_HARDWS_MIN_DISABLE","QUOTA_LIMITS_HARDWS_MIN_ENABLE","SetProcessWorkingSetSizeEx","SetProcessWorkingSetSizeEx function","base.setprocessworkingsetsizeex","memoryapi/SetProcessWorkingSetSizeEx","winbase/SetProcessWorkingSetSizeEx"]
old-location: base\setprocessworkingsetsizeex.htm
tech.root: backup
ms.assetid: 04332239-dfc2-4d32-987a-af187e725b71
ms.date: 12/05/2018
ms.keywords: QUOTA_LIMITS_HARDWS_MAX_DISABLE, QUOTA_LIMITS_HARDWS_MAX_ENABLE, QUOTA_LIMITS_HARDWS_MIN_DISABLE, QUOTA_LIMITS_HARDWS_MIN_ENABLE, SetProcessWorkingSetSizeEx, SetProcessWorkingSetSizeEx function, base.setprocessworkingsetsizeex, memoryapi/SetProcessWorkingSetSizeEx, winbase/SetProcessWorkingSetSizeEx
req.header: memoryapi.h
req.include-header: Windows.h on Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
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
 - SetProcessWorkingSetSizeEx
 - memoryapi/SetProcessWorkingSetSizeEx
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
 - API-MS-Win-Core-Memory-l1-1-1.dll
 - API-MS-Win-Core-Memory-l1-1-2.dll
 - API-MS-Win-Core-Memory-l1-1-3.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
api_name:
 - SetProcessWorkingSetSizeEx
---

# SetProcessWorkingSetSizeEx function


## -description

Sets the minimum and maximum working set sizes for the specified process.

## -parameters

### -param hProcess [in]

A handle to the process whose working set sizes is to be set.

The handle must have <b>PROCESS_SET_QUOTA</b> access rights. For more information, see 
<a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

### -param dwMinimumWorkingSetSize [in]

The minimum working set size for the process, in bytes. The virtual memory manager attempts to keep at least this much memory resident in the process whenever the process is active.

This parameter must be greater than zero but less than or equal to the maximum working set size. The default size is 50 pages (for example, this is 204,800 bytes on systems with a 4K page size). If the value is greater than zero but less than 20 pages, the minimum value is set to 20 pages.

If both <i>dwMinimumWorkingSetSize</i> and <i>dwMaximumWorkingSetSize</i> have the value (<b>SIZE_T</b>)–1, the function removes as many pages as possible from the working set of the specified process.

### -param dwMaximumWorkingSetSize [in]

The maximum working set size for the process, in bytes. The virtual memory manager attempts to keep no more than this much memory resident in the process whenever the process is active and available memory is low.

This parameter must be greater than or equal to 13 pages (for example, 53,248 on systems with a 4K page size), and less than the system-wide maximum (number of available pages minus 512 pages). The default size is 345 pages (for example, this is 1,413,120 bytes on systems with a 4K page size).

If both <i>dwMinimumWorkingSetSize</i> and <i>dwMaximumWorkingSetSize</i> have the value (<b>SIZE_T</b>)–1, the function removes as many pages as possible from the working set of the specified process. For details, see Remarks.

### -param Flags [in]

The flags that control the enforcement of the minimum and maximum working set sizes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="QUOTA_LIMITS_HARDWS_MIN_DISABLE"></a><a id="quota_limits_hardws_min_disable"></a><dl>
<dt><b>QUOTA_LIMITS_HARDWS_MIN_DISABLE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The working set may fall below the minimum working set limit if memory demands are high.

This flag cannot be used with <b>QUOTA_LIMITS_HARDWS_MIN_ENABLE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="QUOTA_LIMITS_HARDWS_MIN_ENABLE"></a><a id="quota_limits_hardws_min_enable"></a><dl>
<dt><b>QUOTA_LIMITS_HARDWS_MIN_ENABLE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The working set will not fall below the minimum working set limit.

This flag cannot be used with <b>QUOTA_LIMITS_HARDWS_MIN_DISABLE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="QUOTA_LIMITS_HARDWS_MAX_DISABLE"></a><a id="quota_limits_hardws_max_disable"></a><dl>
<dt><b>QUOTA_LIMITS_HARDWS_MAX_DISABLE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
<i>The working set may exceed the maximum working set limit if there is abundant memory.</i>

This flag cannot be used with <b>QUOTA_LIMITS_HARDWS_MAX_ENABLE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="QUOTA_LIMITS_HARDWS_MAX_ENABLE"></a><a id="quota_limits_hardws_max_enable"></a><dl>
<dt><b>QUOTA_LIMITS_HARDWS_MAX_ENABLE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The working set will not exceed the maximum working set limit.

This flag cannot be used with <b>QUOTA_LIMITS_HARDWS_MAX_DISABLE</b>.

</td>
</tr>
</table>

## -returns

If the function is succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. If the function fails, the return value is zero. To get extended error information, call 
<b>GetLastError</b>.

## -remarks

The working set of a process is the set of memory pages in the virtual address space of the process that are currently resident in physical memory. These pages are available for an application to use without triggering a page fault. For more information about page faults, see <a href="/windows/desktop/Memory/working-set">Working Set</a>. The minimum and maximum working set sizes affect the virtual memory paging behavior of a process.

The working set of the specified process can be emptied by specifying the value (<b>SIZE_T</b>)–1 for both the minimum and maximum working set sizes. This removes as many pages as possible from the working set. The <a href="/windows/desktop/api/psapi/nf-psapi-emptyworkingset">EmptyWorkingSet</a> function can also be used for this purpose.

If the values of either <i>dwMinimumWorkingSetSize</i> or <i>dwMaximumWorkingSetSize</i> are greater than the process' current working set sizes, the specified process must have the <b>SE_INC_WORKING_SET_NAME</b> privilege. All users generally have this privilege. For more information about security privileges, see 
<a href="/windows/desktop/SecAuthZ/privileges">Privileges</a>.

<b>Windows Server 2003:  </b>The specified process must have the <b>SE_INC_BASE_PRIORITY_NAME</b> privilege. Users in the Administrators and Power Users groups generally have this privilege.

The operating system allocates working set sizes on a first-come, first-served basis. For example, if an application successfully sets 40 megabytes as its minimum working set size on a 64-megabyte system, and a second application requests a 40-megabyte working set size, the operating system denies the second application's request.

By default, using the 
<a href="/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsize">SetProcessWorkingSetSize</a> function to set an application's minimum and maximum working set sizes does not guarantee that the requested memory will be reserved, or that it will remain resident at all times. When an application is idle, or a low-memory situation causes a demand for memory, the operating system can reduce the application's working set below its minimum working set limit. If memory is abundant, the system might allow an application to exceed its maximum working set limit. The <b>QUOTA_LIMITS_HARDWS_MIN_ENABLE</b> and <b>QUOTA_LIMITS_HARDWS_MAX_ENABLE</b> flags enable you to ensure that limits are enforced.

When you increase the working set size of an application, you are taking away physical memory from the rest of the system. This can degrade the performance of other applications and the system as a whole. It can also lead to failures of operations that require physical memory to be present (for example, creating processes, threads, and kernel pool). Thus, you must use the 
<a href="/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsize">SetProcessWorkingSetSize</a> function carefully. You must always consider the performance of the whole system when you are designing an application.

An application can use the 
<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtuallock">VirtualLock</a> function to lock ranges of the application's virtual address space in memory; however, that can potentially degrade the performance of the system.

## -see-also

<a href="/windows/desktop/api/memoryapi/nf-memoryapi-getprocessworkingsetsizeex">GetProcessWorkingSetSizeEx</a>



<a href="/windows/desktop/ProcThread/process-working-set">Process Working Set</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/ProcThread/child-processes">Processes</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtuallock">VirtualLock</a>



<a href="/windows/desktop/Memory/working-set">Working Set</a>
