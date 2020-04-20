---
UID: NF:processthreadsapi.GetCurrentProcess
title: GetCurrentProcess function (processthreadsapi.h)
description: Retrieves a pseudo handle for the current process.helpviewer_keywords: ["GetCurrentProcess","GetCurrentProcess function","_win32_getcurrentprocess","base.getcurrentprocess","processthreadsapi/GetCurrentProcess","winbase/GetCurrentProcess"]
old-location: base\getcurrentprocess.htm
tech.root: ProcThread
ms.assetid: 0471790c-3bb9-4180-8676-941e655b1812
ms.date: 12/05/2018
ms.keywords: GetCurrentProcess, GetCurrentProcess function, _win32_getcurrentprocess, base.getcurrentprocess, processthreadsapi/GetCurrentProcess, winbase/GetCurrentProcess
f1_keywords:
- processthreadsapi/GetCurrentProcess
dev_langs:
- c++
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
- GetCurrentProcess
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://docs.microsoft.com/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>This handle has the maximum access allowed by the security descriptor of the process to the primary token of the process.

A process can create a "real" handle to itself that is valid in the context of other processes, or that can be inherited by other processes, by specifying the pseudo handle as the source handle in a call to the <a href="https://docs.microsoft.com/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a> function. A process can also use the 
<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess">OpenProcess</a> function to open a real handle to itself.

The pseudo handle need not be closed when it is no longer needed. Calling the 
<a href="https://docs.microsoft.com/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function with a pseudo handle has no effect. If the pseudo handle is duplicated by 
<a href="https://docs.microsoft.com/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a>, the duplicate handle must be closed.


#### Examples

For an example, see 
<a href="https://docs.microsoft.com/windows/desktop/ProcThread/creating-a-child-process-with-redirected-input-and-output">Creating a Child Process with Redirected Input and Output</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="https://docs.microsoft.com/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid">GetCurrentProcessId</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentthread">GetCurrentThread</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess">OpenProcess</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/child-processes">Processes</a>
 

 

