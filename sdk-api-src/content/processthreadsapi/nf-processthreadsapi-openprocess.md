---
UID: NF:processthreadsapi.OpenProcess
title: OpenProcess function
author: windows-sdk-content
description: Opens an existing local process object.
old-location: base\openprocess.htm
tech.root: ProcThread
ms.assetid: 8f695c38-19c4-49e4-97de-8b64ea536cb1
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: OpenProcess, OpenProcess function, _win32_openprocess, base.openprocess, processthreadsapi/OpenProcess, winbase/OpenProcess
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
---

# OpenProcess function


## -description


Opens an existing local process object.


## -parameters




### -param dwDesiredAccess [in]

The access to the process object. This access right is checked against the  security descriptor for the process. This parameter can be one or more of the 
<a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">process access rights</a>. 

If the caller has enabled the SeDebugPrivilege privilege, the requested access is  granted regardless of the contents of the security descriptor.


### -param bInheritHandle [in]

If this value is TRUE, processes created by this process will inherit the handle. Otherwise, the processes do not inherit this handle.


### -param dwProcessId [in]

The identifier of the local process to be opened. 

If the specified process is the System Process (0x00000000), the function fails and the last error code is ERROR_INVALID_PARAMETER. If the specified process is the Idle process or one of the CSRSS processes, this function fails and the last error code is ERROR_ACCESS_DENIED because their access restrictions prevent user-level code from opening them.

If you are using <a href="https://msdn.microsoft.com/a442e147-0db0-4911-94de-91728a4b277a">GetCurrentProcessId</a> as an argument to this function, consider using <a href="https://msdn.microsoft.com/0471790c-3bb9-4180-8676-941e655b1812">GetCurrentProcess</a> instead of OpenProcess, for improved performance.



## -returns



If the function succeeds, the return value is an open handle to the specified process.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To open a handle to another local process and obtain full access rights, you must enable the SeDebugPrivilege privilege. For more information, see <a href="https://msdn.microsoft.com/b8e47d04-07c1-4d57-8209-6b0c397476e5">Changing Privileges in a Token</a>.

The handle returned by the 
<b>OpenProcess</b> function can be used in any function that requires a handle to a process, such as the 
<a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">wait functions</a>, provided the appropriate access rights were requested.

When you are finished with the handle, be sure to close it using the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/318d166f-858f-4f33-9422-977e0c4beb3f">Taking a Snapshot and Viewing Processes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/f5d7a39f-6afe-4e4a-a802-e7f875ea6e5b">AssignProcessToJobObject</a>



<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>



<a href="https://msdn.microsoft.com/f5257f78-b20f-4db5-b63e-3bb4e41a4b19">CreateRemoteThread</a>



<a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a>



<a href="https://msdn.microsoft.com/0471790c-3bb9-4180-8676-941e655b1812">GetCurrentProcess</a>



<a href="https://msdn.microsoft.com/a442e147-0db0-4911-94de-91728a4b277a">GetCurrentProcessId</a>



<a href="https://msdn.microsoft.com/210f7595-ac12-4bb2-bd77-819649ebec10">GetExitCodeProcess</a>



<a href="https://msdn.microsoft.com/4199ce12-e82f-4a58-ac66-e0ddc0dffbff">GetModuleFileNameEx</a>



<a href="https://msdn.microsoft.com/2a16b18f-8efa-43f0-9f7d-d38cc8a153d3">GetPriorityClass</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/4bdec0f5-7276-422e-9935-0e231b0fc17d">Processes</a>



<a href="https://msdn.microsoft.com/8774e145-ee7f-44de-85db-0445b905f986">ReadProcessMemory</a>



<a href="https://msdn.microsoft.com/02686637-427a-4cf1-a4e5-60c707af3084">SetPriorityClass</a>



<a href="https://msdn.microsoft.com/8bc0053c-f687-43b5-a435-df1e813a5204">SetProcessWorkingSetSize</a>



<a href="https://msdn.microsoft.com/0e1a8195-4fd3-43d4-ae9e-1a1e05c2119a">TerminateProcess</a>



<a href="https://msdn.microsoft.com/6afd7ae6-e4c5-483c-a638-c85781674c7b">VirtualProtectEx</a>



<a href="https://msdn.microsoft.com/9cd91f1c-58ce-4adc-b027-45748543eb06">WriteProcessMemory</a>
 

 

