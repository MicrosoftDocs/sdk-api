---
UID: NF:winbase.CreateSemaphoreA
title: CreateSemaphoreA function
author: windows-sdk-content
description: Creates or opens a named or unnamed semaphore object.
old-location: base\createsemaphorea.htm
tech.root: sync
ms.assetid: 829C8CC6-3E2C-480A-9F36-41EB93CA8536
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateSemaphoreA, CreateSemaphoreA function, CreateSemaphoreW, base.createsemaphorea, winbase/CreateSemaphoreA, winbase/CreateSemaphoreW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateSemaphoreW (Unicode) and CreateSemaphoreA (ANSI)
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
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-Synch-l1-2-1.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Synch-Ansi-L1-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - CreateSemaphoreA
 - CreateSemaphoreA
 - CreateSemaphoreW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateSemaphoreA function


## -description


Creates or opens a named or unnamed semaphore object.

To specify an access mask for the object, use the <a href="https://msdn.microsoft.com/741461e2-b672-4318-b39b-c6301ef9ab80">CreateSemaphoreEx</a> function.


## -parameters




### -param lpSemaphoreAttributes [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> 
       structure. If this parameter is <b>NULL</b>, the handle cannot be inherited by child 
       processes.

The <b>lpSecurityDescriptor</b> member of the structure specifies a security descriptor 
       for the new semaphore. If this parameter is <b>NULL</b>, the semaphore gets a default security descriptor. The ACLs in the default security descriptor for a semaphore come from the primary or impersonation token of the creator.


### -param lInitialCount [in]

The initial count for the semaphore object. This value must be greater than or equal to zero and less than or equal to <i>lMaximumCount</i>. The state of a semaphore is signaled when its count is greater than zero and nonsignaled when it is zero. The count is decreased by one whenever a wait function releases a thread that was waiting for the semaphore. The count is increased by a specified amount by calling the 
<a href="https://msdn.microsoft.com/9d444318-4d66-4ec3-a65d-bd3b75db9d9b">ReleaseSemaphore</a> function.


### -param lMaximumCount [in]

The maximum count for the semaphore object. This value must be greater than zero.


### -param lpName [in, optional]

The name of the semaphore object. The name is limited to <b>MAX_PATH</b> characters. Name comparison is case sensitive.

If <i>lpName</i> matches the name of an existing named semaphore object, this function requests the <b>SEMAPHORE_ALL_ACCESS</b> access right. In this case, the <i>lInitialCount</i> and <i>lMaximumCount</i> parameters are ignored because they have already been set by the creating process. If the <i>lpSemaphoreAttributes</i> parameter is not <b>NULL</b>, it determines whether the handle can be inherited, but its security-descriptor member is ignored.

If <i>lpName</i> is <b>NULL</b>, the semaphore object is created without a name.

If <i>lpName</i> matches the name of an existing event, mutex, waitable timer, job, or file-mapping object, the function fails and the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function returns <b>ERROR_INVALID_HANDLE</b>. This occurs because these objects share the same namespace.

The name can have a "Global\" or "Local\" prefix to explicitly create the object in the global or session namespace. The remainder of the name can contain any character except the backslash character (\). For more information, see 
<a href="https://msdn.microsoft.com/771e0bbf-bd73-4e87-aa1e-945c1287b517">Kernel Object Namespaces</a>. Fast user switching is implemented using Terminal Services sessions. Kernel object names must follow the guidelines outlined for Terminal Services so that applications can support multiple users.

The object can be created in a private namespace. For more information, see <a href="https://msdn.microsoft.com/6a84ec16-fa65-4cdd-861a-eccf5d0eee2b">Object Namespaces</a>.


## -returns



If the function succeeds, the return value is a handle to the semaphore object. If the named semaphore object existed before the function call, the function returns a handle to the existing object and 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_ALREADY_EXISTS</b>.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The handle returned by 
<a href="https://msdn.microsoft.com/2e55d67b-99de-4f10-8637-00d9d62e4460">CreateSemaphore</a> has the <b>SEMAPHORE_ALL_ACCESS</b> access right; it can be used in any function that requires a handle to a semaphore object, provided that the caller has been granted access. If an semaphore is created from a service or a thread that is impersonating a different user, you can either apply a security descriptor to the semaphore when you create it, or change the default security descriptor for the creating process by changing its default DACL. For more information, see 
<a href="https://msdn.microsoft.com/92478298-617c-4672-a1cc-9a8e9af40327">Synchronization Object Security and Access Rights</a>.

The state of a semaphore object is signaled when its count is greater than zero, and nonsignaled when its count is equal to zero. The <i>lInitialCount</i> parameter specifies the initial count. The count can never be less than zero or greater than the value specified in the <i>lMaximumCount</i> parameter.

Any thread of the calling process can specify the semaphore-object handle in a call to one of the 
<a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">wait functions</a>. The single-object wait functions return when the state of the specified object is signaled. The multiple-object wait functions can be instructed to return either when any one or when all of the specified objects are signaled. When a wait function returns, the waiting thread is released to continue its execution. Each time a thread completes a wait for a semaphore object, the count of the semaphore object is decremented by one. When the thread has finished, it calls the <a href="https://msdn.microsoft.com/9d444318-4d66-4ec3-a65d-bd3b75db9d9b">ReleaseSemaphore</a> function, which increments the count of the semaphore object.

Multiple processes can have handles of the same semaphore object, enabling use of the object for interprocess synchronization. The following object-sharing mechanisms are available:

<ul>
<li>A child process created by the 
<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a> function can inherit a handle to a semaphore object if the <i>lpSemaphoreAttributes</i> parameter of 
<a href="https://msdn.microsoft.com/2e55d67b-99de-4f10-8637-00d9d62e4460">CreateSemaphore</a> enabled inheritance.</li>
<li>A process can specify the semaphore-object handle in a call to the 
<a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a> function to create a duplicate handle that can be used by another process.</li>
<li>A process can specify the name of a semaphore object in a call to the 
<a href="https://msdn.microsoft.com/en-us/library/ms684326(v=VS.85).aspx">OpenSemaphore</a> or 
<a href="https://msdn.microsoft.com/2e55d67b-99de-4f10-8637-00d9d62e4460">CreateSemaphore</a> function.</li>
</ul>
Use the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function to close the handle. The system closes the handle automatically when the process terminates. The semaphore object is destroyed when its last handle has been closed.


#### Examples

For an example that uses 
<b>CreateSemaphore</b>, see 
<a href="https://msdn.microsoft.com/24a5c13c-573a-4fc2-ac19-98188c9eb68a">Using Semaphore Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>



<a href="https://msdn.microsoft.com/741461e2-b672-4318-b39b-c6301ef9ab80">CreateSemaphoreEx</a>



<a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a>



<a href="https://msdn.microsoft.com/00a00227-45fc-49a1-8ff5-aeccb172d16a">Object Names</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684326(v=VS.85).aspx">OpenSemaphore</a>



<a href="https://msdn.microsoft.com/9d444318-4d66-4ec3-a65d-bd3b75db9d9b">ReleaseSemaphore</a>



<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/d9da1d98-a306-4e2d-a149-1eef6a724751">Semaphore Objects</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

