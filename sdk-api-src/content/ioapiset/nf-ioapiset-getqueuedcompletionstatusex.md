---
UID: NF:ioapiset.GetQueuedCompletionStatusEx
title: GetQueuedCompletionStatusEx function (ioapiset.h)
author: windows-sdk-content
description: Retrieves multiple completion port entries simultaneously.
old-location: fs\getqueuedcompletionstatusex_func.htm
tech.root: FileIO
ms.assetid: 3996c02c-562c-4697-a091-e241ad54b239
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetQueuedCompletionStatusEx, GetQueuedCompletionStatusEx function [Files], fs.getqueuedcompletionstatusex_func, ioapiset/GetQueuedCompletionStatusEx, winbase/GetQueuedCompletionStatusEx
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetQueuedCompletionStatusEx function


## -description


Retrieves  multiple completion port entries simultaneously. It waits for pending I/O 
    operations that are associated with the specified completion port to complete.

To dequeue I/O completion packets one at a time, use the 
    <a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a> function.


## -parameters




### -param CompletionPort [in]

A handle to the completion port. To create a completion port, use the 
       <a href="https://msdn.microsoft.com/40cb47fc-7b15-47f6-bee2-2611d4686053">CreateIoCompletionPort</a> function.


### -param lpCompletionPortEntries [out]

On input, points to a pre-allocated array of 
       <a href="https://msdn.microsoft.com/3e244e6c-0731-477a-b1d3-2601c29449ca">OVERLAPPED_ENTRY</a> structures.

On output, receives an array of <a href="https://msdn.microsoft.com/3e244e6c-0731-477a-b1d3-2601c29449ca">OVERLAPPED_ENTRY</a> 
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


### -param fAlertable [in]

If this parameter is <b>FALSE</b>, the function does not return until the time-out period 
       has elapsed or an entry is retrieved.

If the parameter is <b>TRUE</b> and there are no available entries, the function performs 
       an alertable wait. The thread returns when the system queues an I/O completion routine or APC to the thread and 
       the thread executes the function.

A completion routine is queued when the <a href="https://msdn.microsoft.com/6c1a4de1-6cae-4c35-bfba-0bc252fadbd9">ReadFileEx</a> or 
       <a href="https://msdn.microsoft.com/6995c4ee-ba91-41d5-b72d-19dc2eb95945">WriteFileEx</a> function in which it was specified has 
       completed, and the calling thread is the thread that initiated the operation. An APC is queued when you call 
       <a href="https://msdn.microsoft.com/5b141372-7c95-4eb2-987b-64fdf7d0783d">QueueUserAPC</a>.


## -returns



Returns nonzero (<b>TRUE</b>) if successful or zero (<b>FALSE</b>) otherwise.

To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function associates a thread with the specified completion port. A thread can be associated with at most 
     one completion port.

This function returns <b>TRUE</b> when at least one pending I/O is completed, but it is 
     possible that one or more I/O operations failed. Note that it is up to the user of this function to check the 
     list of returned entries in the <i>lpCompletionPortEntries</i> parameter to determine which of 
     them correspond to any possible failed I/O operations by looking at the status contained in the 
     <b>lpOverlapped</b> member in each 
     <a href="https://msdn.microsoft.com/3e244e6c-0731-477a-b1d3-2601c29449ca">OVERLAPPED_ENTRY</a>.

This function returns <b>FALSE</b> when no I/O operation was dequeued. This typically means 
     that an error occurred while processing the parameters to this call, or that the 
     <i>CompletionPort</i> handle was closed or is otherwise invalid. The 
     <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function provides extended error 
     information.

If a call to <a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatusEx</a> 
     fails because the handle associated with it is closed, the function returns <b>FALSE</b> and 
     <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> will return 
     <b>ERROR_ABANDONED_WAIT_0</b>.

Server applications may have several threads calling the 
     <b>GetQueuedCompletionStatusEx</b> function 
     for the same completion port.  As I/O operations complete, they are queued to this port in first-in-first-out 
     order. If a thread is actively waiting on this call, one or more queued requests complete the call for that 
     thread only.

For more information on I/O completion port theory, usage, and associated functions, see 
     <a href="https://msdn.microsoft.com/213c48e8-bb21-43ed-9c00-2a5cf8ac25f0">I/O Completion Ports</a>.

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




<a href="https://msdn.microsoft.com/50f6680f-900e-4411-a849-ec9a911c9e32">ConnectNamedPipe</a>



<a href="https://msdn.microsoft.com/40cb47fc-7b15-47f6-bee2-2611d4686053">CreateIoCompletionPort</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<b>Functions</b>



<a href="https://msdn.microsoft.com/3996c02c-562c-4697-a091-e241ad54b239">GetQueuedCompletionStatusEx</a>



<a href="https://msdn.microsoft.com/213c48e8-bb21-43ed-9c00-2a5cf8ac25f0">I/O Completion Ports</a>



<a href="https://msdn.microsoft.com/30931ed0-495c-4b50-964a-c507d4ebc2be">LockFileEx</a>



<b>Overview Topics</b>



<a href="https://msdn.microsoft.com/69a9b1e5-2d40-42de-a14a-f7b6f29bf571">PostQueuedCompletionStatus</a>



<a href="https://msdn.microsoft.com/4ad4580d-c002-44a4-a5f6-757e83ed8732">ReadFile</a>



<a href="https://msdn.microsoft.com/79afcb18-babb-453e-8618-81b43ecb24c4">TransactNamedPipe</a>



<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>



<a href="https://msdn.microsoft.com/79e955c0-8756-4d6f-bce6-49e8e44d0d3f">WaitCommEvent</a>



<a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a>
 

 

