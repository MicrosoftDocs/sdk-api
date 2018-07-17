---
UID: NF:processthreadsapi.GetCurrentProcess
title: GetCurrentProcess function
author: windows-sdk-content
description: Retrieves a pseudo handle for the current process.
old-location: base\getcurrentprocess.htm
old-project: procthread
ms.assetid: 0471790c-3bb9-4180-8676-941e655b1812
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetCurrentProcess, GetCurrentProcess function, _win32_getcurrentprocess, base.getcurrentprocess, processthreadsapi/GetCurrentProcess, winbase/GetCurrentProcess
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
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
 - GetCurrentProcess
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: ADAM
---

# GetCurrentProcess function


## -description


Retrieves a pseudo handle for the current process.


## -parameters






## -returns



The return value is a pseudo handle to the current process.




## -remarks



A pseudo handle is a special constant, currently (<b>HANDLE</b>)-1, that is interpreted as the current process handle. For compatibility with future operating systems, it is best to call 
<b>GetCurrentProcess</b> instead of hard-coding this constant value. The calling process can use a pseudo handle to specify its own process whenever a process handle is required. Pseudo handles are not inherited by child processes.

This handle has the <b>PROCESS_ALL_ACCESS</b> access right to the process object. For more information, see 
<a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>This handle has the maximum access allowed by the security descriptor of the process to the primary token of the process.

A process can create a "real" handle to itself that is valid in the context of other processes, or that can be inherited by other processes, by specifying the pseudo handle as the source handle in a call to the <a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a> function. A process can also use the 
<a href="https://msdn.microsoft.com/8f695c38-19c4-49e4-97de-8b64ea536cb1">OpenProcess</a> function to open a real handle to itself.

The pseudo handle need not be closed when it is no longer needed. Calling the 
<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function with a pseudo handle has no effect. If the pseudo handle is duplicated by 
<a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a>, the duplicate handle must be closed.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/a4e37069-2b3a-4b6d-9cfd-eb1700ab3bc6">Creating a Child Process with Redirected Input and Output</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff545836">GetCurrentProcessId</a>



<a href="https://msdn.microsoft.com/91a11552-66c1-42bd-b837-8a7685977bc9">GetCurrentThread</a>



<a href="https://msdn.microsoft.com/8f695c38-19c4-49e4-97de-8b64ea536cb1">OpenProcess</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/4bdec0f5-7276-422e-9935-0e231b0fc17d">Processes</a>
 

 

