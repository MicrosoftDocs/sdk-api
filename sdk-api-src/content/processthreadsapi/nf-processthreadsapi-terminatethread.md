---
UID: NF:processthreadsapi.TerminateThread
title: TerminateThread function
author: windows-sdk-content
description: Terminates a thread.
old-location: base\terminatethread.htm
old-project: ProcThread
ms.assetid: ae1ad0f3-67df-4573-af22-7086f0470361
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: TerminateThread, TerminateThread function, _win32_terminatethread, base.terminatethread, processthreadsapi/TerminateThread, winbase/TerminateThread
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
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
tech.root: 
req.typenames: PSS_VA_SPACE_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# TerminateThread function


## -description


Terminates a thread.


## -parameters




### -param hThread [in, out]

A handle to the thread to be terminated.

The handle must have the <b>THREAD_TERMINATE</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/72709446-5c59-4fac-8dc8-7912906ecc85">Thread Security and Access Rights</a>.


### -param dwExitCode [in]

The exit code for the thread. Use the 
<a href="https://msdn.microsoft.com/67482c3d-b845-4c0f-8aa1-0e3cf8cb5127">GetExitCodeThread</a> function to retrieve a thread's exit value.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




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
<a href="https://msdn.microsoft.com/202a4b42-513a-45de-894a-72e56c706a58">CreateThread</a> and 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a> functions has <b>THREAD_TERMINATE</b> access, so any caller holding one of these handles can terminate your thread.

If the target thread is the last thread of a process when this function is called, the thread's process is also terminated.

The state of the thread object becomes signaled, releasing any other threads that had been waiting for the thread to terminate. The thread's termination status changes from <b>STILL_ACTIVE</b> to the value of the <i>dwExitCode</i> parameter.

Terminating a thread does not necessarily remove the thread object from the system. A thread object is deleted when the last thread handle is closed.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>



<a href="https://msdn.microsoft.com/202a4b42-513a-45de-894a-72e56c706a58">CreateThread</a>



<a href="https://msdn.microsoft.com/e7f6d054-c535-4521-a3b4-800a9174732f">ExitThread</a>



<a href="https://msdn.microsoft.com/67482c3d-b845-4c0f-8aa1-0e3cf8cb5127">GetExitCodeThread</a>



<a href="https://msdn.microsoft.com/d020ecc5-89d1-4a0d-a197-15a66e269e86">OpenThread</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/633e5d0c-e9d8-4f9a-9411-17cbe9e2e6e4">Terminating a Thread</a>



<a href="https://msdn.microsoft.com/a78c17dc-d5d9-4baf-8770-597b04fa3fa8">Threads</a>
 

 

