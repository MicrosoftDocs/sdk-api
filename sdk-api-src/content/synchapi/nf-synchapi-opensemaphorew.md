---
UID: NF:synchapi.OpenSemaphoreW
title: OpenSemaphoreW function (synchapi.h)
description: Opens an existing named semaphore object.
helpviewer_keywords: ["OpenSemaphore","OpenSemaphore function","OpenSemaphoreA","OpenSemaphoreW","_win32_opensemaphore","base.opensemaphore","synchapi/OpenSemaphore","synchapi/OpenSemaphoreA","synchapi/OpenSemaphoreW"]
old-location: base\opensemaphore.htm
tech.root: base
ms.assetid: 2ea525b9-f33d-4b72-85e1-6d2cfdc64f5f
ms.date: 12/05/2018
ms.keywords: OpenSemaphore, OpenSemaphore function, OpenSemaphoreA, OpenSemaphoreW, _win32_opensemaphore, base.opensemaphore, synchapi/OpenSemaphore, synchapi/OpenSemaphoreA, synchapi/OpenSemaphoreW
req.header: synchapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OpenSemaphoreW (Unicode) and OpenSemaphoreA (ANSI)
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
 - OpenSemaphoreW
 - synchapi/OpenSemaphoreW
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
 - OpenSemaphore
 - OpenSemaphoreA
 - OpenSemaphoreW
---

# OpenSemaphoreW function


## -description

Opens an existing named semaphore object.

## -parameters

### -param dwDesiredAccess [in]

The access to the semaphore object. The function fails if the security descriptor of the specified object does not permit the requested access for the calling process. For a list of access rights, see 
<a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Synchronization Object Security and Access Rights</a>.

### -param bInheritHandle [in]

If this value is <b>TRUE</b>, processes created by this process will inherit the handle. Otherwise, the processes do not inherit this handle.

### -param lpName [in]

The name of the semaphore to be opened. Name comparisons are case sensitive. 




This function can open objects in a private namespace. For more information, see <a href="/windows/desktop/Sync/object-namespaces">Object Namespaces</a>.

<b>Terminal Services:  </b>The name can have a "Global\" or "Local\" prefix to explicitly open an object in the global or session namespace. The remainder of the name can contain any character except the backslash character (\\). For more information, see 
<a href="/windows/desktop/TermServ/kernel-object-namespaces">Kernel Object Namespaces</a>.

<b>Note</b>  Fast user switching is implemented using Terminal Services sessions. The first user to log on uses session 0, the next user to log on uses session 1, and so on. Kernel object names must follow the guidelines outlined for Terminal Services so that applications can support multiple users.

## -returns

If the function succeeds, the return value is a handle to the semaphore object.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>OpenSemaphore</b> function enables multiple processes to open handles of the same semaphore object. The function succeeds only if some process has already created the semaphore by using the 
<a href="/windows/desktop/api/winbase/nf-winbase-createsemaphorea">CreateSemaphore</a> function. The calling process can use the returned handle in any function that requires a handle to a semaphore object, such as the 
<a href="/windows/desktop/Sync/wait-functions">wait functions</a>, subject to the limitations of the access specified in the <i>dwDesiredAccess</i> parameter.

The handle can be duplicated by using the <a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a> function. Use the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to close the handle. The system closes the handle automatically when the process terminates. The semaphore object is destroyed when its last handle has been closed.

## -see-also

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createsemaphorea">CreateSemaphore</a>



<a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a>



<a href="/windows/desktop/Sync/object-names">Object Names</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-releasesemaphore">ReleaseSemaphore</a>



<a href="/windows/desktop/Sync/semaphore-objects">Semaphore Objects</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>