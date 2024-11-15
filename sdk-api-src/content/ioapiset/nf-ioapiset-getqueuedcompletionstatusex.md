---
UID: NF:ioapiset.GetQueuedCompletionStatusEx
title: GetQueuedCompletionStatusEx function (ioapiset.h)
description: Retrieves multiple completion port entries simultaneously.
helpviewer_keywords: ["GetQueuedCompletionStatusEx","GetQueuedCompletionStatusEx function [Files]","fs.getqueuedcompletionstatusex_func","ioapiset/GetQueuedCompletionStatusEx","winbase/GetQueuedCompletionStatusEx"]
old-location: fs\getqueuedcompletionstatusex_func.htm
tech.root: fs
ms.assetid: 3996c02c-562c-4697-a091-e241ad54b239
ms.date: 12/05/2018
ms.keywords: GetQueuedCompletionStatusEx, GetQueuedCompletionStatusEx function [Files], fs.getqueuedcompletionstatusex_func, ioapiset/GetQueuedCompletionStatusEx, winbase/GetQueuedCompletionStatusEx
req.header: ioapiset.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - GetQueuedCompletionStatusEx
 - ioapiset/GetQueuedCompletionStatusEx
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
 - GetQueuedCompletionStatusEx
---

# GetQueuedCompletionStatusEx function


## -description

Retrieves  multiple completion port entries simultaneously. It waits for pending I/O 
    operations that are associated with the specified completion port to complete.

To dequeue I/O completion packets one at a time, use the 
    <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> function.

## -parameters

### -param CompletionPort [in]

A handle to the completion port. To create a completion port, use the 
       <a href="/windows/desktop/FileIO/createiocompletionport">CreateIoCompletionPort</a> function.

### -param lpCompletionPortEntries [out]

On input, points to a pre-allocated array of 
       <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped_entry">OVERLAPPED_ENTRY</a> structures.

On output, receives an array of <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped_entry">OVERLAPPED_ENTRY</a> 
       structures that hold the entries. The number of array elements is provided by 
       <i>ulNumEntriesRemoved</i>.

The number of bytes transferred during each I/O, the completion key that indicates on which file each I/O 
       occurred, and the overlapped structure address used in each original I/O are all returned in the 
       <i>lpCompletionPortEntries</i> array.

### -param ulCount [in]

The maximum number of entries to remove.

### -param ulNumEntriesRemoved [out]

A pointer to a variable that receives the number of entries actually removed.

### -param dwMilliseconds [in]

The number of milliseconds that the caller is willing to wait for a completion packet to appear at the 
       completion port. If a completion packet does not appear within the specified time, the function times out and 
       returns <b>FALSE</b>.

If <i>dwMilliseconds</i> is <b>INFINITE</b> (0xFFFFFFFF), the function 
       will never time out. If <i>dwMilliseconds</i> is zero and there is no I/O operation to 
       dequeue, the function will time out immediately.

**Windows XP, Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008, and Windows Server 2008 R2:** The <i>dwMilliseconds</i> value includes time spent in low-power states. For example, the timeout continues counting down while the computer is asleep.

**Windows 8 and newer, Windows Server 2012 and newer:** The <i>dwMilliseconds</i> value does not include time spent in low-power states. For example, the timeout does not continue counting down while the computer is asleep.

### -param fAlertable [in]

If this parameter is <b>FALSE</b>, the function does not return until the time-out period 
       has elapsed or an entry is retrieved.

If the parameter is <b>TRUE</b> and there are no available entries, the function performs 
       an alertable wait. The thread returns when the system queues an I/O completion routine or APC to the thread and 
       the thread executes the function.

A completion routine is queued when the <a href="/windows/desktop/api/fileapi/nf-fileapi-readfileex">ReadFileEx</a> or 
       <a href="/windows/desktop/api/fileapi/nf-fileapi-writefileex">WriteFileEx</a> function in which it was specified has 
       completed, and the calling thread is the thread that initiated the operation. An APC is queued when you call 
       <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc">QueueUserAPC</a>.

## -returns

Returns nonzero (<b>TRUE</b>) if successful or zero (<b>FALSE</b>) otherwise.

To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function associates a thread with the specified completion port. A thread can be associated with at most 
     one completion port.

This function returns <b>TRUE</b> when at least one pending I/O is completed, but it is 
     possible that one or more I/O operations failed. Note that it is up to the user of this function to check the 
     list of returned entries in the <i>lpCompletionPortEntries</i> parameter to determine which of 
     them correspond to any possible failed I/O operations by looking at the status contained in the 
     <b>lpOverlapped</b> member in each 
     <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped_entry">OVERLAPPED_ENTRY</a>.

This function returns <b>FALSE</b> when no I/O operation was dequeued. This typically means 
     that an error occurred while processing the parameters to this call, or that the 
     <i>CompletionPort</i> handle was closed or is otherwise invalid. The 
     <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function provides extended error 
     information.

If a call to <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatusEx</a> 
     fails because the handle associated with it is closed, the function returns <b>FALSE</b> and 
     <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return 
     <b>ERROR_ABANDONED_WAIT_0</b>.

Server applications may have several threads calling the 
     <b>GetQueuedCompletionStatusEx</b> function 
     for the same completion port.  As I/O operations complete, they are queued to this port in first-in-first-out 
     order. If a thread is actively waiting on this call, one or more queued requests complete the call for that 
     thread only.

For more information on I/O completion port theory, usage, and associated functions, see 
     <a href="/windows/desktop/FileIO/i-o-completion-ports">I/O Completion Ports</a>.

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
