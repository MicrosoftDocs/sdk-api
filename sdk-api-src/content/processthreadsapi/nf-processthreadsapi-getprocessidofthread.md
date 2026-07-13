---
UID: NF:processthreadsapi.GetProcessIdOfThread
title: GetProcessIdOfThread function (processthreadsapi.h)
description: Retrieves the process identifier of the process associated with the specified thread.
helpviewer_keywords: ["GetProcessIdOfThread","GetProcessIdOfThread function","base.getprocessidofthread","processthreadsapi/GetProcessIdOfThread","winbase/GetProcessIdOfThread"]
old-location: base\getprocessidofthread.htm
tech.root: processthreadsapi
ms.assetid: 1878088b-e0fd-4009-b608-f491805948b5
ms.date: 12/05/2018
ms.keywords: GetProcessIdOfThread, GetProcessIdOfThread function, base.getprocessidofthread, processthreadsapi/GetProcessIdOfThread, winbase/GetProcessIdOfThread
req.header: processthreadsapi.h
req.include-header: Windows.h on Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - GetProcessIdOfThread
 - processthreadsapi/GetProcessIdOfThread
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
 - GetProcessIdOfThread
---

# GetProcessIdOfThread function


## -description

Retrieves the process identifier of the process associated with the specified thread.

## -parameters

### -param Thread [in]

 A handle to the thread. The handle must have the THREAD_QUERY_INFORMATION or THREAD_QUERY_LIMITED_INFORMATION access right. For more information, see 
<a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.

<b>Windows Server 2003:  </b>The handle must have the THREAD_QUERY_INFORMATION access right.

## -returns

If the function succeeds, the return value is the process identifier of the process associated with the specified thread.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Until a process terminates, its process identifier uniquely identifies it on the system. For more information about access rights, see 
<a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid">GetCurrentThreadId</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessid">GetProcessId</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getthreadid">GetThreadId</a>



<a href="/windows/desktop/ProcThread/child-processes">Processes</a>