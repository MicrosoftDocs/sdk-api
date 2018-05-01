---
UID: NF:synchapi.OpenEventW
title: OpenEventW function
author: windows-driver-content
description: Opens an existing named event object.
old-location: base\openevent.htm
old-project: Sync
ms.assetid: 46741024-ace3-44d6-b8a6-5621ad121a1a
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: OpenEvent, OpenEvent function, OpenEventA, OpenEventW, _win32_openevent, base.openevent, synchapi/OpenEvent, synchapi/OpenEventA, synchapi/OpenEventW, winbase/OpenEvent, winbase/OpenEventA, winbase/OpenEventW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: synchapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OpenEventW (Unicode) and OpenEventA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ITEMPROP, *LPITEMPROP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-Synch-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-Synch-l1-2-0.dll
-	API-MS-Win-Core-Synch-l1-2-1.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	MinKernelBase.dll
api_name:
-	OpenEvent
-	OpenEventA
-	OpenEventW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# OpenEventW function


## -description


Opens an existing named event object.


## -parameters




### -param dwDesiredAccess [in]

The access to the event object. The function fails if the security descriptor of the specified object does not permit the requested access for the calling process. For a list of access rights, see 
<a href="https://msdn.microsoft.com/92478298-617c-4672-a1cc-9a8e9af40327">Synchronization Object Security and Access Rights</a>.


### -param bInheritHandle [in]

If this value is <b>TRUE</b>, processes created by this process will inherit the handle. Otherwise, the processes do not inherit this handle.


### -param lpName [in]

The  name of the event to be opened. Name comparisons are case sensitive.

This function can open objects in a private namespace. For more information, see <a href="https://msdn.microsoft.com/6a84ec16-fa65-4cdd-861a-eccf5d0eee2b">Object Namespaces</a>.

<b>Terminal Services:  </b>The name can have a "Global\" or "Local\" prefix to explicitly open an object in the global or session namespace. The remainder of the name can contain any character except the backslash character (\). For more information, see 
<a href="https://msdn.microsoft.com/771e0bbf-bd73-4e87-aa1e-945c1287b517">Kernel Object Namespaces</a>.

<b>Note</b>  Fast user switching is implemented using Terminal Services sessions. The first user to log on uses session 0, the next user to log on uses session 1, and so on. Kernel object names must follow the guidelines outlined for Terminal Services so that applications can support multiple users.


## -returns



If the function succeeds, the return value is a handle to the event object.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>OpenEvent</b> function enables multiple processes to open handles of the same event object. The function succeeds only if some process has already created the event by using the 
<a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a> function. The calling process can use the returned handle in any function that requires a handle to an event object, subject to the limitations of the access specified in the <i>dwDesiredAccess</i> parameter.

The handle can be duplicated by using the <a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a> function. Use the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function to close the handle. The system closes the handle automatically when the process terminates. The event object is destroyed when its last handle has been closed.




## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>



<a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544323">Event Objects</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff557762">Object Names</a>



<a href="https://msdn.microsoft.com/b3cfe15a-1a0e-4c29-8840-032e56404400">PulseEvent</a>



<a href="https://msdn.microsoft.com/bba7caab-d1ed-4261-aeca-49f847458f4c">ResetEvent</a>



<a href="https://msdn.microsoft.com/b474eef1-5df9-4729-b940-0c5f201c5f31">SetEvent</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

