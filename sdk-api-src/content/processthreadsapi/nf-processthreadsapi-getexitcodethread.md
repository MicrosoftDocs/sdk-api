---
UID: NF:processthreadsapi.GetExitCodeThread
title: GetExitCodeThread function (processthreadsapi.h)
description: Retrieves the termination status of the specified thread.
helpviewer_keywords: ["GetExitCodeThread","GetExitCodeThread function","_win32_getexitcodethread","base.getexitcodethread","processthreadsapi/GetExitCodeThread","winbase/GetExitCodeThread"]
old-location: base\getexitcodethread.htm
tech.root: processthreadsapi
ms.assetid: 67482c3d-b845-4c0f-8aa1-0e3cf8cb5127
ms.date: 12/05/2018
ms.keywords: GetExitCodeThread, GetExitCodeThread function, _win32_getexitcodethread, base.getexitcodethread, processthreadsapi/GetExitCodeThread, winbase/GetExitCodeThread
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
req.lib: Kernel32.lib; WindowsPhoneCore.lib on Windows Phone 8.1
req.dll: Kernel32.dll; KernelBase.dll on Windows Phone 8.1
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetExitCodeThread
 - processthreadsapi/GetExitCodeThread
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
 - KernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - GetExitCodeThread
---

# GetExitCodeThread function


## -description

Retrieves the termination status of the specified thread.

## -parameters

### -param hThread [in]

A handle to the thread.

The handle must have the <b>THREAD_QUERY_INFORMATION</b> or <b>THREAD_QUERY_LIMITED_INFORMATION</b> access right. For more information, see 
<a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the <b>THREAD_QUERY_INFORMATION</b> access right.

### -param lpExitCode [out]

A pointer to a variable to receive the thread termination status. For more information, see Remarks.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function returns immediately. If the specified thread has not terminated and the function succeeds, the status returned is <b>STILL_ACTIVE</b>. If the thread has terminated and the function succeeds, the status returned is one of the following values:

<ul>
<li>The exit value specified in the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a> or 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread">TerminateThread</a> function.</li>
<li>The return value from the thread function.</li>
<li>The exit value of the thread's process.</li>
</ul>
<div class="alert"><b>Important</b>  The <b>GetExitCodeThread</b> function returns a valid error code defined by the application only after the thread terminates. Therefore, an application should not use <b>STILL_ACTIVE</b> (259) as an error code. If a thread returns <b>STILL_ACTIVE</b> (259) as an error code, applications that test for this value could interpret it to mean that the thread is still running and continue to test for the completion of the thread after the thread has terminated, which could put the application into an infinite loop. To avoid this problem, callers should call the <b>GetExitCodeThread</b> function only after the thread has been confirmed to have exited. Use the <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a> function with a wait duration of zero to determine whether a thread has exited. </div>
<div> </div>
<b>Windows Phone 8.1:</b> This function is supported for Windows Phone Store apps on Windows Phone 8.1 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess">GetExitCodeProcess</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthread">OpenThread</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread">TerminateThread</a>



<a href="/windows/desktop/ProcThread/terminating-a-thread">Terminating a Thread</a>