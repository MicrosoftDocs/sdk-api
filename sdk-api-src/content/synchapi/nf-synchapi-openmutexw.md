---
UID: NF:synchapi.OpenMutexW
title: OpenMutexW function (synchapi.h)
description: Opens an existing named mutex object.
helpviewer_keywords: ["OpenMutex","OpenMutex function","OpenMutexA","OpenMutexW","_win32_openmutex","base.openmutex","synchapi/OpenMutex","synchapi/OpenMutexA","synchapi/OpenMutexW"]
old-location: base\openmutex.htm
tech.root: base
ms.assetid: 0ea363c2-1ff7-4bf5-9e94-f1f17b8c8a11
ms.date: 12/05/2018
ms.keywords: OpenMutex, OpenMutex function, OpenMutexA, OpenMutexW, _win32_openmutex, base.openmutex, synchapi/OpenMutex, synchapi/OpenMutexA, synchapi/OpenMutexW
req.header: synchapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OpenMutexW (Unicode) and OpenMutexA (ANSI)
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
 - OpenMutexW
 - synchapi/OpenMutexW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Synch-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Synch-l1-2-0.dll
 - API-MS-Win-Core-Synch-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Synch-Ansi-L1-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - OpenMutex
 - OpenMutexA
 - OpenMutexW
---

# OpenMutexW function


## -description

Opens an existing named mutex object.

## -parameters

### -param dwDesiredAccess [in]

The access to the mutex object. Only the <b>SYNCHRONIZE</b> access right is required to use a mutex; to change the mutex's security, specify <b>MUTEX_ALL_ACCESS</b>. The function fails if the security descriptor of the specified object does not permit the requested access for the calling process. For a list of access rights, see 
<a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Synchronization Object Security and Access Rights</a>.

### -param bInheritHandle [in]

If this value is <b>TRUE</b>, processes created by this process will inherit the handle. Otherwise, the processes do not inherit this handle.

### -param lpName [in]

The name of the mutex to be opened. Name comparisons are case sensitive. 




This function can open objects in a private namespace. For more information, see <a href="/windows/desktop/Sync/object-namespaces">Object Namespaces</a>.

<b>Terminal Services:  </b>The name can have a "Global\" or "Local\" prefix to explicitly open an object in the global or session namespace. The remainder of the name can contain any character except the backslash character (\\). For more information, see 
<a href="/windows/desktop/TermServ/kernel-object-namespaces">Kernel Object Namespaces</a>.

<b>Note</b>  Fast user switching is implemented using Terminal Services sessions. The first user to log on uses session 0, the next user to log on uses session 1, and so on. Kernel object names must follow the guidelines outlined for Terminal Services so that applications can support multiple users.

## -returns

If the function succeeds, the return value is a handle to the mutex object.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If a named mutex does not exist, the function fails and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_FILE_NOT_FOUND</b>.

## -remarks

The 
<b>OpenMutex</b> function enables multiple processes to open handles of the same mutex object. The function succeeds only if some process has already created the mutex by using the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-createmutexa">CreateMutex</a> function. The calling process can use the returned handle in any function that requires a handle to a mutex object, such as the 
<a href="/windows/desktop/Sync/wait-functions">wait functions</a>, subject to the limitations of the access specified in the <i>dwDesiredAccess</i> parameter.

The handle can be duplicated by using the <a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a> function. Use the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to close the handle. The system closes the handle automatically when the process terminates. The mutex object is destroyed when its last handle has been closed.

If your multithreaded application must repeatedly create, open, and close a named mutex object, a race condition can occur. In this situation, it is better to use <a href="/windows/desktop/api/synchapi/nf-synchapi-createmutexa">CreateMutex</a> instead of <b>OpenMutex</b>, because <b>CreateMutex</b> opens a mutex if it exists and creates it if it does not.


#### Examples

For an example that uses 
<b>OpenMutex</b>, see 
<a href="/windows/desktop/Sync/using-named-objects">Using Named Objects</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-createmutexa">CreateMutex</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a>



<a href="/windows/desktop/Sync/mutex-objects">Mutex Objects</a>



<a href="/windows/desktop/Sync/object-names">Object Names</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-releasemutex">ReleaseMutex</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>