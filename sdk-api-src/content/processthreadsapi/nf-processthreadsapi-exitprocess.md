---
UID: NF:processthreadsapi.ExitProcess
title: ExitProcess function (processthreadsapi.h)
description: Ends the calling process and all its threads.
helpviewer_keywords: ["ExitProcess","ExitProcess function","_win32_exitprocess","base.exitprocess","processthreadsapi/ExitProcess","winbase/ExitProcess"]
old-location: base\exitprocess.htm
tech.root: processthreadsapi
ms.assetid: c26dbf15-62e8-4892-b7c5-2e6c085e4cd5
ms.date: 12/05/2018
ms.keywords: ExitProcess, ExitProcess function, _win32_exitprocess, base.exitprocess, processthreadsapi/ExitProcess, winbase/ExitProcess
req.header: processthreadsapi.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - ExitProcess
 - processthreadsapi/ExitProcess
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
 - ExitProcess
---

# ExitProcess function


## -description

Ends the calling process and all its threads.

## -parameters

### -param uExitCode [in]

The exit code for the process and all threads.

## -remarks

Use the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess">GetExitCodeProcess</a> function to retrieve the process's exit value. Use the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getexitcodethread">GetExitCodeThread</a> function to retrieve a thread's exit value.

Exiting a process causes the following:

<ol>
<li>All of the threads in the process, except the calling thread, terminate their execution without receiving a DLL_THREAD_DETACH notification.</li>
<li>The states of all of the threads terminated in step 1 become signaled.</li>
<li>The entry-point functions of all loaded dynamic-link libraries (DLLs) are called with DLL_PROCESS_DETACH. </li>
<li>After all attached DLLs have executed any process termination code, the <b>ExitProcess</b> function terminates the current process, including the calling thread.</li>
<li>The state of the calling thread becomes signaled.</li>
<li>All of the object handles opened by the process are closed.</li>
<li>The termination status of the process changes from STILL_ACTIVE to the exit value of the process.</li>
<li>The state of the process object becomes signaled, satisfying any threads that had been waiting for the process to terminate.</li>
</ol>
If one of the terminated threads in the process holds a lock and the DLL detach code in one of the loaded DLLs attempts to acquire the same lock, then calling <b>ExitProcess</b> results in a deadlock. In contrast, if a process terminates by calling 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess">TerminateProcess</a>, the DLLs that the process is attached to are not notified of the process termination. Therefore, if you do not know the state of all threads in your process, it is better to call <b>TerminateProcess</b> than  <b>ExitProcess</b>. Note that returning from the <b>main</b> function of an application results in a call to <b>ExitProcess</b>.

Calling 
<b>ExitProcess</b> in a DLL can lead to unexpected application or system errors. Be sure to call 
<b>ExitProcess</b> from a DLL only if you know which applications or system components will load the DLL and that it is safe to call 
<b>ExitProcess</b> in this context. 

Exiting a process does not cause child processes to be terminated.

Exiting a process does not necessarily remove the process object from the operating system. A process object is deleted when the last handle to the process is closed.


#### Examples

For an example, see 
<a href="/windows/desktop/ProcThread/creating-a-child-process-with-redirected-input-and-output">Creating a Child Process with Redirected Input and Output</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createremotethread">CreateRemoteThread</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread">CreateThread</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess">GetExitCodeProcess</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getexitcodethread">GetExitCodeThread</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess">OpenProcess</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/ProcThread/child-processes">Processes</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess">TerminateProcess</a>



<a href="/windows/desktop/ProcThread/terminating-a-process">Terminating a Process</a>