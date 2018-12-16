---
UID: NF:processthreadsapi.CreateThread
title: CreateThread function
author: windows-sdk-content
description: Creates a thread to execute within the virtual address space of the calling process.
old-location: base\createthread.htm
tech.root: procthread
ms.assetid: 202a4b42-513a-45de-894a-72e56c706a58
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CREATE_SUSPENDED, CreateThread, CreateThread function, STACK_SIZE_PARAM_IS_A_RESERVATION, _win32_createthread, base.createthread, processthreadsapi/CreateThread, winbase/CreateThread
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
req.lib: Kernel32.lib; WindowsPhoneCore.lib on Windows Phone 8.1
req.dll: Kernel32.dll; KernelBase.dll on Windows Phone 8.1
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - KernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - CreateThread
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateThread function


## -description


Creates a thread to execute within the virtual address space of the calling process.

To create a thread that runs in the virtual address space of another process, use the 
<a href="https://msdn.microsoft.com/f5257f78-b20f-4db5-b63e-3bb4e41a4b19">CreateRemoteThread</a> function.


## -parameters




### -param lpThreadAttributes [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> 
       structure that determines whether the returned handle can be inherited by child processes. If 
       <i>lpThreadAttributes</i> is NULL, the handle cannot be inherited.

The <b>lpSecurityDescriptor</b> member of the structure specifies a security descriptor for the new thread. If <i>lpThreadAttributes</i> is NULL, the thread gets a default security descriptor. The ACLs in the default security descriptor for a thread come from the primary token of the creator.


### -param dwStackSize [in]

The initial size of the stack, in bytes. The system rounds this value to the nearest page. If this parameter is zero, the new thread uses the default size for the executable. For more information, see 
<a href="https://msdn.microsoft.com/abb2d5c1-040b-4c36-aae5-3517b6a8c540">Thread Stack Size</a>.


### -param lpStartAddress [in]

A pointer to the application-defined function to be executed by the thread. This pointer represents the starting address of the thread. For more information on the thread function, see 
<a href="https://msdn.microsoft.com/f0dc203f-200e-42f1-940c-24e3fe080175">ThreadProc</a>.


### -param lpParameter [in, optional]

A pointer to a variable to be passed to the thread.


### -param dwCreationFlags [in]

The flags that control the creation of the thread.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The thread runs immediately after creation.

</td>
</tr>
<tr>
<td width="40%"><a id="CREATE_SUSPENDED"></a><a id="create_suspended"></a><dl>
<dt><b>CREATE_SUSPENDED</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The thread is created in a suspended state, and does not run until the 
<a href="https://msdn.microsoft.com/ffc4e474-635b-4bf7-a68f-073899fb3fde">ResumeThread</a> function is called.

</td>
</tr>
<tr>
<td width="40%"><a id="STACK_SIZE_PARAM_IS_A_RESERVATION"></a><a id="stack_size_param_is_a_reservation"></a><dl>
<dt><b>STACK_SIZE_PARAM_IS_A_RESERVATION</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
The <i>dwStackSize</i> parameter specifies the initial reserve size of the stack. If this flag is not specified, <i>dwStackSize</i> specifies the commit size.

</td>
</tr>
</table>
 


### -param lpThreadId [out, optional]

A pointer to a variable that receives the  thread identifier. If this parameter is 
      <b>NULL</b>, the thread identifier is not returned.
     


## -returns



If the function succeeds, the return value is a handle to the new thread.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

Note that <b>CreateThread</b> may succeed even if 
       <i>lpStartAddress</i> points to data, code, or is not accessible. If the start address is 
       invalid when the thread runs, an exception occurs, and the thread terminates. Thread termination due to a 
       invalid start address is handled as an error exit for the thread's process. This behavior is similar to the 
       asynchronous nature of <a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>, where the 
       process is created even if it refers to invalid or missing dynamic-link libraries (DLLs).




## -remarks



The number of threads a process can create is limited by the available virtual memory. By default, every thread has one megabyte of stack space. Therefore, you can create at most 2,048 threads. If you reduce the default stack size, you can create more threads. However, your application will have better performance if you create one thread per processor and build queues of requests for which the application maintains the context information. A thread would process all requests in a queue before processing requests in the next queue.

The new thread handle is created with the <b>THREAD_ALL_ACCESS</b> access right. If a security descriptor is not provided when the thread is created, a default security descriptor is constructed for the new thread using the primary token of the   process that is creating the thread. When a caller attempts to access the thread  with the <a href="https://msdn.microsoft.com/d020ecc5-89d1-4a0d-a197-15a66e269e86">OpenThread</a> function, the effective token of the caller is evaluated against this  security descriptor to grant or deny access. 

 The newly created thread  has full access rights to itself when calling the <a href="https://msdn.microsoft.com/91a11552-66c1-42bd-b837-8a7685977bc9">GetCurrentThread</a>  function. 

<b>Windows Server 2003:  </b>The thread's access rights to itself are computed by evaluating the primary token of the process in which the thread was created  against the default security descriptor constructed for the thread. If the thread is created in a remote process, the primary token of the remote process is used. As a result, the newly created thread may have reduced access rights to itself when calling <a href="https://msdn.microsoft.com/91a11552-66c1-42bd-b837-8a7685977bc9">GetCurrentThread</a>. Some access rights including <b>THREAD_SET_THREAD_TOKEN</b> and <b>THREAD_GET_CONTEXT</b> may not be present, leading to unexpected failures. For this reason, creating a thread while impersonating another user is not recommended.

 If the thread is created in a runnable state (that is, if the <b>CREATE_SUSPENDED</b> flag is not used), the thread can start running before <b>CreateThread</b> returns and, in particular, before  the caller receives the handle and identifier of the created thread.

The thread execution begins at the function specified by the <i>lpStartAddress</i> parameter. If this function returns, the <b>DWORD</b> return value is used to terminate the thread in an implicit call to the 
<a href="https://msdn.microsoft.com/e7f6d054-c535-4521-a3b4-800a9174732f">ExitThread</a> function. Use the 
<a href="https://msdn.microsoft.com/67482c3d-b845-4c0f-8aa1-0e3cf8cb5127">GetExitCodeThread</a> function to get the thread's return value.

The thread is created with a thread priority of <b>THREAD_PRIORITY_NORMAL</b>. Use the 
<a href="https://msdn.microsoft.com/9e5ce4e8-bdd1-48c3-aa1d-b24b2b7bfb00">GetThreadPriority</a> and 
<a href="https://msdn.microsoft.com/e3992e19-b546-4b0b-aa6a-dd9a7e330bf3">SetThreadPriority</a> functions to get and set the priority value of a thread.

When a thread terminates, the thread object attains a signaled state, satisfying any threads that were waiting on the object.

The thread object remains in the system until the thread has terminated and all handles to it have been closed through a call to 
<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>.

The 
<a href="https://msdn.microsoft.com/c26dbf15-62e8-4892-b7c5-2e6c085e4cd5">ExitProcess</a>, 
<a href="https://msdn.microsoft.com/e7f6d054-c535-4521-a3b4-800a9174732f">ExitThread</a>, 
<b>CreateThread</b>, 
<a href="https://msdn.microsoft.com/f5257f78-b20f-4db5-b63e-3bb4e41a4b19">CreateRemoteThread</a> functions, and a process that is starting (as the result of a call by 
<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>) are serialized between each other within a process. Only one of these events can happen in an address space at a time. This means that the following restrictions hold:

<ul>
<li>During process startup and DLL initialization routines, new threads can be created, but they do not begin execution until DLL initialization is done for the process.</li>
<li>Only one thread in a process can be in a DLL initialization or detach routine at a time.</li>
<li>
<a href="https://msdn.microsoft.com/c26dbf15-62e8-4892-b7c5-2e6c085e4cd5">ExitProcess</a> does not complete until there are no threads in their DLL initialization or detach routines.</li>
</ul>
A thread in an executable that calls the C run-time library (CRT) should use the <a href="http://go.microsoft.com/fwlink/p/?linkid=125829">_beginthreadex</a> and <a href="http://go.microsoft.com/fwlink/p/?linkid=125830">_endthreadex</a> functions for thread management rather than 
<b>CreateThread</b> and 
<a href="https://msdn.microsoft.com/e7f6d054-c535-4521-a3b4-800a9174732f">ExitThread</a>; this requires the use of the multithreaded version of the CRT. If a thread created using <b>CreateThread</b> calls the CRT, the CRT may terminate the process in low-memory conditions.

<b>Windows Phone 8.1:</b> This function is supported for Windows Phone Store apps on Windows Phone 8.1 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/eb0cc3c0-14f2-4913-a592-4ba3eaf67002">Creating Threads</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>



<a href="https://msdn.microsoft.com/f5257f78-b20f-4db5-b63e-3bb4e41a4b19">CreateRemoteThread</a>



<a href="https://msdn.microsoft.com/c26dbf15-62e8-4892-b7c5-2e6c085e4cd5">ExitProcess</a>



<a href="https://msdn.microsoft.com/e7f6d054-c535-4521-a3b4-800a9174732f">ExitThread</a>



<a href="https://msdn.microsoft.com/67482c3d-b845-4c0f-8aa1-0e3cf8cb5127">GetExitCodeThread</a>



<a href="https://msdn.microsoft.com/9e5ce4e8-bdd1-48c3-aa1d-b24b2b7bfb00">GetThreadPriority</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/ffc4e474-635b-4bf7-a68f-073899fb3fde">ResumeThread</a>



<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/e3992e19-b546-4b0b-aa6a-dd9a7e330bf3">SetThreadPriority</a>



<a href="https://msdn.microsoft.com/1332abcb-3356-4890-a03c-843358c1a3ce">SuspendThread</a>



<a href="https://msdn.microsoft.com/f0dc203f-200e-42f1-940c-24e3fe080175">ThreadProc</a>



<a href="https://msdn.microsoft.com/a78c17dc-d5d9-4baf-8770-597b04fa3fa8">Threads</a>
 

 

