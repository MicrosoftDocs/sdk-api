---
UID: NF:processthreadsapi.GetExitCodeProcess
title: GetExitCodeProcess function (processthreadsapi.h)
description: Retrieves the termination status of the specified process.
helpviewer_keywords: ["GetExitCodeProcess","GetExitCodeProcess function","_win32_getexitcodeprocess","base.getexitcodeprocess","processthreadsapi/GetExitCodeProcess","winbase/GetExitCodeProcess"]
old-location: base\getexitcodeprocess.htm
tech.root: processthreadsapi
ms.assetid: 210f7595-ac12-4bb2-bd77-819649ebec10
ms.date: 12/05/2018
ms.keywords: GetExitCodeProcess, GetExitCodeProcess function, _win32_getexitcodeprocess, base.getexitcodeprocess, processthreadsapi/GetExitCodeProcess, winbase/GetExitCodeProcess
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
 - GetExitCodeProcess
 - processthreadsapi/GetExitCodeProcess
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
 - GetExitCodeProcess
---

# GetExitCodeProcess function


## -description

Retrieves the termination status of the specified process.

## -parameters

### -param hProcess [in]

A handle to the process.

The handle must have the <b>PROCESS_QUERY_INFORMATION</b> or <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access right. For more information, see 
<a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the <b>PROCESS_QUERY_INFORMATION</b> access right.

### -param lpExitCode [out]

A pointer to a variable to receive the process termination status. For more information, see Remarks.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function returns immediately. If the process has not terminated and the function succeeds, the status returned is <b>STILL_ACTIVE</b> (a macro for **STATUS_PENDING** (minwinbase.h)). If the process has terminated and the function succeeds, the status returned is one of the following values:

<ul>
<li>The exit value specified in the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess">ExitProcess</a> or 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess">TerminateProcess</a> function.</li>
<li>The return value from the <a href="/cpp/cpp/main-function-command-line-args">main</a> or <a href="/windows/win32/api/winbase/nf-winbase-winmain">WinMain</a> function of the process.</li>
<li>The exception value for an unhandled exception that caused the process to terminate.</li>
</ul>

> [!IMPORTANT]
> The **GetExitCodeProcess** function returns a valid error code defined by the application only after the thread terminates. Therefore, an application should not use **STILL_ACTIVE** (259) as an error code (**STILL_ACTIVE** is a macro for **STATUS_PENDING** (minwinbase.h)). If a thread returns **STILL_ACTIVE** (259) as an error code, then applications that test for that value could interpret it to mean that the thread is still running, and continue to test for the completion of the thread after the thread has terminated, which could put the application into an infinite loop.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess">ExitProcess</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/ProcThread/child-processes">Processes</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess">TerminateProcess</a>



<a href="/windows/desktop/ProcThread/terminating-a-process">Terminating a Process</a>



<a href="/windows/win32/api/winbase/nf-winbase-winmain">WinMain</a>