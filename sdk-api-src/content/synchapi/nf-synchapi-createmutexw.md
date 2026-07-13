---
UID: NF:synchapi.CreateMutexW
title: CreateMutexW function (synchapi.h)
description: Creates or opens a named or unnamed mutex object. (Unicode)
helpviewer_keywords: ["CreateMutex", "CreateMutex function", "CreateMutexW", "_win32_createmutex", "base.createmutex", "synchapi/CreateMutex", "synchapi/CreateMutexW"]
old-location: base\createmutex.htm
tech.root: base
ms.assetid: c8315d1c-98c9-4f0a-ae0d-800d7d8100cd
ms.date: 12/05/2018
ms.keywords: CreateMutex, CreateMutex function, CreateMutexA, CreateMutexW, _win32_createmutex, base.createmutex, synchapi/CreateMutex, synchapi/CreateMutexA, synchapi/CreateMutexW, winbase/CreateMutex, winbase/CreateMutexA, winbase/CreateMutexW
req.header: synchapi.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateMutexW (Unicode) and CreateMutexA (ANSI)
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
 - CreateMutexW
 - synchapi/CreateMutexW
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
api_name:
 - CreateMutex
 - CreateMutexA
 - CreateMutexW
---

# CreateMutexW function


## -description

Creates or opens a named or unnamed mutex object.

To specify an access mask for the object, use the <a href="/windows/desktop/api/synchapi/nf-synchapi-createmutexexa">CreateMutexEx</a> function.

## -parameters

### -param lpMutexAttributes [in, optional]

A pointer to a 
<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure. If this parameter is <b>NULL</b>, the handle cannot be inherited by child processes. 




The <b>lpSecurityDescriptor</b> member of the structure specifies a security descriptor for the new mutex. If <i>lpMutexAttributes</i> is <b>NULL</b>, the mutex gets a default security descriptor. The ACLs in the default security descriptor for a mutex come from the primary or impersonation token of the creator. For more information, see <a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Synchronization Object Security and Access Rights</a>.

### -param bInitialOwner [in]

If this value is <b>TRUE</b> and the caller created the mutex, the calling thread obtains initial ownership of the mutex object. Otherwise, the calling thread does not obtain ownership of the mutex. To determine if the caller created the mutex, see the Return Values section.

### -param lpName [in, optional]

The name of the mutex object. The name is limited to <b>MAX_PATH</b> characters. Name comparison is case sensitive. 




If <i>lpName</i> matches the name of an existing named mutex object, this function requests the <b>MUTEX_ALL_ACCESS</b> access right. In this case, the <i>bInitialOwner</i> parameter is ignored because it has already been set by the creating process. If the <i>lpMutexAttributes</i> parameter is not <b>NULL</b>, it determines whether the handle can be inherited, but its security-descriptor member is ignored.

If <i>lpName</i> is <b>NULL</b>, the mutex object is created without a name.

If <i>lpName</i> matches the name of an existing event, semaphore, waitable timer, job, or file-mapping object, the function fails and the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns <b>ERROR_INVALID_HANDLE</b>. This occurs because these objects share the same namespace.

The name can have a "Global\" or "Local\" prefix to explicitly create the object in the global or session namespace. The remainder of the name can contain any character except the backslash character (\\). For more information, see 
<a href="/windows/desktop/TermServ/kernel-object-namespaces">Kernel Object Namespaces</a>. Fast user switching is implemented using Terminal Services sessions. Kernel object names must follow the guidelines outlined for Terminal Services so that applications can support multiple users.

The object can be created in a private namespace. For more information, see <a href="/windows/desktop/Sync/object-namespaces">Object Namespaces</a>.

## -returns

If the function succeeds, the return value is a handle to the newly created mutex object.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If the mutex is a named mutex and the object existed before this function call, the return value is a handle to the existing object, 
and the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns <b>ERROR_ALREADY_EXISTS</b>.

## -remarks

The handle returned by 
<b>CreateMutex</b> has the <b>MUTEX_ALL_ACCESS</b> access right; it can be used in any function that requires a handle to a mutex object, provided that the caller has been granted access. If a mutex is created from a service or a thread that is impersonating a different user, you can either apply a security descriptor to the mutex when you create it, or change the default security descriptor for the creating process by changing its  default DACL. For more information, see 
<a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Synchronization Object Security and Access Rights</a>.

If you are using a named mutex to limit your application to a single instance, a malicious user can create this mutex before you do and prevent your application from starting. To prevent this situation, create a randomly named mutex and store the name so that it can only be obtained by an authorized user. Alternatively, you can use a file for this purpose. To limit your application to one instance per user, create a locked file in the user's profile directory.

Any thread of the calling process can specify the mutex-object handle in a call to one of the 
<a href="/windows/desktop/Sync/wait-functions">wait functions</a>. The single-object wait functions return when the state of the specified object is signaled. The multiple-object wait functions can be instructed to return either when any one or when all of the specified objects are signaled. When a wait function returns, the waiting thread is released to continue its execution.

The state of a mutex object is signaled when it is not owned by any thread. The creating thread can use the <i>bInitialOwner</i> flag to request immediate ownership of the mutex. Otherwise, a thread must use one of the wait functions to request ownership. When the mutex's state is signaled, one waiting thread is granted ownership, the mutex's state changes to nonsignaled, and the wait function returns. Only one thread can own a mutex at any given time. The owning thread uses the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-releasemutex">ReleaseMutex</a> function to release its ownership.

The thread that owns a mutex can specify the same mutex in repeated wait function calls without blocking its execution. Typically, you would not wait repeatedly for the same mutex, but this mechanism prevents a thread from deadlocking itself while waiting for a mutex that it already owns. However, to release its ownership, the thread must call 
<a href="/windows/desktop/api/synchapi/nf-synchapi-releasemutex">ReleaseMutex</a> once for each time that the mutex satisfied a wait.

Two or more processes can call 
<b>CreateMutex</b> to create the same named mutex. The first process actually creates the mutex, and subsequent processes with sufficient access rights simply open a handle to the existing mutex. This enables multiple processes to get handles of the same mutex, while relieving the user of the responsibility of ensuring that the creating process is started first. When using this technique, you should set the <i>bInitialOwner</i> flag to <b>FALSE</b>; otherwise, it can be difficult to be certain which process has initial ownership.

Multiple processes can have handles of the same mutex object, enabling use of the object for interprocess synchronization. The following object-sharing mechanisms are available:

<ul>
<li>A child process created by the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> function can inherit a handle to a mutex object if the <i>lpMutexAttributes</i> parameter of 
<b>CreateMutex</b> enabled inheritance. This mechanism works for both named and unnamed mutexes.</li>
<li>A process can specify the handle to a mutex object in a call to the <a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a> function to create a duplicate handle that can be used by another process. This mechanism works for both named and unnamed mutexes.</li>
<li>A process can specify a named mutex in a call to the 
[OpenMutex](./nf-synchapi-openmutexw.md) or 
<b>CreateMutex</b> function to retrieve a handle to the mutex object.</li>
</ul>
Use the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to close the handle. The system closes the handle automatically when the process terminates. The mutex object is destroyed when its last handle has been closed.


#### Examples

For an example that uses 
<b>CreateMutex</b>, see 
<a href="/windows/desktop/Sync/using-mutex-objects">Using Mutex Objects</a>.

<div class="code"></div>




> [!NOTE]
> The synchapi.h header defines CreateMutex as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-createmutexexa">CreateMutexEx</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a>



<a href="/windows/desktop/Sync/mutex-objects">Mutex Objects</a>



<a href="/windows/desktop/Sync/object-names">Object Names</a>



[OpenMutex](./nf-synchapi-openmutexw.md)



<a href="/windows/desktop/api/synchapi/nf-synchapi-releasemutex">ReleaseMutex</a>



<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>
