---
UID: NF:processthreadsapi.OpenThread
title: OpenThread function (processthreadsapi.h)
author: windows-sdk-content
description: Opens an existing thread object.
old-location: base\openthread.htm
tech.root: ProcThread
ms.assetid: d020ecc5-89d1-4a0d-a197-15a66e269e86
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: OpenThread, OpenThread function, _win32_openthread, base.openthread, processthreadsapi/OpenThread, winbase/OpenThread
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
ms.custom: 19H1
---

# OpenThread function


## -description


Opens an existing thread object.


## -parameters




### -param dwDesiredAccess [in]

The access to the thread object. This access right is checked against the security descriptor for the thread. This parameter can be one or more of the 
<a href="https://docs.microsoft.com/windows/desktop/ProcThread/thread-security-and-access-rights">thread access rights</a>.

If the caller has enabled the SeDebugPrivilege privilege, the requested access is  granted regardless of the contents of the security descriptor.


### -param bInheritHandle [in]

If this value is TRUE, processes created by this process will inherit the handle. Otherwise, the processes do not inherit this handle.


### -param dwThreadId [in]

The identifier of the thread to be opened.


## -returns



If the function succeeds, the return value is an open handle to the specified thread.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The handle returned by 
<b>OpenThread</b> can be used in any function that requires a handle to a thread, such as the 
<a href="https://docs.microsoft.com/windows/desktop/Sync/wait-functions">wait functions</a>, provided you requested the appropriate access rights. The handle is granted access to the thread object only to the extent it was specified in the <i>dwDesiredAccess</i> parameter.

When you are finished with the handle, be sure to close it by using the 
<a href="https://docs.microsoft.com/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getexitcodethread">GetExitCodeThread</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getthreadcontext">GetThreadContext</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-resumethread">ResumeThread</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadcontext">SetThreadContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-settokeninformation">SetTokenInformation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-suspendthread">SuspendThread</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread">TerminateThread</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/multiple-threads">Threads</a>
 

 

