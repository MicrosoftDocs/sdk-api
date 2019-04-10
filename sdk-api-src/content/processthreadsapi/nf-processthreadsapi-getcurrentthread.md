---
UID: NF:processthreadsapi.GetCurrentThread
title: GetCurrentThread function (processthreadsapi.h)
author: windows-sdk-content
description: Retrieves a pseudo handle for the calling thread.
old-location: base\getcurrentthread.htm
tech.root: ProcThread
ms.assetid: 91a11552-66c1-42bd-b837-8a7685977bc9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCurrentThread, GetCurrentThread function, _win32_getcurrentthread, base.getcurrentthread, processthreadsapi/GetCurrentThread, winbase/GetCurrentThread
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
 - GetCurrentThread
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetCurrentThread function


## -description


Retrieves a pseudo handle for the calling thread.


## -parameters






## -returns



The return value is a pseudo handle for the current thread.




## -remarks



A pseudo handle is a special constant that is interpreted as the current thread handle. The calling thread can use this handle to specify itself whenever a thread handle is required. Pseudo handles are not inherited by child processes.

This handle has the <b>THREAD_ALL_ACCESS</b> access right to the thread object. For more information, see 
<a href="https://msdn.microsoft.com/72709446-5c59-4fac-8dc8-7912906ecc85">Thread Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>This handle has the maximum access allowed by the security descriptor of the thread to the primary token of the process.

The function cannot be used by one thread to create a handle that can be used by other threads to refer to the first thread. The handle is always interpreted as referring to the thread that is using it. A thread can create a "real" handle to itself that can be used by other threads, or inherited by other processes, by specifying the pseudo handle as the source handle in a call to the <a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a> function.

The pseudo handle need not be closed when it is no longer needed. Calling the 
<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function with this handle has no effect. If the pseudo handle is duplicated by 
<a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a>, the duplicate handle must be closed.

Do not create a thread while impersonating a security context. The call will succeed, however the newly created thread will have reduced access rights to itself when calling <b>GetCurrentThread</b>. The access rights granted this thread will  be derived from the access rights the impersonated user has to the process.  Some access rights including <b>THREAD_SET_THREAD_TOKEN</b> and <b>THREAD_GET_CONTEXT</b> may not be present, leading to unexpected failures.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/library/Aa379648(v=VS.85).aspx">Checking Client Access</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a>



<a href="https://msdn.microsoft.com/0471790c-3bb9-4180-8676-941e655b1812">GetCurrentProcess</a>



<a href="https://msdn.microsoft.com/a496f61a-e027-44e7-8b22-4f6651d7afb2">GetCurrentThreadId</a>



<a href="https://msdn.microsoft.com/d020ecc5-89d1-4a0d-a197-15a66e269e86">OpenThread</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/a78c17dc-d5d9-4baf-8770-597b04fa3fa8">Threads</a>
 

 

