---
UID: NF:synchapi.OpenWaitableTimerW
title: OpenWaitableTimerW function
author: windows-sdk-content
description: Opens an existing named waitable timer object.
old-location: base\openwaitabletimer.htm
old-project: sync
ms.assetid: 0f9b49ea-5d04-449c-9b7d-f79ab28b548b
ms.author: windowssdkdev
ms.date: 07/06/2018
ms.keywords: OpenWaitableTimer, OpenWaitableTimer function, OpenWaitableTimerA, OpenWaitableTimerW, _win32_openwaitabletimer, base.openwaitabletimer, synchapi/OpenWaitableTimer, synchapi/OpenWaitableTimerA, synchapi/OpenWaitableTimerW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: synchapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OpenWaitableTimerW (Unicode) and OpenWaitableTimerA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ITEMPROP, *LPITEMPROP
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
 - OpenWaitableTimer
 - OpenWaitableTimerA
 - OpenWaitableTimerW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# OpenWaitableTimerW function


## -description


Opens an existing named waitable timer object.


## -parameters




### -param dwDesiredAccess [in]

The access to the timer object. The function fails if the security descriptor of the specified object does 
      not permit the requested access for the calling process. For a list of access rights, see 
      <a href="https://msdn.microsoft.com/92478298-617c-4672-a1cc-9a8e9af40327">Synchronization Object Security and Access Rights</a>.


### -param bInheritHandle [in]

If this value is <b>TRUE</b>, processes created by this process will inherit the handle. Otherwise, the processes do not inherit this handle.


### -param lpTimerName [in]

The name of the timer object. The name is limited to <b>MAX_PATH</b> characters. Name comparison is case sensitive.

This function can open objects in a private namespace. For more information, see <a href="https://msdn.microsoft.com/6a84ec16-fa65-4cdd-861a-eccf5d0eee2b">Object Namespaces</a>.

<b>Terminal Services:  </b>The name can have a "Global\" or "Local\" prefix to explicitly open an object in the global or session namespace. The remainder of the name can contain any character except the backslash character (\). For more information, see 
<a href="https://msdn.microsoft.com/771e0bbf-bd73-4e87-aa1e-945c1287b517">Kernel Object Namespaces</a>.

<b>Note</b>  Fast user switching is implemented using Terminal Services sessions. The first user to log on uses session 0, the next user to log on uses session 1, and so on. Kernel object names must follow the guidelines outlined for Terminal Services so that applications can support multiple users.


## -returns



If the function succeeds, the return value is a handle to the timer object.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>OpenWaitableTimer</b> function enables multiple processes to open handles to the same timer object. The function succeeds only if some process has already created the timer using the 
<a href="https://msdn.microsoft.com/41c915c4-424d-43dd-89d9-a6b4fbee701c">CreateWaitableTimer</a> function. The calling process can use the returned handle in any function that requires the handle to a timer object, such as the 
<a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">wait functions</a>, subject to the limitations of the access specified in the <i>dwDesiredAccess</i> parameter.

The returned handle can be duplicated by using the <a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a> function. Use the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function to close the handle. The system closes the handle automatically when the process terminates. The timer object is destroyed when its last handle has been closed.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0400 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/614a237b-71b3-4091-975d-4c0b3cd6ec69">CancelWaitableTimer</a>



<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>



<a href="https://msdn.microsoft.com/41c915c4-424d-43dd-89d9-a6b4fbee701c">CreateWaitableTimer</a>



<a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff557762">Object Names</a>



<a href="https://msdn.microsoft.com/237e22dc-696d-473f-8bb5-c28f7c7c75b2">SetWaitableTimer</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>



<a href="https://msdn.microsoft.com/5d39ada0-ea31-40d7-b075-aeb657ee508c">Waitable Timer Objects</a>
 

 

