---
UID: NF:processthreadsapi.OpenProcess
title: OpenProcess function (processthreadsapi.h)
author: windows-sdk-content
description: Opens an existing local process object.
old-location: base\openprocess.htm
tech.root: ProcThread
ms.assetid: 8f695c38-19c4-49e4-97de-8b64ea536cb1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: OpenProcess, OpenProcess function, _win32_openprocess, base.openprocess, processthreadsapi/OpenProcess, winbase/OpenProcess
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
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-core-synch-l1-1-0.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - OpenProcess
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# OpenProcess function


## -description


Opens an existing local process object.


## -parameters




### -param dwDesiredAccess [in]

The access to the process object. This access right is checked against the  security descriptor for the process. This parameter can be one or more of the 
<a href="https://docs.microsoft.com/windows/desktop/ProcThread/process-security-and-access-rights">process access rights</a>. 

If the caller has enabled the SeDebugPrivilege privilege, the requested access is  granted regardless of the contents of the security descriptor.


### -param bInheritHandle [in]

If this value is TRUE, processes created by this process will inherit the handle. Otherwise, the processes do not inherit this handle.


### -param dwProcessId [in]

The identifier of the local process to be opened. 

If the specified process is the System Process (0x00000000), the function fails and the last error code is ERROR_INVALID_PARAMETER. If the specified process is the Idle process or one of the CSRSS processes, this function fails and the last error code is ERROR_ACCESS_DENIED because their access restrictions prevent user-level code from opening them.

If you are using <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid">GetCurrentProcessId</a> as an argument to this function, consider using <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess">GetCurrentProcess</a> instead of OpenProcess, for improved performance.



## -returns



If the function succeeds, the return value is an open handle to the specified process.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



To open a handle to another local process and obtain full access rights, you must enable the SeDebugPrivilege privilege. For more information, see <a href="https://docs.microsoft.com/windows/desktop/SecBP/changing-privileges-in-a-token">Changing Privileges in a Token</a>.

The handle returned by the 
<b>OpenProcess</b> function can be used in any function that requires a handle to a process, such as the 
<a href="https://docs.microsoft.com/windows/desktop/Sync/wait-functions">wait functions</a>, provided the appropriate access rights were requested.

When you are finished with the handle, be sure to close it using the <a href="https://docs.microsoft.com/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function.


#### Examples

For an example, see 
<a href="https://docs.microsoft.com/windows/desktop/ToolHelp/taking-a-snapshot-and-viewing-processes">Taking a Snapshot and Viewing Processes</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/jobapi2/nf-jobapi2-assignprocesstojobobject">AssignProcessToJobObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createremotethread">CreateRemoteThread</a>



<a href="https://docs.microsoft.com/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess">GetCurrentProcess</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid">GetCurrentProcessId</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess">GetExitCodeProcess</a>



<a href="https://docs.microsoft.com/windows/desktop/api/psapi/nf-psapi-getmodulefilenameexa">GetModuleFileNameEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getpriorityclass">GetPriorityClass</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/child-processes">Processes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/memoryapi/nf-memoryapi-readprocessmemory">ReadProcessMemory</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setpriorityclass">SetPriorityClass</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-setprocessworkingsetsize">SetProcessWorkingSetSize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess">TerminateProcess</a>



<a href="https://docs.microsoft.com/windows/desktop/api/memoryapi/nf-memoryapi-virtualprotectex">VirtualProtectEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/memoryapi/nf-memoryapi-writeprocessmemory">WriteProcessMemory</a>
 

 

