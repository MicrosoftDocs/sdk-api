---
UID: NF:synchapi.CreateWaitableTimerW
title: CreateWaitableTimerW function
author: windows-sdk-content
description: Creates or opens a waitable timer object.
old-location: base\createwaitabletimer.htm
tech.root: sync
ms.assetid: 41c915c4-424d-43dd-89d9-a6b4fbee701c
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: CreateWaitableTimer, CreateWaitableTimer function, CreateWaitableTimerA, CreateWaitableTimerW, _win32_createwaitabletimer, base.createwaitabletimer, synchapi/CreateWaitableTimer, synchapi/CreateWaitableTimerA, synchapi/CreateWaitableTimerW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateWaitableTimerW function


## -description


Creates or opens a waitable timer object.

To specify an access mask for the object, use the <a href="https://msdn.microsoft.com/9ef51567-7d0f-4a2e-a798-289564733410">CreateWaitableTimerEx</a> function.


## -parameters




### -param lpTimerAttributes [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> structure that specifies a security descriptor for the new timer object and determines whether child processes can inherit the returned handle. 

If <i>lpTimerAttributes</i> is <b>NULL</b>, the timer object gets a default security descriptor and the handle cannot be inherited. The ACLs in the default security descriptor for a timer come from the primary or impersonation token of the creator.


### -param bManualReset [in]

If this parameter is <b>TRUE</b>, the timer is a manual-reset notification timer. Otherwise, the timer is a synchronization timer.


### -param lpTimerName [in, optional]

The name of the timer object. The name is limited to <b>MAX_PATH</b> characters. Name comparison is case sensitive. 




If <i>lpTimerName</i> is <b>NULL</b>, the timer object is created without a name.

If <i>lpTimerName</i> matches the name of an existing event, semaphore, mutex, job, or file-mapping object, the function fails and 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_INVALID_HANDLE</b>. This occurs because these objects share the same namespace.

The name can have a "Global\" or "Local\" prefix to explicitly create the object in the global or session namespace. The remainder of the name can contain any character except the backslash character (\). For more information, see 
<a href="https://msdn.microsoft.com/771e0bbf-bd73-4e87-aa1e-945c1287b517">Kernel Object Namespaces</a>. Fast user switching is implemented using Terminal Services sessions. Kernel object names must follow the guidelines outlined for Terminal Services so that applications can support multiple users.

The object can be created in a private namespace. For more information, see <a href="https://msdn.microsoft.com/6a84ec16-fa65-4cdd-861a-eccf5d0eee2b">Object Namespaces</a>.


## -returns



If the function succeeds, the return value is a handle to the timer object. If the named timer object exists before the function call, the function returns a handle to the existing object and 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_ALREADY_EXISTS</b>.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The handle returned by 
<b>CreateWaitableTimer</b> is created with the <b>TIMER_ALL_ACCESS</b> access right; it can be used in any function that requires a handle to a timer object, provided that the caller has been granted access. If a timer is created from a service or thread that is impersonating a different user, you can either apply a security descriptor to the timer when you create it, or change the default security descriptor for the creating process by changing its default DACL. For more information, see 
<a href="https://msdn.microsoft.com/92478298-617c-4672-a1cc-9a8e9af40327">Synchronization Object Security and Access Rights</a>.

Any thread of the calling process can specify the timer object handle in a call to one of the 
<a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">wait functions</a>.

Multiple processes can have handles to the same timer object, enabling use of the object for interprocess synchronization.

<ul>
<li>A process created by the 
<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a> function can inherit a handle to a timer object if the <i>lpTimerAttributes</i> parameter of 
<b>CreateWaitableTimer</b> enables inheritance.</li>
<li>A process can specify the timer object handle in a call to the <a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a> function. The resulting handle can be used by another process.</li>
<li>A process can specify the name of a timer object in a call to the 
<a href="https://msdn.microsoft.com/0f9b49ea-5d04-449c-9b7d-f79ab28b548b">OpenWaitableTimer</a> or 
<b>CreateWaitableTimer</b> function.</li>
</ul>
Use the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function to close the handle. The system closes the handle automatically when the process terminates. The timer object is destroyed when its last handle has been closed.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0400 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.

To associate a timer with a window, use the <a href="https://msdn.microsoft.com/393038fa-972f-4151-b90a-cebf84c50867">SetTimer</a> function.


#### Examples

For an example that uses 
<b>CreateWaitableTimer</b>, see 
<a href="https://msdn.microsoft.com/3c84c2ad-6bac-4f14-a633-51d4529314af">Using Waitable Timer Objects</a>.


<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/614a237b-71b3-4091-975d-4c0b3cd6ec69">CancelWaitableTimer</a>



<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>



<a href="https://msdn.microsoft.com/9ef51567-7d0f-4a2e-a798-289564733410">CreateWaitableTimerEx</a>



<a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a>



<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>



<a href="https://msdn.microsoft.com/00a00227-45fc-49a1-8ff5-aeccb172d16a">Object Names</a>



<a href="https://msdn.microsoft.com/0f9b49ea-5d04-449c-9b7d-f79ab28b548b">OpenWaitableTimer</a>



<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/237e22dc-696d-473f-8bb5-c28f7c7c75b2">SetWaitableTimer</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>



<a href="https://msdn.microsoft.com/5d39ada0-ea31-40d7-b075-aeb657ee508c">Waitable Timer Objects</a>
 

 

