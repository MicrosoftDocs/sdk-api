---
UID: NF:synchapi.CreateSemaphoreExW
title: CreateSemaphoreExW function (synchapi.h)
description: Creates or opens a named or unnamed semaphore object and returns a handle to the object. (CreateSemaphoreExW)
helpviewer_keywords: ["CreateSemaphoreExA","CreateSemaphoreExW","CreateSemaphoreExW function","base.createsemaphoreex","synchapi/CreateSemaphoreExA","synchapi/CreateSemaphoreExW"]
old-location: base\createsemaphoreex.htm
tech.root: base
ms.assetid: 741461e2-b672-4318-b39b-c6301ef9ab80
ms.date: 12/05/2018
ms.keywords: CreateSemaphoreExA, CreateSemaphoreExW, CreateSemaphoreExW function, base.createsemaphoreex, synchapi/CreateSemaphoreExA, synchapi/CreateSemaphoreExW
req.header: synchapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateSemaphoreExW (Unicode) and CreateSemaphoreExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateSemaphoreExW
 - synchapi/CreateSemaphoreExW
dev_langs:
 - c++
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
 - API-MS-Win-Core-Synch-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - CreateSemaphoreExW
 - CreateSemaphoreExA
 - CreateSemaphoreExW
---

# CreateSemaphoreExW function


## -description

Creates or opens a named or unnamed semaphore object and returns a handle to the object.

## -parameters

### -param lpSemaphoreAttributes [in, optional]

A pointer to a 
<a href="/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)">SECURITY_ATTRIBUTES</a> structure. If this parameter is <b>NULL</b>, the semaphore handle cannot be inherited by child processes. 




The <b>lpSecurityDescriptor</b> member of the structure specifies a security descriptor for the new semaphore. If this parameter is <b>NULL</b>, the semaphore gets a default security descriptor. The ACLs in the default security descriptor for a semaphore come from the primary or impersonation token of the creator.

### -param lInitialCount [in]

The initial count for the semaphore object. This value must be greater than or equal to zero and less than or equal to <i>lMaximumCount</i>. The state of a semaphore is signaled when its count is greater than zero and nonsignaled when it is zero. The count is decreased by one whenever a wait function releases a thread that was waiting for the semaphore. The count is increased by a specified amount by calling the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-releasesemaphore">ReleaseSemaphore</a> function.

### -param lMaximumCount [in]

The maximum count for the semaphore object. This value must be greater than zero.

### -param lpName [in, optional]

A pointer to a null-terminated string specifying the name of the semaphore object. The name is limited to <b>MAX_PATH</b> characters. Name comparison is case sensitive.

If <i>lpName</i> matches the name of an existing named semaphore object, the <i>lInitialCount</i> and <i>lMaximumCount</i> parameters are ignored because they have already been set by the creating process. If the <i>lpSemaphoreAttributes</i> parameter is not <b>NULL</b>, it determines whether the handle can be inherited.

If <i>lpName</i> is <b>NULL</b>, the semaphore object is created without a name.

If <i>lpName</i> matches the name of an existing event, mutex, waitable timer, job, or file-mapping object, the function fails and the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns <b>ERROR_INVALID_HANDLE</b>. This occurs because these objects share the same namespace.

The name can have a "Global\" or "Local\" prefix to explicitly create the object in the global or session namespace. The remainder of the name can contain any character except the backslash character (\\). For more information, see 
<a href="/windows/desktop/TermServ/kernel-object-namespaces">Kernel Object Namespaces</a>. Fast user switching is implemented using Terminal Services sessions. Kernel object names must follow the guidelines outlined for Terminal Services so that applications can support multiple users.

The object can be created in a private namespace. For more information, see <a href="/windows/desktop/Sync/object-namespaces">Object Namespaces</a>.

### -param dwFlags

This parameter is reserved and must be 0.

### -param dwDesiredAccess [in]

The access mask for the semaphore object. For a list of access rights, see 
<a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Synchronization Object Security and Access Rights</a>.

## -returns

If the function succeeds, the return value is a handle to the semaphore object. If the named semaphore object existed before the function call, the function returns a handle to the existing object and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_ALREADY_EXISTS</b>.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The state of a semaphore object is signaled when its count is greater than zero, and nonsignaled when its count is equal to zero. The <i>lInitialCount</i> parameter specifies the initial count. The count can never be less than zero or greater than the value specified in the <i>lMaximumCount</i> parameter.

Any thread of the calling process can specify the semaphore-object handle in a call to one of the 
<a href="/windows/desktop/Sync/wait-functions">wait functions</a>. The single-object wait functions return when the state of the specified object is signaled. The multiple-object wait functions can be instructed to return either when any one or when all of the specified objects are signaled. When a wait function returns, the waiting thread is released to continue its execution. Each time a thread completes a wait for a semaphore object, the count of the semaphore object is decremented by one. When the thread has finished, it calls the <a href="/windows/desktop/api/synchapi/nf-synchapi-releasesemaphore">ReleaseSemaphore</a> function, which increments the count of the semaphore object.

Multiple processes can have handles of the same semaphore object, enabling use of the object for interprocess synchronization. The following object-sharing mechanisms are available:

<ul>
<li>A child process created by the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> function can inherit a handle to a semaphore object if the <i>lpSemaphoreAttributes</i> parameter of 
<b>CreateSemaphoreEx</b> enabled inheritance.</li>
<li>A process can specify the semaphore-object handle in a call to the 
<a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a> function to create a duplicate handle that can be used by another process.</li>
<li>A process can specify the name of a semaphore object in a call to the 
<a href="/windows/win32/api/synchapi/nf-synchapi-opensemaphorew">OpenSemaphore</a> or 
<b>CreateSemaphoreEx</b> function.</li>
</ul>
Use the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to close the handle. The system closes the handle automatically when the process terminates. The semaphore object is destroyed when its last handle has been closed.

## -see-also

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/Sync/semaphore-objects">Semaphore Objects</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>
