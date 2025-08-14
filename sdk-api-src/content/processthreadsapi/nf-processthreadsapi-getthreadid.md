---
UID: NF:processthreadsapi.GetThreadId
title: GetThreadId function (processthreadsapi.h)
description: Retrieves the thread identifier of the specified thread.
helpviewer_keywords: ["GetThreadId","GetThreadId function","base.getthreadid","processthreadsapi/GetThreadId","winbase/GetThreadId"]
old-location: base\getthreadid.htm
tech.root: processthreadsapi
ms.assetid: 198dfe9e-713f-46ce-90eb-24bfe42d2bf6
ms.date: 12/05/2018
ms.keywords: GetThreadId, GetThreadId function, base.getthreadid, processthreadsapi/GetThreadId, winbase/GetThreadId
req.header: processthreadsapi.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetThreadId
 - processthreadsapi/GetThreadId
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
 - API-MS-Win-Core-ProcessThreads-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - GetThreadId
---

# GetThreadId function


## -description

Retrieves the thread identifier of the specified thread.

## -parameters

### -param Thread [in]

A handle to the thread. The handle must have the THREAD_QUERY_INFORMATION or THREAD_QUERY_LIMITED_INFORMATION access right. For more information about access rights, see 
<a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.

<b>Windows Server 2003:  </b>The handle must have the THREAD_QUERY_INFORMATION access right.

## -returns

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Until a thread terminates, its thread identifier uniquely identifies it on the system.

To compile an application that uses this function, define _WIN32_WINNT as 0x0502 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid">GetCurrentThreadId</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessid">GetProcessId</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessidofthread">GetProcessIdOfThread</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/ProcThread/multiple-threads">Threads</a>