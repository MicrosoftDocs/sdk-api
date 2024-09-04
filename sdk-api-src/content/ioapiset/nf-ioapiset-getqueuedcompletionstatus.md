---
UID: NF:ioapiset.GetQueuedCompletionStatus
title: GetQueuedCompletionStatus function (ioapiset.h)
description: Attempts to dequeue an I/O completion packet from the specified I/O completion port.
helpviewer_keywords: ["GetQueuedCompletionStatus","GetQueuedCompletionStatus function [Files]","_win32_getqueuedcompletionstatus","base.getqueuedcompletionstatus","fs.getqueuedcompletionstatus","ioapiset/GetQueuedCompletionStatus"]
old-location: fs\getqueuedcompletionstatus.htm
tech.root: fs
ms.assetid: 8121a38b-0fe1-43b8-aed6-4b85af1feba9
ms.date: 12/05/2018
ms.keywords: GetQueuedCompletionStatus, GetQueuedCompletionStatus function [Files], _win32_getqueuedcompletionstatus, base.getqueuedcompletionstatus, fs.getqueuedcompletionstatus, ioapiset/GetQueuedCompletionStatus
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
 - GetQueuedCompletionStatus
 - ioapiset/GetQueuedCompletionStatus
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
 - GetQueuedCompletionStatus
---

# GetQueuedCompletionStatus function


## -description

Attempts to dequeue an I/O completion packet from the specified I/O completion port. If there is no completion packet queued, the function waits for a pending I/O operation associated 
with the completion port to complete.

To dequeue multiple I/O completion packets at once, use the <a href="/windows/desktop/FileIO/getqueuedcompletionstatusex-func">GetQueuedCompletionStatusEx</a> function.

## -parameters

### -param CompletionPort [in]

A handle to the completion port. To create a completion port, use the 
<a href="/windows/desktop/FileIO/createiocompletionport">CreateIoCompletionPort</a> function.

### -param lpNumberOfBytesTransferred

A pointer to a variable that receives the number of bytes transferred in a completed I/O operation.

### -param lpCompletionKey [out]

A pointer to a variable that receives the completion key value associated with the file handle whose I/O operation has completed. A completion key is a per-file key that is specified in a call to 
<a href="/windows/desktop/FileIO/createiocompletionport">CreateIoCompletionPort</a>.

### -param lpOverlapped [out]

A pointer to a variable that receives the address of the 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure that was specified when the completed I/O operation was started. 

Even if you have passed the function a file handle associated with a completion port and a valid 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure, an application can prevent completion port notification. This is done by specifying a valid event handle for the <b>hEvent</b> member of the <b>OVERLAPPED</b> structure, and setting its low-order bit. A valid event handle whose low-order bit is set prevents the completion of the overlapped I/O from enqueing a completion packet to the completion port.
### -param dwMilliseconds [in]

The number of milliseconds that the caller is willing to wait for a completion packet to appear at the completion port. If a completion packet does not appear within the specified time, the function times out, returns <b>FALSE</b>, and sets *<i>lpOverlapped</i> to <b>NULL</b>.

If <i>dwMilliseconds</i> is <b>INFINITE</b>, the function will never time out. If <i>dwMilliseconds</i> is zero and there is no I/O operation to dequeue, the function will time out immediately.

**Windows XP, Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008, and Windows Server 2008 R2:** The <i>dwMilliseconds</i> value includes time spent in low-power states. For example, the timeout continues counting down while the computer is asleep.

**Windows 8 and newer, Windows Server 2012 and newer:** The <i>dwMilliseconds</i> value does not include time spent in low-power states. For example, the timeout does not continue counting down while the computer is asleep.

## -returns

Returns nonzero (<b>TRUE</b>) if successful or zero (<b>FALSE</b>) otherwise.

To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

For more information, see the Remarks section.

## -remarks

This function associates a thread with the specified completion port. A thread can be associated with at most one completion port.  

If a call to <b>GetQueuedCompletionStatus</b> fails because the completion port handle associated with it is closed while the call is outstanding, the function returns <b>FALSE</b>, <i>*lpOverlapped</i> will be <b>NULL</b>,  and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return <b>ERROR_ABANDONED_WAIT_0</b>.

<b>Windows Server 2003 and Windows XP:  </b>Closing the completion port handle while a call is outstanding will not result in the previously stated behavior.  The function will continue to wait until an entry is removed from the port or until a time-out occurs, if specified as a value other than <b>INFINITE</b>.

If the <b>GetQueuedCompletionStatus</b> function succeeds, it dequeued a completion packet for a successful I/O operation from the completion port and has stored information in the variables pointed to by the
following parameters: <i>lpNumberOfBytes</i>, <i>lpCompletionKey</i>, and <i>lpOverlapped</i>. Upon failure (the return value is <b>FALSE</b>), those same parameters can contain particular value combinations as follows:

<ul>
<li>If *<i>lpOverlapped</i> is <b>NULL</b>, the function did not dequeue a completion packet from the completion port. In this case, the function does not store information in
 the variables pointed to by the <i>lpNumberOfBytes</i> and <i>lpCompletionKey</i> parameters, and their values are indeterminate.</li>
<li>If *<i>lpOverlapped</i> is not <b>NULL</b> and the function dequeues a completion packet for a failed I/O operation from the completion port, the function stores
 information about the failed operation in the variables pointed to by <i>lpNumberOfBytes</i>, <i>lpCompletionKey</i>, and <i>lpOverlapped</i>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.</li>
</ul>
For more information on I/O completion port theory, usage, and associated functions, see <a href="/windows/desktop/FileIO/i-o-completion-ports">I/O Completion Ports</a>.

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

<a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe">ConnectNamedPipe</a>



<a href="/windows/desktop/FileIO/createiocompletionport">CreateIoCompletionPort</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<b>Functions</b>



<a href="/windows/desktop/FileIO/getqueuedcompletionstatusex-func">GetQueuedCompletionStatusEx</a>



<a href="/windows/desktop/FileIO/i-o-completion-ports">I/O Completion Ports</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-lockfileex">LockFileEx</a>



<b>Overview Topics</b>



<a href="/windows/desktop/FileIO/postqueuedcompletionstatus">PostQueuedCompletionStatus</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a>



<a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe">TransactNamedPipe</a>



<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>



<a href="/windows/desktop/api/winbase/nf-winbase-waitcommevent">WaitCommEvent</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a>
