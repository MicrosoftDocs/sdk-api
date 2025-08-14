---
UID: NF:processthreadsapi.GetProcessId
title: GetProcessId function (processthreadsapi.h)
description: Retrieves the process identifier of the specified process.
helpviewer_keywords: ["GetProcessId","GetProcessId function","base.getprocessid","processthreadsapi/GetProcessId","winbase/GetProcessId"]
old-location: base\getprocessid.htm
tech.root: processthreadsapi
ms.assetid: 9a024147-8bfe-427a-af12-a63f23328e38
ms.date: 12/05/2018
ms.keywords: GetProcessId, GetProcessId function, base.getprocessid, processthreadsapi/GetProcessId, winbase/GetProcessId
req.header: processthreadsapi.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP1 [desktop apps \| UWP apps]
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
 - GetProcessId
 - processthreadsapi/GetProcessId
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
 - GetProcessId
---

# GetProcessId function


## -description

Retrieves the process identifier of the specified process.

## -parameters

### -param Process [in]

A handle to the process. The handle must have the PROCESS_QUERY_INFORMATION or PROCESS_QUERY_LIMITED_INFORMATION access right. For more information, see 
<a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the PROCESS_QUERY_INFORMATION access right.

## -returns

If the function succeeds, the return value is the process identifier.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Until a process terminates, its process identifier uniquely identifies it on the system. For more information about access rights, see 
<a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid">GetCurrentProcessId</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessidofthread">GetProcessIdOfThread</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getthreadid">GetThreadId</a>



<a href="/windows/desktop/ProcThread/child-processes">Processes</a>