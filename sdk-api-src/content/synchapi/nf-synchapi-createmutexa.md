---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CreateMutexA function


## -description


Creates or opens a named or unnamed mutex object.

To specify an access mask for the object, use the <a href="https://msdn.microsoft.com/c22ec98a-29c0-444e-afa4-fa2ad131a086">CreateMutexEx</a> function.


## -parameters




### -param lpMutexAttributes [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> structure. If this parameter is <b>NULL</b>, the handle cannot be inherited by child processes. 




The <b>lpSecurityDescriptor</b> member of the structure specifies a security descriptor for the new mutex. If <i>lpMutexAttributes</i> is <b>NULL</b>, the mutex gets a default security descriptor. The ACLs in the default security descriptor for a mutex come from the primary or impersonation token of the creator. For more information, see <a href="https://msdn.microsoft.com/92478298-617c-4672-a1cc-9a8e9af40327">Synchronization Object Security and Access Rights</a>.


### -param bInitialOwner [in]

If this value is <b>TRUE</b> and the caller created the mutex, the calling thread obtains initial ownership of the mutex object. Otherwise, the calling thread does not obtain ownership of the mutex. To determine if the caller created the mutex, see the Return Values section.


### -param lpName [in, optional]

The name of the mutex object. The name is limited to <b>MAX_PATH</b> characters. Name comparison is case sensitive. 




If <i>lpName</i> matches the name of an existing named mutex object, this function requests the <b>MUTEX_ALL_ACCESS</b> access right. In this case, the <i>bInitialOwner</i> parameter is ignored because it has already been set by the creating process. If the <i>lpMutexAttributes</i> parameter is not <b>NULL</b>, it determines whether the handle can be inherited, but its security-descriptor member is ignored.

If <i>lpName</i> is <b>NULL</b>, the mutex object is created without a name.

If <i>lpName</i> matches the name of an existing event, semaphore, waitable timer, job, or file-mapping object, the function fails and the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function returns <b>ERROR_INVALID_HANDLE</b>. This occurs because these objects share the same namespace.

The name can have a "Global\" or "Local\" prefix to explicitly create the object in the global or session namespace. The remainder of the name can contain any character except the backslash character (\). For more information, see 
<a href="https://msdn.microsoft.com/771e0bbf-bd73-4e87-aa1e-945c1287b517">Kernel Object Namespaces</a>. Fast user switching is implemented using Terminal Services sessions. Kernel object names must follow the guidelines outlined for Terminal Services so that applications can support multiple users.

The object can be created in a private namespace. For more information, see <a href="https://msdn.microsoft.com/6a84ec16-fa65-4cdd-861a-eccf5d0eee2b">Object Namespaces</a>.


## -returns



If the function succeeds, the return value is a handle to the newly created mutex object.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If the mutex is a named mutex and the object existed before this function call, the return value is a handle to the existing object, 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_ALREADY_EXISTS</b>, <i>bInitialOwner</i> is ignored, and the calling thread is not granted ownership. However, if the caller has limited access rights, the function will fail with <b>ERROR_ACCESS_DENIED</b> and the caller should use the <a href="https://msdn.microsoft.com/0ea363c2-1ff7-4bf5-9e94-f1f17b8c8a11">OpenMutex</a> function.




## -remarks



The handle returned by 
<b>CreateMutex</b> has the <b>MUTEX_ALL_ACCESS</b> access right; it can be used in any function that requires a handle to a mutex object, provided that the caller has been granted access. If a mutex is created from a service or a thread that is impersonating a different user, you can either apply a security descriptor to the mutex when you create it, or change the default security descriptor for the creating process by changing its  default DACL. For more information, see 
<a href="https://msdn.microsoft.com/92478298-617c-4672-a1cc-9a8e9af40327">Synchronization Object Security and Access Rights</a>.

If you are using a named mutex to limit your application to a single instance, a malicious user can create this mutex before you do and prevent your application from starting. To prevent this situation, create a randomly named mutex and store the name so that it can only be obtained by an authorized user. Alternatively, you can use a file for this purpose. To limit your application to one instance per user, create a locked file in the user's profile directory.

Any thread of the calling process can specify the mutex-object handle in a call to one of the 
<a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">wait functions</a>. The single-object wait functions return when the state of the specified object is signaled. The multiple-object wait functions can be instructed to return either when any one or when all of the specified objects are signaled. When a wait function returns, the waiting thread is released to continue its execution.

The state of a mutex object is signaled when it is not owned by any thread. The creating thread can use the <i>bInitialOwner</i> flag to request immediate ownership of the mutex. Otherwise, a thread must use one of the wait functions to request ownership. When the mutex's state is signaled, one waiting thread is granted ownership, the mutex's state changes to nonsignaled, and the wait function returns. Only one thread can own a mutex at any given time. The owning thread uses the 
<a href="https://msdn.microsoft.com/c3e4daa8-92de-455c-847c-ea59225b3aa2">ReleaseMutex</a> function to release its ownership.

The thread that owns a mutex can specify the same mutex in repeated wait function calls without blocking its execution. Typically, you would not wait repeatedly for the same mutex, but this mechanism prevents a thread from deadlocking itself while waiting for a mutex that it already owns. However, to release its ownership, the thread must call 
<a href="https://msdn.microsoft.com/c3e4daa8-92de-455c-847c-ea59225b3aa2">ReleaseMutex</a> once for each time that the mutex satisfied a wait.

Two or more processes can call 
<b>CreateMutex</b> to create the same named mutex. The first process actually creates the mutex, and subsequent processes with sufficient access rights simply open a handle to the existing mutex. This enables multiple processes to get handles of the same mutex, while relieving the user of the responsibility of ensuring that the creating process is started first. When using this technique, you should set the <i>bInitialOwner</i> flag to <b>FALSE</b>; otherwise, it can be difficult to be certain which process has initial ownership.

Multiple processes can have handles of the same mutex object, enabling use of the object for interprocess synchronization. The following object-sharing mechanisms are available:

<ul>
<li>A child process created by the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a> function can inherit a handle to a mutex object if the <i>lpMutexAttributes</i> parameter of 
<b>CreateMutex</b> enabled inheritance. This mechanism works for both named and unnamed mutexes.</li>
<li>A process can specify the handle to a mutex object in a call to the <a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a> function to create a duplicate handle that can be used by another process. This mechanism works for both named and unnamed mutexes.</li>
<li>A process can specify a named mutex in a call to the 
<a href="https://msdn.microsoft.com/0ea363c2-1ff7-4bf5-9e94-f1f17b8c8a11">OpenMutex</a> or 
<b>CreateMutex</b> function to retrieve a handle to the mutex object.</li>
</ul>
Use the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function to close the handle. The system closes the handle automatically when the process terminates. The mutex object is destroyed when its last handle has been closed.


#### Examples

For an example that uses 
<b>CreateMutex</b>, see 
<a href="https://msdn.microsoft.com/0f69ba50-69ce-467a-b068-8fd8f07c6c78">Using Mutex Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/c22ec98a-29c0-444e-afa4-fa2ad131a086">CreateMutexEx</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>



<a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556417">Mutex Objects</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff557762">Object Names</a>



<a href="https://msdn.microsoft.com/0ea363c2-1ff7-4bf5-9e94-f1f17b8c8a11">OpenMutex</a>



<a href="https://msdn.microsoft.com/c3e4daa8-92de-455c-847c-ea59225b3aa2">ReleaseMutex</a>



<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

