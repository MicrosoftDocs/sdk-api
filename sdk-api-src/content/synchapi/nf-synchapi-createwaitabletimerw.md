---
UID: NF:synchapi.CreateWaitableTimerW
title: CreateWaitableTimerW function (synchapi.h)
description: Creates or opens a waitable timer object.
helpviewer_keywords: ["CreateWaitableTimer","CreateWaitableTimer function","CreateWaitableTimerA","CreateWaitableTimerW","_win32_createwaitabletimer","base.createwaitabletimer","synchapi/CreateWaitableTimer","synchapi/CreateWaitableTimerA","synchapi/CreateWaitableTimerW"]
old-location: base\createwaitabletimer.htm
tech.root: base
ms.assetid: 41c915c4-424d-43dd-89d9-a6b4fbee701c
ms.date: 12/05/2018
ms.keywords: CreateWaitableTimer, CreateWaitableTimer function, CreateWaitableTimerA, CreateWaitableTimerW, _win32_createwaitabletimer, base.createwaitabletimer, synchapi/CreateWaitableTimer, synchapi/CreateWaitableTimerA, synchapi/CreateWaitableTimerW
req.header: synchapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateWaitableTimerW (Unicode) and CreateWaitableTimerA (ANSI)
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
 - CreateWaitableTimerW
 - synchapi/CreateWaitableTimerW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Synch-Ansi-L1-1-0.dll
 - API-MS-Win-Core-Synch-L1-2-1.dll
 - Kernel32Legacy.dll
 - KernelBase.dll
api_name:
 - CreateWaitableTimer
 - CreateWaitableTimerA
 - CreateWaitableTimerW
---

# CreateWaitableTimerW function


## -description

Creates or opens a waitable timer object.

To specify an access mask for the object, use the [CreateWaitableTimerEx](./nf-synchapi-createwaitabletimerexw.md) function.

## -parameters

### -param lpTimerAttributes [in, optional]

A pointer to a 
<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure that specifies a security descriptor for the new timer object and determines whether child processes can inherit the returned handle. 

If <i>lpTimerAttributes</i> is <b>NULL</b>, the timer object gets a default security descriptor and the handle cannot be inherited. The ACLs in the default security descriptor for a timer come from the primary or impersonation token of the creator.

### -param bManualReset [in]

If this parameter is <b>TRUE</b>, the timer is a manual-reset notification timer. Otherwise, the timer is a synchronization timer.

### -param lpTimerName [in, optional]

The name of the timer object. The name is limited to <b>MAX_PATH</b> characters. Name comparison is case sensitive. 




If <i>lpTimerName</i> is <b>NULL</b>, the timer object is created without a name.

If <i>lpTimerName</i> matches the name of an existing event, semaphore, mutex, job, or file-mapping object, the function fails and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_INVALID_HANDLE</b>. This occurs because these objects share the same namespace.

The name can have a "Global\" or "Local\" prefix to explicitly create the object in the global or session namespace. The remainder of the name can contain any character except the backslash character (\\). For more information, see 
<a href="/windows/desktop/TermServ/kernel-object-namespaces">Kernel Object Namespaces</a>. Fast user switching is implemented using Terminal Services sessions. Kernel object names must follow the guidelines outlined for Terminal Services so that applications can support multiple users.

The object can be created in a private namespace. For more information, see <a href="/windows/desktop/Sync/object-namespaces">Object Namespaces</a>.

## -returns

If the function succeeds, the return value is a handle to the timer object. If the named timer object exists before the function call, the function returns a handle to the existing object and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_ALREADY_EXISTS</b>.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The handle returned by 
<b>CreateWaitableTimer</b> is created with the <b>TIMER_ALL_ACCESS</b> access right; it can be used in any function that requires a handle to a timer object, provided that the caller has been granted access. If a timer is created from a service or thread that is impersonating a different user, you can either apply a security descriptor to the timer when you create it, or change the default security descriptor for the creating process by changing its default DACL. For more information, see 
<a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Synchronization Object Security and Access Rights</a>.

Any thread of the calling process can specify the timer object handle in a call to one of the 
<a href="/windows/desktop/Sync/wait-functions">wait functions</a>.

Multiple processes can have handles to the same timer object, enabling use of the object for interprocess synchronization.

<ul>
<li>A process created by the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> function can inherit a handle to a timer object if the <i>lpTimerAttributes</i> parameter of 
<b>CreateWaitableTimer</b> enables inheritance.</li>
<li>A process can specify the timer object handle in a call to the <a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a> function. The resulting handle can be used by another process.</li>
<li>A process can specify the name of a timer object in a call to the <a href="/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw">OpenWaitableTimer</a> or <b>CreateWaitableTimer</b> function.</li>
</ul>
Use the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to close the handle. The system closes the handle automatically when the process terminates. The timer object is destroyed when its last handle has been closed.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0400 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

To associate a timer with a window, use the <a href="/windows/desktop/api/winuser/nf-winuser-settimer">SetTimer</a> function.


#### Examples

For an example that uses 
<b>CreateWaitableTimer</b>, see 
<a href="/windows/desktop/Sync/using-waitable-timer-objects">Using Waitable Timer Objects</a>.


<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/synchapi/nf-synchapi-cancelwaitabletimer">CancelWaitableTimer</a>



<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



[CreateWaitableTimerEx](./nf-synchapi-createwaitabletimerexw.md)



<a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="/windows/desktop/Sync/object-names">Object Names</a>



[OpenWaitableTimer](./nf-synchapi-openwaitabletimerw.md)



<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-setwaitabletimer">SetWaitableTimer</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>



<a href="/windows/desktop/Sync/waitable-timer-objects">Waitable Timer Objects</a>