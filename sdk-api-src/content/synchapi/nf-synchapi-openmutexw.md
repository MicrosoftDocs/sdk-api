---
UID: NF:synchapi.OpenMutexW
title: OpenMutexW function
author: windows-sdk-content
description: Opens an existing named mutex object.
old-location: base\openmutex.htm
tech.root: sync
ms.assetid: 0ea363c2-1ff7-4bf5-9e94-f1f17b8c8a11
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: OpenMutex, OpenMutex function, OpenMutexA, OpenMutexW, _win32_openmutex, base.openmutex, synchapi/OpenMutex, synchapi/OpenMutexA, synchapi/OpenMutexW
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
req.unicode-ansi: OpenMutexW (Unicode) and OpenMutexA (ANSI)
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OpenMutexW function


## -description


Opens an existing named mutex object.


## -parameters




### -param dwDesiredAccess [in]

The access to the mutex object. Only the <b>SYNCHRONIZE</b> access right is required to use a mutex; to change the mutex's security, specify <b>MUTEX_ALL_ACCESS</b>. The function fails if the security descriptor of the specified object does not permit the requested access for the calling process. For a list of access rights, see 
<a href="https://msdn.microsoft.com/92478298-617c-4672-a1cc-9a8e9af40327">Synchronization Object Security and Access Rights</a>.


### -param bInheritHandle [in]

If this value is <b>TRUE</b>, processes created by this process will inherit the handle. Otherwise, the processes do not inherit this handle.


### -param lpName [in]

The name of the mutex to be opened. Name comparisons are case sensitive. 




This function can open objects in a private namespace. For more information, see <a href="https://msdn.microsoft.com/6a84ec16-fa65-4cdd-861a-eccf5d0eee2b">Object Namespaces</a>.

<b>Terminal Services:  </b>The name can have a "Global\" or "Local\" prefix to explicitly open an object in the global or session namespace. The remainder of the name can contain any character except the backslash character (\). For more information, see 
<a href="https://msdn.microsoft.com/771e0bbf-bd73-4e87-aa1e-945c1287b517">Kernel Object Namespaces</a>.

<b>Note</b>  Fast user switching is implemented using Terminal Services sessions. The first user to log on uses session 0, the next user to log on uses session 1, and so on. Kernel object names must follow the guidelines outlined for Terminal Services so that applications can support multiple users.


## -returns



If the function succeeds, the return value is a handle to the mutex object.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If a named mutex does not exist, the function fails and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_FILE_NOT_FOUND</b>.




## -remarks



The 
<b>OpenMutex</b> function enables multiple processes to open handles of the same mutex object. The function succeeds only if some process has already created the mutex by using the 
<a href="https://msdn.microsoft.com/c8315d1c-98c9-4f0a-ae0d-800d7d8100cd">CreateMutex</a> function. The calling process can use the returned handle in any function that requires a handle to a mutex object, such as the 
<a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">wait functions</a>, subject to the limitations of the access specified in the <i>dwDesiredAccess</i> parameter.

The handle can be duplicated by using the <a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a> function. Use the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function to close the handle. The system closes the handle automatically when the process terminates. The mutex object is destroyed when its last handle has been closed.

If your multithreaded application must repeatedly create, open, and close a named mutex object, a race condition can occur. In this situation, it is better to use <a href="https://msdn.microsoft.com/c8315d1c-98c9-4f0a-ae0d-800d7d8100cd">CreateMutex</a> instead of <b>OpenMutex</b>, because <b>CreateMutex</b> opens a mutex if it exists and creates it if it does not.


#### Examples

For an example that uses 
<b>OpenMutex</b>, see 
<a href="https://msdn.microsoft.com/06199f83-8fe0-42b9-9db1-58fe1443db4e">Using Named Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/c8315d1c-98c9-4f0a-ae0d-800d7d8100cd">CreateMutex</a>



<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>



<a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a>



<a href="https://msdn.microsoft.com/eca0795a-1fd0-4034-9d61-9416670919cf">Mutex Objects</a>



<a href="https://msdn.microsoft.com/00a00227-45fc-49a1-8ff5-aeccb172d16a">Object Names</a>



<a href="https://msdn.microsoft.com/c3e4daa8-92de-455c-847c-ea59225b3aa2">ReleaseMutex</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

