---
UID: NF:synchapi.CreateMutexExW
title: CreateMutexExW function (synchapi.h)
description: Creates or opens a named or unnamed mutex object and returns a handle to the object. (Unicode)
helpviewer_keywords: ["CREATE_MUTEX_INITIAL_OWNER", "CreateMutexEx", "CreateMutexEx function", "CreateMutexExW", "base.createmutexex", "synchapi/CreateMutexEx", "synchapi/CreateMutexExW"]
old-location: base\createmutexex.htm
tech.root: base
ms.assetid: c22ec98a-29c0-444e-afa4-fa2ad131a086
ms.date: 12/05/2018
ms.keywords: CREATE_MUTEX_INITIAL_OWNER, CreateMutexEx, CreateMutexEx function, CreateMutexExA, CreateMutexExW, base.createmutexex, synchapi/CreateMutexEx, synchapi/CreateMutexExA, synchapi/CreateMutexExW, winbase/CreateMutexEx, winbase/CreateMutexExA, winbase/CreateMutexExW
req.header: synchapi.h
req.include-header: Windows.h on Windows 7, Windows Server 2008  Windows Server 2008 R2
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateMutexExW
 - synchapi/CreateMutexExW
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
 - CreateMutexEx
 - CreateMutexExA
 - CreateMutexExW
---

# CreateMutexExW function


## -description

Creates or opens a named or unnamed mutex object and returns a handle to the object.

## -parameters

### -param lpMutexAttributes [in, optional]

A pointer to a 
<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure. If this parameter is <b>NULL</b>, the mutex handle cannot be inherited by child processes. 




The <b>lpSecurityDescriptor</b> member of the structure specifies a security descriptor for the new mutex. If <i>lpMutexAttributes</i> is <b>NULL</b>, the mutex gets a default security descriptor. The ACLs in the default security descriptor for a mutex come from the primary or impersonation token of the creator. For more information, see <a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Synchronization Object Security and Access Rights</a>.

### -param lpName [in, optional]

The name of the mutex object. The name is limited to <b>MAX_PATH</b> characters. Name comparison is case sensitive. 



      

If <i>lpName</i> is <b>NULL</b>, the mutex object is created without a name.

If <i>lpName</i> matches the name of an existing event, semaphore, waitable timer, job, or file-mapping object, the function fails and the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns <b>ERROR_INVALID_HANDLE</b>. This occurs because these objects share the same namespace.

The name can have a "Global\" or "Local\" prefix to explicitly create the object in the global or session namespace. The remainder of the name can contain any character except the backslash character (\\). For more information, see 
<a href="/windows/desktop/TermServ/kernel-object-namespaces">Kernel Object Namespaces</a>. Fast user switching is implemented using Terminal Services sessions. Kernel object names must follow the guidelines outlined for Terminal Services so that applications can support multiple users.

The object can be created in a private namespace. For more information, see <a href="/windows/desktop/Sync/object-namespaces">Object Namespaces</a>.

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
<a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Synchronization Object Security and Access Rights</a>.

## -returns

If the function succeeds, the return value is a handle to the newly created mutex object.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If the mutex is a named mutex and the object existed before this function call, the return value is a handle to the existing object, and the [GetLastError](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR_ALREADY_EXISTS**.

## -remarks

If you are using a named mutex to limit your application to a single instance, a malicious user can create this mutex before you do and prevent your application from starting. To prevent this situation, create a randomly named mutex and store the name so that it can only be obtained by an authorized user. Alternatively, you can use a file for this purpose. To limit your application to one instance per user, create a locked file in the user's profile directory.

Any thread of the calling process can specify the mutex-object handle in a call to one of the 
<a href="/windows/desktop/Sync/wait-functions">wait functions</a>. The single-object wait functions return when the state of the specified object is signaled. The multiple-object wait functions can be instructed to return either when any one or when all of the specified objects are signaled. When a wait function returns, the waiting thread is released to continue its execution.

The state of a mutex object is signaled when it is not owned by any thread. The creating thread can use the <i>dwFlags</i> parameter to request immediate ownership of the mutex. Otherwise, a thread must use one of the wait functions to request ownership. When the mutex's state is signaled, one waiting thread is granted ownership, the mutex's state changes to nonsignaled, and the wait function returns. Only one thread can own a mutex at any given time. The owning thread uses the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-releasemutex">ReleaseMutex</a> function to release its ownership.

The thread that owns a mutex can specify the same mutex in repeated wait function calls without blocking its execution. Typically, you would not wait repeatedly for the same mutex, but this mechanism prevents a thread from deadlocking itself while waiting for a mutex that it already owns. However, to release its ownership, the thread must call 
<a href="/windows/desktop/api/synchapi/nf-synchapi-releasemutex">ReleaseMutex</a> once for each time that the mutex satisfied a wait.

Two or more processes can call 
<a href="/windows/desktop/api/synchapi/nf-synchapi-createmutexa">CreateMutex</a> to create the same named mutex. The first process actually creates the mutex, and subsequent processes with sufficient access rights simply open a handle to the existing mutex. This enables multiple processes to get handles of the same mutex, while relieving the user of the responsibility of ensuring that the creating process is started first. When using this technique, you should not use the <b>CREATE_MUTEX_INITIAL_OWNER</b> flag; otherwise, it can be difficult to be certain which process has initial ownership.

Multiple processes can have handles of the same mutex object, enabling use of the object for interprocess synchronization. The following object-sharing mechanisms are available:

<ul>
<li>A child process created by the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> function can inherit a handle to a mutex object if the <i>lpMutexAttributes</i> parameter of 
<a href="/windows/desktop/api/synchapi/nf-synchapi-createmutexa">CreateMutex</a> enabled inheritance. This mechanism works for both named and unnamed mutexes.</li>
<li>A process can specify the handle to a mutex object in a call to the <a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a> function to create a duplicate handle that can be used by another process. This mechanism works for both named and unnamed mutexes.</li>
<li>A process can specify a named mutex in a call to the 
[OpenMutex](./nf-synchapi-openmutexw.md) or 
<a href="/windows/desktop/api/synchapi/nf-synchapi-createmutexa">CreateMutex</a> function to retrieve a handle to the mutex object.</li>
</ul>
Use the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to close the handle. The system closes the handle automatically when the process terminates. The mutex object is destroyed when its last handle has been closed.





> [!NOTE]
> The synchapi.h header defines CreateMutexEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/Sync/mutex-objects">Mutex Objects</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>
