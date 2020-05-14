---
UID: NF:synchapi.CreateWaitableTimerExW
title: CreateWaitableTimerExW function (synchapi.h)
description: Creates or opens a waitable timer object and returns a handle to the object.
helpviewer_keywords: ["CREATE_WAITABLE_TIMER_MANUAL_RESET","CreateWaitableTimerEx","CreateWaitableTimerEx function","CreateWaitableTimerExA","CreateWaitableTimerExW","base.createwaitabletimerex","synchapi/CreateWaitableTimerEx","synchapi/CreateWaitableTimerExA","synchapi/CreateWaitableTimerExW"]
old-location: base\createwaitabletimerex.htm
tech.root: Sync
ms.assetid: 9ef51567-7d0f-4a2e-a798-289564733410
ms.date: 12/05/2018
ms.keywords: CREATE_WAITABLE_TIMER_MANUAL_RESET, CreateWaitableTimerEx, CreateWaitableTimerEx function, CreateWaitableTimerExA, CreateWaitableTimerExW, base.createwaitabletimerex, synchapi/CreateWaitableTimerEx, synchapi/CreateWaitableTimerExA, synchapi/CreateWaitableTimerExW
f1_keywords:
- synchapi/CreateWaitableTimerEx
dev_langs:
- c++
req.header: synchapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateWaitableTimerExW (Unicode) and CreateWaitableTimerExA (ANSI)
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
- API-MS-Win-Core-Synch-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-Synch-l1-2-0.dll
- API-MS-Win-Core-Synch-l1-2-1.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
- API-MS-Win-Core-Synch-Ansi-L1-1-0.dll
- Kernel32Legacy.dll
api_name:
- CreateWaitableTimerEx
- CreateWaitableTimerExA
- CreateWaitableTimerExW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CreateWaitableTimerExW function


## -description


Creates or opens a waitable timer object and returns a handle to the object.


## -parameters




### -param lpTimerAttributes [in, optional]

A pointer to a 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)">SECURITY_ATTRIBUTES</a> structure. If this parameter is <b>NULL</b>, the timer handle cannot be inherited by child processes. 

If <i>lpTimerAttributes</i> is <b>NULL</b>, the timer object gets a default security descriptor and the handle cannot be inherited. The ACLs in the default security descriptor for a timer come from the primary or impersonation token of the creator.


### -param lpTimerName [in, optional]

The name of the timer object. The name is limited to <b>MAX_PATH</b> characters. Name comparison is case sensitive. 




If <i>lpTimerName</i> is <b>NULL</b>, the timer object is created without a name.

If <i>lpTimerName</i> matches the name of an existing event, semaphore, mutex, job, or file-mapping object, the function fails and 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_INVALID_HANDLE</b>. This occurs because these objects share the same namespace.

The name can have a "Global\" or "Local\" prefix to explicitly create the object in the global or session namespace. The remainder of the name can contain any character except the backslash character (\). For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/TermServ/kernel-object-namespaces">Kernel Object Namespaces</a>. Fast user switching is implemented using Terminal Services sessions. Kernel object names must follow the guidelines outlined for Terminal Services so that applications can support multiple users.

The object can be created in a private namespace. For more information, see <a href="https://docs.microsoft.com/windows/desktop/Sync/object-namespaces">Object Namespaces</a>.


### -param dwFlags [in]

This parameter can be 0 or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CREATE_WAITABLE_TIMER_MANUAL_RESET"></a><a id="create_waitable_timer_manual_reset"></a><dl>
<dt><b>CREATE_WAITABLE_TIMER_MANUAL_RESET</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The timer must be manually reset. Otherwise, the system automatically resets the timer after releasing a single waiting thread.

</td>
</tr>
</table>
 


### -param dwDesiredAccess [in]

The access mask for the timer object. For a list of access rights, see 
<a href="https://docs.microsoft.com/windows/desktop/Sync/synchronization-object-security-and-access-rights">Synchronization Object Security and Access Rights</a>.


## -returns



If the function succeeds, the return value is a handle to the timer object. If the named timer object exists before the function call, the function returns a handle to the existing object and 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_ALREADY_EXISTS</b>.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



Any thread of the calling process can specify the timer object handle in a call to one of the 
<a href="https://docs.microsoft.com/windows/desktop/Sync/wait-functions">wait functions</a>.

Multiple processes can have handles to the same timer object, enabling use of the object for interprocess synchronization.

<ul>
<li>A process created by the 
<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> function can inherit a handle to a timer object if the <i>lpTimerAttributes</i> parameter of 
<b>CreateWaitableTimerEx</b> enables inheritance.</li>
<li>A process can specify the timer object handle in a call to the <a href="https://docs.microsoft.com/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a> function. The resulting handle can be used by another process.</li>
<li>A process can specify the name of a timer object in a call to the 
[OpenWaitableTimer](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw) or 
<b>CreateWaitableTimerEx</b> function.</li>
</ul>
Use the <a href="https://docs.microsoft.com/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to close the handle. The system closes the handle automatically when the process terminates. The timer object is destroyed when its last handle has been closed.

To associate a timer with a window, use the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-settimer">SetTimer</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="https://docs.microsoft.com/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Sync/waitable-timer-objects">Waitable Timer Objects</a>
 

 

