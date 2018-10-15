---
UID: NF:processthreadsapi.GetExitCodeProcess
title: GetExitCodeProcess function
author: windows-sdk-content
description: Retrieves the termination status of the specified process.
old-location: base\getexitcodeprocess.htm
tech.root: ProcThread
ms.assetid: 210f7595-ac12-4bb2-bd77-819649ebec10
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetExitCodeProcess, GetExitCodeProcess function, _win32_getexitcodeprocess, base.getexitcodeprocess, processthreadsapi/GetExitCodeProcess, winbase/GetExitCodeProcess
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
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
 - GetExitCodeProcess
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetExitCodeProcess function


## -description


Retrieves the termination status of the specified process.


## -parameters




### -param hProcess [in]

A handle to the process.

The handle must have the <b>PROCESS_QUERY_INFORMATION</b> or <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the <b>PROCESS_QUERY_INFORMATION</b> access right.


### -param lpExitCode [out]

A pointer to a variable to receive the process termination status. For more information, see Remarks.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function returns immediately. If the process has not terminated and the function succeeds, the status returned is <b>STILL_ACTIVE</b>. If the process has terminated and the function succeeds, the status returned is one of the following values:

<ul>
<li>The exit value specified in the 
<a href="https://msdn.microsoft.com/c26dbf15-62e8-4892-b7c5-2e6c085e4cd5">ExitProcess</a> or 
<a href="https://msdn.microsoft.com/0e1a8195-4fd3-43d4-ae9e-1a1e05c2119a">TerminateProcess</a> function.</li>
<li>The return value from the <a href="http://go.microsoft.com/fwlink/p/?linkid=125835">main</a> or <a href="http://go.microsoft.com/fwlink/p/?linkid=125836">WinMain</a> function of the process.</li>
<li>The exception value for an unhandled exception that caused the process to terminate.</li>
</ul>
<div class="alert"><b>Important</b>  The <b>GetExitCodeProcess</b> function returns a valid error code defined by the application only after the thread terminates. Therefore, an application should not use <b>STILL_ACTIVE</b> (259) as an error code. If a thread returns <b>STILL_ACTIVE</b> (259) as an error code, applications that test for this value could interpret it to mean that the thread is still running and continue to test for the completion of the thread after the thread has terminated, which could put the application into an infinite loop.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c26dbf15-62e8-4892-b7c5-2e6c085e4cd5">ExitProcess</a>



<a href="https://msdn.microsoft.com/e7f6d054-c535-4521-a3b4-800a9174732f">ExitThread</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/4bdec0f5-7276-422e-9935-0e231b0fc17d">Processes</a>



<a href="https://msdn.microsoft.com/0e1a8195-4fd3-43d4-ae9e-1a1e05c2119a">TerminateProcess</a>



<a href="https://msdn.microsoft.com/af24d157-2719-4052-8029-1eb8010047cc">Terminating a Process</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=125836">WinMain</a>
 

 

