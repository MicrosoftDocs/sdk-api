---
UID: NF:processthreadsapi.OpenThread
title: OpenThread function
author: windows-sdk-content
description: Opens an existing thread object.
old-location: base\openthread.htm
tech.root: ProcThread
ms.assetid: d020ecc5-89d1-4a0d-a197-15a66e269e86
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: OpenThread, OpenThread function, _win32_openthread, base.openthread, processthreadsapi/OpenThread, winbase/OpenThread
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
 - OpenThread
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- OpenThread
: 
---

# OpenThread function


## -description


Opens an existing thread object.


## -parameters




### -param dwDesiredAccess [in]

The access to the thread object. This access right is checked against the security descriptor for the thread. This parameter can be one or more of the 
<a href="https://msdn.microsoft.com/72709446-5c59-4fac-8dc8-7912906ecc85">thread access rights</a>.

If the caller has enabled the SeDebugPrivilege privilege, the requested access is  granted regardless of the contents of the security descriptor.


### -param bInheritHandle [in]

If this value is TRUE, processes created by this process will inherit the handle. Otherwise, the processes do not inherit this handle.


### -param dwThreadId [in]

The identifier of the thread to be opened.


## -returns



If the function succeeds, the return value is an open handle to the specified thread.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The handle returned by 
<b>OpenThread</b> can be used in any function that requires a handle to a thread, such as the 
<a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">wait functions</a>, provided you requested the appropriate access rights. The handle is granted access to the thread object only to the extent it was specified in the <i>dwDesiredAccess</i> parameter.

When you are finished with the handle, be sure to close it by using the 
<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function.




## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/67482c3d-b845-4c0f-8aa1-0e3cf8cb5127">GetExitCodeThread</a>



<a href="https://msdn.microsoft.com/3b65283e-34d2-4374-87fe-fa8ae45fbbcf">GetThreadContext</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/ffc4e474-635b-4bf7-a68f-073899fb3fde">ResumeThread</a>



<a href="https://msdn.microsoft.com/be134953-b569-48ea-80ac-ab14dee24500">SetThreadContext</a>



<a href="https://msdn.microsoft.com/cdb8af74-540d-4059-ac64-6243f6aabaa6">SetTokenInformation</a>



<a href="https://msdn.microsoft.com/1332abcb-3356-4890-a03c-843358c1a3ce">SuspendThread</a>



<a href="https://msdn.microsoft.com/ae1ad0f3-67df-4573-af22-7086f0470361">TerminateThread</a>



<a href="https://msdn.microsoft.com/a78c17dc-d5d9-4baf-8770-597b04fa3fa8">Threads</a>
 

 

