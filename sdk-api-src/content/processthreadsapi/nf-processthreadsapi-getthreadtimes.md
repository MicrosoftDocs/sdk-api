---
UID: NF:processthreadsapi.GetThreadTimes
title: GetThreadTimes function (processthreadsapi.h)
description: Retrieves timing information for the specified thread.
helpviewer_keywords: ["GetThreadTimes","GetThreadTimes function","_win32_getthreadtimes","base.getthreadtimes","processthreadsapi/GetThreadTimes","winbase/GetThreadTimes"]
old-location: base\getthreadtimes.htm
tech.root: processthreadsapi
ms.assetid: eb61aa05-15d8-4251-947a-54df8433b858
ms.date: 12/05/2018
ms.keywords: GetThreadTimes, GetThreadTimes function, _win32_getthreadtimes, base.getthreadtimes, processthreadsapi/GetThreadTimes, winbase/GetThreadTimes
req.header: processthreadsapi.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
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
 - GetThreadTimes
 - processthreadsapi/GetThreadTimes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-processthreads-l1-1-8.dll
 - api-ms-win-core-processthreads-l1-1-7.dll
 - api-ms-win-core-processthreads-l1-1-6.dll
 - api-ms-win-core-processthreads-l1-1-5.dll
 - api-ms-win-core-processthreads-l1-1-4.dll
 - Kernel32.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - GetThreadTimes
---

# GetThreadTimes function


## -description

Retrieves timing information for the specified thread.

## -parameters

### -param hThread [in]

A handle to the thread whose timing information is sought. The handle must have the <b>THREAD_QUERY_INFORMATION</b> or <b>THREAD_QUERY_LIMITED_INFORMATION</b> access right. For more information, see 
<a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the <b>THREAD_QUERY_INFORMATION</b> access right.

### -param lpCreationTime [out]

A pointer to a 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that receives the creation time of the thread.

### -param lpExitTime [out]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that receives the exit time of the thread. If the thread has not exited, the content of this structure is undefined.

### -param lpKernelTime [out]

A pointer to a 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that receives the amount of time that the thread has executed in kernel mode.

### -param lpUserTime [out]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that receives the amount of time that the thread has executed in user mode.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All times are expressed using 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> data structures. Such a structure contains two 32-bit values that combine to form a 64-bit count of 100-nanosecond time units.

Thread creation and exit times are points in time expressed as the amount of time that has elapsed since midnight on January 1, 1601 at Greenwich, England. There are several functions that an application can use to convert such values to more generally useful forms; see 
<a href="/windows/desktop/SysInfo/time-functions">Time Functions</a>.

Thread kernel mode and user mode times are amounts of time. For example, if a thread has spent one second in kernel mode, this function will fill the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure specified by <i>lpKernelTime</i> with a 64-bit value of ten million. That is the number of 100-nanosecond units in one second.

To retrieve the number of CPU clock cycles used by the threads, use the <a href="/windows/desktop/api/realtimeapiset/nf-realtimeapiset-querythreadcycletime">QueryThreadCycleTime</a> function.

## -see-also

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="/windows/desktop/api/winbase/nf-winbase-filetimetodosdatetime">FileTimeToDosDateTime</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime">FileTimeToLocalFileTime</a>



<a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-filetimetosystemtime">FileTimeToSystemTime</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthread">OpenThread</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/ProcThread/multiple-threads">Threads</a>