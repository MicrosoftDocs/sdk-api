---
UID: NF:ioapiset.CreateIoCompletionPort
title: CreateIoCompletionPort function (ioapiset.h)
description: Creates an input/output (I/O) completion port and associates it with a specified file handle, or creates an I/O completion port that is not yet associated with a file handle, allowing association at a later time.
helpviewer_keywords: ["CreateIoCompletionPort","CreateIoCompletionPort function [Files]","_win32_createiocompletionport","base.createiocompletionport","fs.createiocompletionport","ioapiset/CreateIoCompletionPort","winbase/CreateIoCompletionPort"]
old-location: fs\createiocompletionport.htm
tech.root: fs
ms.assetid: 40cb47fc-7b15-47f6-bee2-2611d4686053
ms.date: 12/05/2018
ms.keywords: CreateIoCompletionPort, CreateIoCompletionPort function [Files], _win32_createiocompletionport, base.createiocompletionport, fs.createiocompletionport, ioapiset/CreateIoCompletionPort, winbase/CreateIoCompletionPort
req.header: ioapiset.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
ms.custom: 19H1
f1_keywords:
 - CreateIoCompletionPort
 - ioapiset/CreateIoCompletionPort
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-io-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-io-l1-1-1.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
api_name:
 - CreateIoCompletionPort
---

# CreateIoCompletionPort function


## -description

Creates an input/output (I/O) completion port and associates it with a specified file handle, or creates an I/O completion port that is not yet associated with a file handle, allowing association at a later time.

Associating an instance of an opened file handle with an I/O completion port allows a process to receive notification of the completion of asynchronous I/O operations involving that file handle.
<div class="alert"><b>Note</b>  <p class="note">The term <i>file handle</i> as used here refers to a system abstraction that represents an overlapped I/O endpoint, not only a file on disk. Any system objects that support overlapped I/O—such as network endpoints, TCP sockets, named pipes, and mail slots—can be used as file handles. For additional information, see the Remarks section.

</div><div> </div>

## -parameters

### -param FileHandle [in]

An open file handle or <b>INVALID_HANDLE_VALUE</b>.

The handle must be to an object that supports overlapped I/O.

If a handle is provided, it has to have been opened for overlapped I/O completion. For example, you must specify the <b>FILE_FLAG_OVERLAPPED</b> flag when using the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function to obtain the handle.

If <b>INVALID_HANDLE_VALUE</b> is specified, the function creates an I/O completion port without associating it with a file handle. In this case, the <i>ExistingCompletionPort</i> parameter must be <b>NULL</b> and the <i>CompletionKey</i> parameter is ignored.

### -param ExistingCompletionPort [in, optional]

A handle to an existing I/O completion port or <b>NULL</b>.

If this parameter specifies an existing I/O completion port, the function associates it with the handle specified by the <i>FileHandle</i> parameter. The function returns the handle of the existing I/O completion port if successful; it does not create a new I/O completion port.

If this parameter is <b>NULL</b>, the function creates a new I/O completion port and, if the <i>FileHandle</i> parameter is valid, associates it with the new I/O completion port. Otherwise no file handle association occurs. The function returns the handle to the new I/O completion port if successful.

### -param CompletionKey [in]

The per-handle user-defined completion key that is included in every I/O completion packet for the specified file handle. For more information, see the Remarks section.

### -param NumberOfConcurrentThreads [in]

The maximum number of threads that the operating system can allow to concurrently process I/O completion packets for the I/O completion port. This parameter is ignored if the <i>ExistingCompletionPort</i> parameter is not <b>NULL</b>.

If this parameter is zero, the system allows as many concurrently running threads as there are processors in the system.

## -returns

If the function succeeds, the return value is the handle to an I/O completion port:

<ul>
<li>
If the <i>ExistingCompletionPort</i> parameter was <b>NULL</b>, the return value is a new handle.

</li>
<li>
If the <i>ExistingCompletionPort</i> parameter was a valid I/O completion port handle, the return value is that same handle.

</li>
<li>
If the <i>FileHandle</i> parameter was a valid handle, that file handle is now associated with the returned I/O completion port.

</li>
</ul>
If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

The I/O system can be instructed to send I/O completion notification packets to I/O completion ports, where they are queued. The 
<b>CreateIoCompletionPort</b> function provides this functionality.

An I/O completion port and its handle are associated with the process that created it and is not sharable between processes. However, a single handle is sharable between threads in the same process.

<b>CreateIoCompletionPort</b> can be used in three distinct modes:

<ul>
<li>Create only an I/O completion port without associating it with a file handle. </li>
<li>Associate an existing I/O completion port with a file handle.</li>
<li>Perform both creation and association in a single call.</li>
</ul>
To create an I/O completion port without associating it, set the <i>FileHandle</i> parameter to <b>INVALID_HANDLE_VALUE</b>, the <i>ExistingCompletionPort</i> parameter to <b>NULL</b>, and the <i>CompletionKey</i> parameter to zero (which is ignored in this case). Set the <i>NumberOfConcurrentThreads</i> parameter to the desired concurrency value for the new I/O completion port, or zero for the default (the number of processors in the system).

The handle passed in the <i>FileHandle</i> parameter can be any handle that supports overlapped I/O. Most commonly, this is a handle opened by the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function using the <b>FILE_FLAG_OVERLAPPED</b> flag (for example, files, mail slots, and pipes). Objects created by other functions such as <a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a> can also be associated with an I/O completion port. For an example using sockets, see <a href="/windows/desktop/api/mswsock/nf-mswsock-acceptex">AcceptEx</a>. A handle can be associated with only one I/O completion port, and after the association is made, the handle remains associated with that I/O completion port until it is closed.

For more information on I/O completion port theory, usage, and associated functions, see <a href="/windows/desktop/FileIO/i-o-completion-ports">I/O Completion Ports</a>.

Multiple file handles can be associated with a single I/O completion port by calling <b>CreateIoCompletionPort</b> multiple times with the same I/O completion port handle in the <i>ExistingCompletionPort</i> parameter and a different file handle in the <i>FileHandle</i> parameter each time.

Use the <i>CompletionKey</i> parameter to help your application track which I/O operations have completed. This value is not used by <b>CreateIoCompletionPort</b> for functional control; rather, it is attached to the file handle specified in the <i>FileHandle</i> parameter at the time of association with an I/O completion port. This completion key should be unique for each file handle, and it accompanies the file handle throughout the internal completion queuing process. It is returned in the <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> function call when a completion packet arrives. The <i>CompletionKey</i> parameter is also used by the <a href="/windows/desktop/FileIO/postqueuedcompletionstatus">PostQueuedCompletionStatus</a> function to queue your own special-purpose completion packets.

After an instance of an open handle is associated with an I/O completion port, it cannot be used in the 
                <a href="/windows/desktop/api/fileapi/nf-fileapi-readfileex">ReadFileEx</a> or 
<a href="/windows/desktop/api/fileapi/nf-fileapi-writefileex">WriteFileEx</a> function because these functions have their own asynchronous I/O mechanisms. 

It is best not to share a file handle associated with an I/O completion port by using either handle inheritance or a call to the 
<a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a> function. Operations performed with such duplicate handles generate completion notifications. Careful consideration is advised.

The I/O completion port handle and every file handle associated with that particular I/O completion port are known as <i>references to the I/O completion port</i>. The I/O completion port is released when there are no more references to it. Therefore, all of these handles must be properly closed to release the I/O completion port and its associated system resources. After these conditions are satisfied, close the I/O completion port handle by calling the 
<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function.

In Windows 8 and Windows Server 2012, this function is supported by the following technologies.

<table>
<tr>
<th>Technology</th>
<th>Supported</th>
</tr>
<tr>
<td>
Server Message Block (SMB) 3.0 protocol

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Cluster Shared Volume File System (CsvFS)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
Yes

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mswsock/nf-mswsock-acceptex">AcceptEx</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<b>Functions</b>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a>



<a href="/windows/desktop/FileIO/getqueuedcompletionstatusex-func">GetQueuedCompletionStatusEx</a>



<a href="/windows/desktop/FileIO/i-o-completion-ports">I/O Completion Ports</a>



<b>Overview Topics</b>



<a href="/windows/desktop/FileIO/postqueuedcompletionstatus">PostQueuedCompletionStatus</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfileex">ReadFileEx</a>



<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows 
    Headers</a>



<a href="/windows/desktop/WinSock/windows-sockets-start-page-2">Windows Sockets 2</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefileex">WriteFileEx</a>