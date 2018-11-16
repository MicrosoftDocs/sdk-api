---
UID: NF:processthreadsapi.TerminateProcess
title: TerminateProcess function
author: windows-sdk-content
description: Terminates the specified process and all of its threads.
old-location: base\terminateprocess.htm
tech.root: ProcThread
ms.assetid: 0e1a8195-4fd3-43d4-ae9e-1a1e05c2119a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: TerminateProcess, TerminateProcess function, _win32_terminateprocess, base.terminateprocess, processthreadsapi/TerminateProcess, winbase/TerminateProcess
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
 - TerminateProcess
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- TerminateProcess
: 
---

# TerminateProcess function


## -description


Terminates the specified process and all of its threads.


## -parameters




### -param hProcess [in]

A handle to the process to be terminated.

The handle must have the <b>PROCESS_TERMINATE</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.


### -param uExitCode [in]

The exit code to be used by the process and threads terminated as a result of this call. Use the 
<a href="https://msdn.microsoft.com/210f7595-ac12-4bb2-bd77-819649ebec10">GetExitCodeProcess</a> function to retrieve a process's exit value. Use the 
<a href="https://msdn.microsoft.com/67482c3d-b845-4c0f-8aa1-0e3cf8cb5127">GetExitCodeThread</a> function to retrieve a thread's exit value.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>TerminateProcess</b> function is used to unconditionally cause a process to exit. The state of global data maintained by dynamic-link libraries (DLLs) may be compromised if 
<b>TerminateProcess</b> is used rather than 
<a href="https://msdn.microsoft.com/c26dbf15-62e8-4892-b7c5-2e6c085e4cd5">ExitProcess</a>.

This function stops execution of all threads within the process and requests cancellation of all pending I/O. The terminated process cannot exit until all pending I/O has been completed or canceled. When a process terminates, its kernel object is not destroyed until all processes that have open handles to the process have released those handles.

<b>TerminateProcess</b> is asynchronous; it initiates termination and returns immediately. If you need to be sure the process has terminated, call the <a href="https://msdn.microsoft.com/e37ebff7-b44e-469d-81ab-7a6bd1a0c822">WaitForSingleObject</a> function with a handle to the process.

A process cannot prevent itself from being terminated.




## -see-also




<a href="https://msdn.microsoft.com/c26dbf15-62e8-4892-b7c5-2e6c085e4cd5">ExitProcess</a>



<a href="https://msdn.microsoft.com/210f7595-ac12-4bb2-bd77-819649ebec10">GetExitCodeProcess</a>



<a href="https://msdn.microsoft.com/67482c3d-b845-4c0f-8aa1-0e3cf8cb5127">GetExitCodeThread</a>



<a href="https://msdn.microsoft.com/8f695c38-19c4-49e4-97de-8b64ea536cb1">OpenProcess</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/4bdec0f5-7276-422e-9935-0e231b0fc17d">Processes</a>



<a href="https://msdn.microsoft.com/af24d157-2719-4052-8029-1eb8010047cc">Terminating a Process</a>
 

 

