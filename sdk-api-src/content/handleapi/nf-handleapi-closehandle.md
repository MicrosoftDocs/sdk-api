---
UID: NF:handleapi.CloseHandle
title: CloseHandle function (handleapi.h)
description: Closes an open object handle.
helpviewer_keywords: ["CloseHandle","CloseHandle function","_win32_closehandle","base.closehandle","handleapi/CloseHandle"]
old-location: base\closehandle.htm
tech.root: winprog
ms.assetid: 9b84891d-62ca-4ddc-97b7-c4c79482abd9
ms.date: 12/05/2018
ms.keywords: CloseHandle, CloseHandle function, _win32_closehandle, base.closehandle, handleapi/CloseHandle
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: snippet-project
f1_keywords:
 - CloseHandle
 - handleapi/CloseHandle
dev_langs:
 - c++
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
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If the application is running under a debugger,  the function will throw an exception if it receives either a  handle value that is not valid  or a pseudo-handle value. This can happen if you close a handle twice, or if you  call 
<b>CloseHandle</b> on a handle returned by the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea">FindFirstFile</a> function instead of calling the <a href="/windows/desktop/api/fileapi/nf-fileapi-findclose">FindClose</a> function.

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
The documentation for the functions that create these objects indicates that <b>CloseHandle</b> should be used when you are finished with the object, and what happens to pending operations on the object after the handle is closed. In general, <b>CloseHandle</b> invalidates the specified object handle, decrements the object's handle count, and performs object retention checks. After the last handle to an object is closed, the object is removed from the system. For a summary of the creator functions for these objects, see <a href="/windows/desktop/SysInfo/kernel-objects">Kernel Objects</a>.

Generally, an application should call <b>CloseHandle</b> once for each handle it opens. It is usually not necessary to call <b>CloseHandle</b> if a function that uses a handle fails with ERROR_INVALID_HANDLE, because this error usually indicates that the handle is already invalidated. However, some functions use ERROR_INVALID_HANDLE to indicate that the object itself is no longer valid. For example, a function that attempts to use a handle to a file on a network might fail with ERROR_INVALID_HANDLE if the network connection is severed, because the file object is no longer available. In this case, the application should close the handle.

If a handle is transacted, all handles bound to a transaction should be closed before the transaction is committed. If a transacted handle was opened by calling <a href="/windows/desktop/api/winbase/nf-winbase-createfiletransacteda">CreateFileTransacted</a> with the FILE_FLAG_DELETE_ON_CLOSE flag, the file is not deleted until the application closes the handle and calls <a href="/windows/desktop/api/ktmw32/nf-ktmw32-committransaction">CommitTransaction</a>. For more information about transacted objects, see <a href="/windows/desktop/Ktm/programming-model">Working With Transactions</a>.

Closing a thread handle does not terminate the associated thread or remove the thread object. Closing a process handle does not terminate the associated process or remove the process object. To remove a thread object, you must terminate the thread, then close all handles to the thread. For more information, see <a href="/windows/desktop/ProcThread/terminating-a-thread">Terminating a Thread</a>. To remove a process object, you must terminate the process, then close all handles to the process. For more information, see <a href="/windows/desktop/ProcThread/terminating-a-process">Terminating a Process</a>.

Closing a handle to a file mapping can succeed even when there are file views that are still open. For more information, see <a href="/windows/desktop/Memory/closing-a-file-mapping-object">Closing a File Mapping Object</a>.

Do not use the <b>CloseHandle</b>  function to close a socket. Instead, use  the <a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a> function, which releases all resources associated with the socket including the handle to the socket object. For more information, see <a href="/windows/desktop/WinSock/graceful-shutdown-linger-options-and-socket-closure-2">Socket Closure</a>.

Do not use the <b>CloseHandle</b>  function to close a handle to an open registry key. Instead, use  the <a href="/windows/desktop/api/winreg/nf-winreg-regclosekey">RegCloseKey</a> function. <b>CloseHandle</b> does not close the handle to the registry key, but does not return an error to indicate this failure.


#### Examples


```cpp
dwPriorityClass = 0;
hProcess = OpenProcess( PROCESS_ALL_ACCESS, FALSE, pe32.th32ProcessID );
if( hProcess == NULL )
	printError( TEXT("OpenProcess") );
else
{
	dwPriorityClass = GetPriorityClass( hProcess );
	if( !dwPriorityClass )
	printError( TEXT("GetPriorityClass") );
	CloseHandle( hProcess );
}
```

To see this example in context, see 
<a href="/windows/desktop/ToolHelp/taking-a-snapshot-and-viewing-processes">Taking a Snapshot and Viewing Processes</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createfiletransacteda">CreateFileTransacted</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-deletefilea">DeleteFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findclose">FindClose</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea">FindFirstFile</a>



<a href="/windows/desktop/SysInfo/handle-and-object-functions">Handle and
		  Object Functions</a>



<a href="/windows/desktop/SysInfo/kernel-objects">Kernel Objects</a>



<a href="/windows/desktop/SysInfo/object-interface">Object Interface</a>