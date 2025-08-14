---
UID: NF:processthreadsapi.TerminateThread
title: TerminateThread function (processthreadsapi.h)
description: Terminates a thread.
helpviewer_keywords: ["TerminateThread","TerminateThread function","_win32_terminatethread","base.terminatethread","processthreadsapi/TerminateThread","winbase/TerminateThread"]
old-location: base\terminatethread.htm
tech.root: processthreadsapi
ms.assetid: ae1ad0f3-67df-4573-af22-7086f0470361
ms.date: 12/05/2018
ms.keywords: TerminateThread, TerminateThread function, _win32_terminatethread, base.terminatethread, processthreadsapi/TerminateThread, winbase/TerminateThread
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
 - TerminateThread
 - processthreadsapi/TerminateThread
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
 - TerminateThread
---

# TerminateThread function


## -description

Terminates a thread.

## -parameters

### -param hThread [in, out]

A handle to the thread to be terminated.

The handle must have the <b>THREAD_TERMINATE</b> access right. For more information, see 
<a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.

### -param dwExitCode [in]

The exit code for the thread. Use the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getexitcodethread">GetExitCodeThread</a> function to retrieve a thread's exit value.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>TerminateThread</b> is used to cause a thread to exit. When this occurs, the target thread has no chance to execute any user-mode code. DLLs attached to the thread are not notified that the thread is terminating. The system frees the thread's initial stack.

<b>Windows Server 2003 and Windows XP:  </b>The target thread's initial stack is not freed, causing a resource leak.

<b>TerminateThread</b> is a dangerous function that should only be used in the most extreme cases. You should call 
<b>TerminateThread</b> only if you know exactly what the target thread is doing, and you control all of the code that the target thread could possibly be running at the time of the termination. For example, 
<b>TerminateThread</b> can result in the following problems:

<ul>
<li>If the target thread owns a critical section, the critical section will not be released.</li>
<li>If the target thread is allocating memory from the heap, the heap lock will not be released.</li>
<li>If the target thread is executing certain kernel32 calls when it is terminated, the kernel32 state for the thread's process could be inconsistent.</li>
<li>If the target thread is manipulating the global state of a shared DLL, the state of the DLL could be destroyed, affecting other users of the DLL.</li>
</ul>
A thread cannot protect itself against 
<b>TerminateThread</b>, other than by controlling access to its handles. The thread handle returned by the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread">CreateThread</a> and 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> functions has <b>THREAD_TERMINATE</b> access, so any caller holding one of these handles can terminate your thread.

If the target thread is the last thread of a process when this function is called, the thread's process is also terminated.

The state of the thread object becomes signaled, releasing any other threads that had been waiting for the thread to terminate. The thread's termination status changes from <b>STILL_ACTIVE</b> to the value of the <i>dwExitCode</i> parameter.

Terminating a thread does not necessarily remove the thread object from the system. A thread object is deleted when the last thread handle is closed.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread">CreateThread</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getexitcodethread">GetExitCodeThread</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthread">OpenThread</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/ProcThread/terminating-a-thread">Terminating a Thread</a>



<a href="/windows/desktop/ProcThread/multiple-threads">Threads</a>