---
UID: NF:handleapi.CloseHandle
title: CloseHandle function
author: windows-sdk-content
description: Closes an open object handle.
old-location: base\closehandle.htm
tech.root: sysinfo
ms.assetid: 9b84891d-62ca-4ddc-97b7-c4c79482abd9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CloseHandle, CloseHandle function, _win32_closehandle, base.closehandle, handleapi/CloseHandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: handleapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - API-MS-Win-Core-handle-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - CloseHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CloseHandle function


## -description


Closes an open object handle.


## -parameters




### -param hObject [in]

A valid handle to an open object.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If the application is running under a debugger,  the function will throw an exception if it receives either a  handle value that is not valid  or a pseudo-handle value. This can happen if you close a handle twice, or if you  call 
<b>CloseHandle</b> on a handle returned by the 
<a href="https://msdn.microsoft.com/02fc92c4-582d-4c9f-a811-b5c839e9fffa">FindFirstFile</a> function instead of calling the <a href="https://msdn.microsoft.com/64b3bc49-1e0e-4572-9d9f-936c45f5b01c">FindClose</a> function.




## -remarks



The 
<b>CloseHandle</b> function closes handles to the following objects:

<ul>
<li>Access token</li>
<li>Communications device</li>
<li>Console input</li>
<li>Console screen buffer</li>
<li>Event</li>
<li>File</li>
<li>File mapping</li>
<li>I/O completion port</li>
<li>Job</li>
<li>Mailslot</li>
<li>Memory resource notification</li>
<li>Mutex</li>
<li>Named pipe</li>
<li>Pipe</li>
<li>Process</li>
<li>Semaphore</li>
<li>Thread</li>
<li>Transaction</li>
<li>Waitable timer</li>
</ul>
The documentation for the functions that create these objects indicates that <b>CloseHandle</b> should be used when you are finished with the object, and what happens to pending operations on the object after the handle is closed. In general, <b>CloseHandle</b> invalidates the specified object handle, decrements the object's handle count, and performs object retention checks. After the last handle to an object is closed, the object is removed from the system. For a summary of the creator functions for these objects, see <a href="https://msdn.microsoft.com/3e3288dd-155a-41d0-9d43-5f49ed4c4a9d">Kernel Objects</a>.

Generally, an application should call <b>CloseHandle</b> once for each handle it opens. It is usually not necessary to call <b>CloseHandle</b> if a function that uses a handle fails with ERROR_INVALID_HANDLE, because this error usually indicates that the handle is already invalidated. However, some functions use ERROR_INVALID_HANDLE to indicate that the object itself is no longer valid. For example, a function that attempts to use a handle to a file on a network might fail with ERROR_INVALID_HANDLE if the network connection is severed, because the file object is no longer available. In this case, the application should close the handle.

If a handle is transacted, all handles bound to a transaction should be closed before the transaction is committed. If a transacted handle was opened by calling <a href="https://msdn.microsoft.com/0cbc081d-8787-409b-84bc-a6a28d8f83a0">CreateFileTransacted</a> with the FILE_FLAG_DELETE_ON_CLOSE flag, the file is not deleted until the application closes the handle and calls <a href="https://msdn.microsoft.com/17db5e1f-685b-46f0-bac6-dff4c18bb515">CommitTransaction</a>. For more information about transacted objects, see <a href="https://msdn.microsoft.com/356c66dc-5ddd-472f-835c-2e2cb019bcfd">Working With Transactions</a>.

Closing a thread handle does not terminate the associated thread or remove the thread object. Closing a process handle does not terminate the associated process or remove the process object. To remove a thread object, you must terminate the thread, then close all handles to the thread. For more information, see <a href="https://msdn.microsoft.com/633e5d0c-e9d8-4f9a-9411-17cbe9e2e6e4">Terminating a Thread</a>. To remove a process object, you must terminate the process, then close all handles to the process. For more information, see <a href="https://msdn.microsoft.com/af24d157-2719-4052-8029-1eb8010047cc">Terminating a Process</a>.

Closing a handle to a file mapping can succeed even when there are file views that are still open. For more information, see <a href="https://msdn.microsoft.com/d62d068c-9b1d-4dbf-8b21-31a636a41456">Closing a File Mapping Object</a>.

Do not use the <b>CloseHandle</b>  function to close a socket. Instead, use  the <a href="https://msdn.microsoft.com/2f357aa8-389b-4c92-8a9f-289e048cc41c">closesocket</a> function, which releases all resources associated with the socket including the handle to the socket object. For more information, see <a href="https://msdn.microsoft.com/383747c3-dd3d-4a18-b4e8-2815d5e5c0c7">Socket Closure</a>.

Do not use the <b>CloseHandle</b>  function to close a handle to an open registry key. Instead, use  the <a href="https://msdn.microsoft.com/10175499-abf3-4694-9594-bb97b43f3fa5">RegCloseKey</a> function. <b>CloseHandle</b> does not close the handle to the registry key, but does not return an error to indicate this failure.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/318d166f-858f-4f33-9422-977e0c4beb3f">Taking a Snapshot and Viewing Processes</a>.

<div class="code"></div>



## -see-also




<a href="base.createfile">CreateFile</a>



<a href="https://msdn.microsoft.com/0cbc081d-8787-409b-84bc-a6a28d8f83a0">CreateFileTransacted</a>



<a href="base.deletefile">DeleteFile</a>



<a href="base.findclose">FindClose</a>



<a href="base.findfirstfile">FindFirstFile</a>



<a href="https://msdn.microsoft.com/b4769e19-7478-4919-a9d2-8086ece6da70">Handle and
		  Object Functions</a>



<a href="https://msdn.microsoft.com/3e3288dd-155a-41d0-9d43-5f49ed4c4a9d">Kernel Objects</a>



<a href="https://msdn.microsoft.com/437419c7-d6c5-4cae-b5d0-d552c75d4448">Object Interface</a>
 

 

