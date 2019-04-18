---
UID: NF:processthreadsapi.ExitThread
title: ExitThread function (processthreadsapi.h)
author: windows-sdk-content
description: Ends the calling thread.
old-location: base\exitthread.htm
tech.root: ProcThread
ms.assetid: e7f6d054-c535-4521-a3b4-800a9174732f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ExitThread, ExitThread function, _win32_exitthread, base.exitthread, processthreadsapi/ExitThread, winbase/ExitThread
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - KernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - ExitThread
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ExitThread function


## -description


Ends the calling thread.


## -parameters




### -param dwExitCode [in]

The exit code for the thread.


## -returns



This function does not return a value.




## -remarks



<b>ExitThread</b> is the preferred method of exiting a thread in C code. However, in C++ code, the thread is exited before any destructors can be called or any other automatic cleanup can be performed. Therefore, in C++ code, you should return from your thread function.

When this function is called (either explicitly or by returning from a thread procedure), the current thread's stack is deallocated, all pending I/O initiated by the thread is canceled, and the thread terminates. The entry-point function of all attached dynamic-link libraries (DLLs) is invoked with a value indicating that the thread is detaching from the DLL.

If the thread is the last thread in the process when this function is called, the thread's process is also terminated.

The state of the thread object becomes signaled, releasing any other threads that had been waiting for the thread to terminate. The thread's termination status changes from STILL_ACTIVE to the value of the <i>dwExitCode</i> parameter.

Terminating a thread does not necessarily remove the thread object from the operating system. A thread object is deleted when the last handle to the thread is closed.

The 
<a href="https://msdn.microsoft.com/c26dbf15-62e8-4892-b7c5-2e6c085e4cd5">ExitProcess</a>, 
<b>ExitThread</b>, 
<a href="https://msdn.microsoft.com/202a4b42-513a-45de-894a-72e56c706a58">CreateThread</a>, 
<a href="https://msdn.microsoft.com/f5257f78-b20f-4db5-b63e-3bb4e41a4b19">CreateRemoteThread</a> functions, and a process that is starting (as the result of a 
<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a> call) are serialized between each other within a process. Only one of these events can happen in an address space at a time. This means the following restrictions hold:

<ul>
<li>During process startup and DLL initialization routines, new threads can be created, but they do not begin execution until DLL initialization is done for the process.</li>
<li>Only one thread in a process can be in a DLL initialization or detach routine at a time.</li>
<li>
<a href="https://msdn.microsoft.com/c26dbf15-62e8-4892-b7c5-2e6c085e4cd5">ExitProcess</a> does not return until no threads are in their DLL initialization or detach routines.</li>
</ul>
A thread in an executable that is linked to the static C run-time library (CRT) should use <b>_beginthread</b> and <b>_endthread</b> for thread management rather than 
<b>CreateThread</b> and 
<b>ExitThread</b>. Failure to do so results in small memory leaks when 
the thread calls <b>ExitThread</b>. Another work around is to link the executable to the CRT in a DLL instead of the static CRT. Note that this memory leak only occurs from a DLL if the DLL is linked to the static CRT and a thread calls the <a href="https://msdn.microsoft.com/25e0e533-35e3-48c6-80a5-f063d38d87ca">DisableThreadLibraryCalls</a> function. Otherwise, it is safe to call <b>CreateThread</b> and 
<b>ExitThread</b> from a thread in a DLL that links to the static CRT.

Use the 
<a href="https://msdn.microsoft.com/67482c3d-b845-4c0f-8aa1-0e3cf8cb5127">GetExitCodeThread</a> function to retrieve a thread's exit code.

<b>Windows Phone 8.1:</b> This function is supported for Windows Phone Store apps on Windows Phone 8.1 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/f3f455bb-7563-4920-a728-f75fa5854dc9">Using Event Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>



<a href="https://msdn.microsoft.com/f5257f78-b20f-4db5-b63e-3bb4e41a4b19">CreateRemoteThread</a>



<a href="https://msdn.microsoft.com/202a4b42-513a-45de-894a-72e56c706a58">CreateThread</a>



<a href="https://msdn.microsoft.com/c26dbf15-62e8-4892-b7c5-2e6c085e4cd5">ExitProcess</a>



<a href="https://msdn.microsoft.com/be63fdbf-b3a4-44a8-99b4-b41e159952a7">FreeLibraryAndExitThread</a>



<a href="https://msdn.microsoft.com/67482c3d-b845-4c0f-8aa1-0e3cf8cb5127">GetExitCodeThread</a>



<a href="https://msdn.microsoft.com/d020ecc5-89d1-4a0d-a197-15a66e269e86">OpenThread</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/ae1ad0f3-67df-4573-af22-7086f0470361">TerminateThread</a>



<a href="https://msdn.microsoft.com/a78c17dc-d5d9-4baf-8770-597b04fa3fa8">Threads</a>
 

 

