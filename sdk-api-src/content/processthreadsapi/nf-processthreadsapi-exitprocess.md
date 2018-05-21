---
UID: NF:processthreadsapi.ExitProcess
title: ExitProcess function
author: windows-driver-content
description: Ends the calling process and all its threads.
old-location: base\exitprocess.htm
old-project: ProcThread
ms.assetid: c26dbf15-62e8-4892-b7c5-2e6c085e4cd5
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: ExitProcess, ExitProcess function, _win32_exitprocess, base.exitprocess, processthreadsapi/ExitProcess, winbase/ExitProcess
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PSS_VA_SPACE_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-ProcessThreads-l1-1-0.dll
-	KernelBase.dll
-	MinKernelBase.dll
-	API-MS-Win-Core-ProcessThreads-l1-1-1.dll
-	API-MS-Win-Core-ProcessThreads-l1-1-2.dll
-	api-ms-win-downlevel-kernel32-l1-1-0.dll
-	API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
-	ExitProcess
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ExitProcess function


## -description


Ends the calling process and all its threads.


## -parameters




### -param uExitCode [in]

The exit code for the process and all threads.


## -returns



This function does not return a value.




## -remarks



Use the 
<a href="https://msdn.microsoft.com/210f7595-ac12-4bb2-bd77-819649ebec10">GetExitCodeProcess</a> function to retrieve the process's exit value. Use the 
<a href="https://msdn.microsoft.com/67482c3d-b845-4c0f-8aa1-0e3cf8cb5127">GetExitCodeThread</a> function to retrieve a thread's exit value.

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
<a href="https://msdn.microsoft.com/0e1a8195-4fd3-43d4-ae9e-1a1e05c2119a">TerminateProcess</a>, the DLLs that the process is attached to are not notified of the process termination. Therefore, if you do not know the state of all threads in your process, it is better to call <b>TerminateProcess</b> than  <b>ExitProcess</b>. Note that returning from the <b>main</b> function of an application results in a call to <b>ExitProcess</b>.

Calling 
<b>ExitProcess</b> in a DLL can lead to unexpected application or system errors. Be sure to call 
<b>ExitProcess</b> from a DLL only if you know which applications or system components will load the DLL and that it is safe to call 
<b>ExitProcess</b> in this context. 

Exiting a process does not cause child processes to be terminated.

Exiting a process does not necessarily remove the process object from the operating system. A process object is deleted when the last handle to the process is closed.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/a4e37069-2b3a-4b6d-9cfd-eb1700ab3bc6">Creating a Child Process with Redirected Input and Output</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>



<a href="https://msdn.microsoft.com/f5257f78-b20f-4db5-b63e-3bb4e41a4b19">CreateRemoteThread</a>



<a href="https://msdn.microsoft.com/202a4b42-513a-45de-894a-72e56c706a58">CreateThread</a>



<a href="https://msdn.microsoft.com/e7f6d054-c535-4521-a3b4-800a9174732f">ExitThread</a>



<a href="https://msdn.microsoft.com/210f7595-ac12-4bb2-bd77-819649ebec10">GetExitCodeProcess</a>



<a href="https://msdn.microsoft.com/67482c3d-b845-4c0f-8aa1-0e3cf8cb5127">GetExitCodeThread</a>



<a href="https://msdn.microsoft.com/8f695c38-19c4-49e4-97de-8b64ea536cb1">OpenProcess</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/4bdec0f5-7276-422e-9935-0e231b0fc17d">Processes</a>



<a href="https://msdn.microsoft.com/0e1a8195-4fd3-43d4-ae9e-1a1e05c2119a">TerminateProcess</a>



<a href="https://msdn.microsoft.com/af24d157-2719-4052-8029-1eb8010047cc">Terminating a Process</a>
 

 

