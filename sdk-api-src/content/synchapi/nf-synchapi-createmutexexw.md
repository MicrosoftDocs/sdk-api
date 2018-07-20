---
UID: NF:synchapi.CreateMutexExW
title: CreateMutexExW function
author: windows-sdk-content
description: Creates or opens a named or unnamed mutex object and returns a handle to the object.
old-location: base\createmutexex.htm
old-project: sync
ms.assetid: c22ec98a-29c0-444e-afa4-fa2ad131a086
ms.author: windowssdkdev
ms.date: 07/06/2018
ms.keywords: CREATE_MUTEX_INITIAL_OWNER, CreateMutexEx, CreateMutexEx function, CreateMutexExA, CreateMutexExW, base.createmutexex, synchapi/CreateMutexEx, synchapi/CreateMutexExA, synchapi/CreateMutexExW, winbase/CreateMutexEx, winbase/CreateMutexExA, winbase/CreateMutexExW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: synchapi.h
req.include-header: Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateMutexExW (Unicode) and CreateMutexExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ITEMPROP, *LPITEMPROP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Synch-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Synch-l1-2-0.dll
 - API-MS-Win-Core-Synch-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - CreateMutexEx
 - CreateMutexExA
 - CreateMutexExW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# CreateMutexExW function


## -description


Creates or opens a named or unnamed mutex object and returns a handle to the object.


## -parameters




### -param lpMutexAttributes [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> structure. If this parameter is <b>NULL</b>, the mutex handle cannot be inherited by child processes. 




The <b>lpSecurityDescriptor</b> member of the structure specifies a security descriptor for the new mutex. If <i>lpMutexAttributes</i> is <b>NULL</b>, the mutex gets a default security descriptor. The ACLs in the default security descriptor for a mutex come from the primary or impersonation token of the creator. For more information, see <a href="https://msdn.microsoft.com/92478298-617c-4672-a1cc-9a8e9af40327">Synchronization Object Security and Access Rights</a>.


### -param lpName [in, optional]

The name of the mutex object. The name is limited to <b>MAX_PATH</b> characters. Name comparison is case sensitive. 



      

If <i>lpName</i> is <b>NULL</b>, the mutex object is created without a name.

If <i>lpName</i> matches the name of an existing event, semaphore, waitable timer, job, or file-mapping object, the function fails and the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function returns <b>ERROR_INVALID_HANDLE</b>. This occurs because these objects share the same namespace.

The name can have a "Global\" or "Local\" prefix to explicitly create the object in the global or session namespace. The remainder of the name can contain any character except the backslash character (\). For more information, see 
<a href="https://msdn.microsoft.com/771e0bbf-bd73-4e87-aa1e-945c1287b517">Kernel Object Namespaces</a>. Fast user switching is implemented using Terminal Services sessions. Kernel object names must follow the guidelines outlined for Terminal Services so that applications can support multiple users.

The object can be created in a private namespace. For more information, see <a href="https://msdn.microsoft.com/6a84ec16-fa65-4cdd-861a-eccf5d0eee2b">Object Namespaces</a>.


### -param dwFlags [in]

This parameter can be 0 or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CREATE_MUTEX_INITIAL_OWNER"></a><a id="create_mutex_initial_owner"></a><dl>
<dt><b>CREATE_MUTEX_INITIAL_OWNER</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The object creator is the initial owner of the mutex.

</td>
</tr>
</table>
 


### -param dwDesiredAccess [in]

The access mask for the mutex object. For a list of access rights, see 
<a href="https://msdn.microsoft.com/92478298-617c-4672-a1cc-9a8e9af40327">Synchronization Object Security and Access Rights</a>.


## -returns



If the function succeeds, the return value is a handle to the newly created mutex object.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If the mutex is a named mutex and the object existed before this function call, the return value is a handle to the existing object, 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_ALREADY_EXISTS</b>, <i>bInitialOwner</i> is ignored, and the calling thread is not granted ownership. However, if the caller has limited access rights, the function will fail with <b>ERROR_ACCESS_DENIED</b> and the caller should use the <a href="https://msdn.microsoft.com/0ea363c2-1ff7-4bf5-9e94-f1f17b8c8a11">OpenMutex</a> function.




## -remarks



If you are using a named mutex to limit your application to a single instance, a malicious user can create this mutex before you do and prevent your application from starting. To prevent this situation, create a randomly named mutex and store the name so that it can only be obtained by an authorized user. Alternatively, you can use a file for this purpose. To limit your application to one instance per user, create a locked file in the user's profile directory.

Any thread of the calling process can specify the mutex-object handle in a call to one of the 
<a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">wait functions</a>. The single-object wait functions return when the state of the specified object is signaled. The multiple-object wait functions can be instructed to return either when any one or when all of the specified objects are signaled. When a wait function returns, the waiting thread is released to continue its execution.

The state of a mutex object is signaled when it is not owned by any thread. The creating thread can use the <i>dwFlags</i> parameter to request immediate ownership of the mutex. Otherwise, a thread must use one of the wait functions to request ownership. When the mutex's state is signaled, one waiting thread is granted ownership, the mutex's state changes to nonsignaled, and the wait function returns. Only one thread can own a mutex at any given time. The owning thread uses the 
<a href="https://msdn.microsoft.com/c3e4daa8-92de-455c-847c-ea59225b3aa2">ReleaseMutex</a> function to release its ownership.

The thread that owns a mutex can specify the same mutex in repeated wait function calls without blocking its execution. Typically, you would not wait repeatedly for the same mutex, but this mechanism prevents a thread from deadlocking itself while waiting for a mutex that it already owns. However, to release its ownership, the thread must call 
<a href="https://msdn.microsoft.com/c3e4daa8-92de-455c-847c-ea59225b3aa2">ReleaseMutex</a> once for each time that the mutex satisfied a wait.

Two or more processes can call 
<a href="https://msdn.microsoft.com/c8315d1c-98c9-4f0a-ae0d-800d7d8100cd">CreateMutex</a> to create the same named mutex. The first process actually creates the mutex, and subsequent processes with sufficient access rights simply open a handle to the existing mutex. This enables multiple processes to get handles of the same mutex, while relieving the user of the responsibility of ensuring that the creating process is started first. When using this technique, you should not use the <b>CREATE_MUTEX_INITIAL_OWNER</b> flag; otherwise, it can be difficult to be certain which process has initial ownership.

Multiple processes can have handles of the same mutex object, enabling use of the object for interprocess synchronization. The following object-sharing mechanisms are available:

<ul>
<li>A child process created by the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a> function can inherit a handle to a mutex object if the <i>lpMutexAttributes</i> parameter of 
<a href="https://msdn.microsoft.com/c8315d1c-98c9-4f0a-ae0d-800d7d8100cd">CreateMutex</a> enabled inheritance. This mechanism works for both named and unnamed mutexes.</li>
<li>A process can specify the handle to a mutex object in a call to the <a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a> function to create a duplicate handle that can be used by another process. This mechanism works for both named and unnamed mutexes.</li>
<li>A process can specify a named mutex in a call to the 
<a href="https://msdn.microsoft.com/0ea363c2-1ff7-4bf5-9e94-f1f17b8c8a11">OpenMutex</a> or 
<a href="https://msdn.microsoft.com/c8315d1c-98c9-4f0a-ae0d-800d7d8100cd">CreateMutex</a> function to retrieve a handle to the mutex object.</li>
</ul>
Use the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function to close the handle. The system closes the handle automatically when the process terminates. The mutex object is destroyed when its last handle has been closed.




## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556417">Mutex Objects</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

