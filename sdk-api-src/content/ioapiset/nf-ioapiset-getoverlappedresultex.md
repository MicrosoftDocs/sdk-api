---
UID: NF:ioapiset.GetOverlappedResultEx
title: GetOverlappedResultEx function (ioapiset.h)
author: windows-sdk-content
description: Retrieves the results of an overlapped operation on the specified file, named pipe, or communications device within the specified time-out interval. The calling thread can perform an alertable wait.
old-location: base\getoverlappedresultex.htm
tech.root: Sync
ms.assetid: 2f77f7fe-bdde-4c52-8571-fe0ab533aa7f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetOverlappedResultEx, GetOverlappedResultEx function, base.getoverlappedresultex, ioapiset/GetOverlappedResultEx
ms.topic: function
req.header: ioapiset.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - API-MS-Win-Core-io-l1-1-1.dll
 - KernelBase.dll
 - MinKernelBase.dll
api_name:
 - GetOverlappedResultEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetOverlappedResultEx function


## -description


Retrieves the results of an overlapped operation on the specified file, named pipe, or communications device within the  specified time-out interval.  The calling thread can perform an alertable wait.


## -parameters




### -param hFile [in]

A handle to the file, named pipe, or communications device. This is the same handle that was specified when the overlapped operation was started by a call to the 
<a href="https://msdn.microsoft.com/en-us/library/Aa365467(v=VS.85).aspx">ReadFile</a>, 
<a href="https://msdn.microsoft.com/en-us/library/Aa365747(v=VS.85).aspx">WriteFile</a>, 
<a href="https://msdn.microsoft.com/50f6680f-900e-4411-a849-ec9a911c9e32">ConnectNamedPipe</a>, 
<a href="https://msdn.microsoft.com/79afcb18-babb-453e-8618-81b43ecb24c4">TransactNamedPipe</a>, 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>, or 
<a href="https://msdn.microsoft.com/79e955c0-8756-4d6f-bce6-49e8e44d0d3f">WaitCommEvent</a> function.


### -param lpOverlapped [in]

A pointer to an 
<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure that was specified when the overlapped operation was started.


### -param lpNumberOfBytesTransferred [out]

A pointer to a variable that receives the number of bytes that were actually transferred by a read or write operation. For a 
<a href="https://msdn.microsoft.com/79afcb18-babb-453e-8618-81b43ecb24c4">TransactNamedPipe</a> operation, this is the number of bytes that were read from the pipe. For a 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> operation, this is the number of bytes of output data returned by the device driver. For a 
<a href="https://msdn.microsoft.com/50f6680f-900e-4411-a849-ec9a911c9e32">ConnectNamedPipe</a> or 
<a href="https://msdn.microsoft.com/79e955c0-8756-4d6f-bce6-49e8e44d0d3f">WaitCommEvent</a> operation, this value is undefined.


### -param dwMilliseconds [in]

The time-out interval, in milliseconds. 

If <i>dwMilliseconds</i> is zero and the operation is still in progress, the function  returns immediately and the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function returns <b>ERROR_IO_INCOMPLETE</b>.

If <i>dwMilliseconds</i> is nonzero and the operation is still in progress, the function waits until the object is signaled, an I/O completion routine or APC is queued, or the interval elapses before returning. Use <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to get extended error information.

If <i>dwMilliseconds</i> is <b>INFINITE</b>, the function returns only when the object is signaled or an I/O completion routine or APC is queued.




### -param bAlertable [in]

If this parameter is <b>TRUE</b> and the calling thread is in the waiting state, the function returns when the system queues an I/O completion routine or APC. The calling thread then runs the routine or function. Otherwise, the function does not return, and the completion routine or APC function is not executed.



A completion routine is queued when the <a href="https://msdn.microsoft.com/6c1a4de1-6cae-4c35-bfba-0bc252fadbd9">ReadFileEx</a> or <a href="https://msdn.microsoft.com/6995c4ee-ba91-41d5-b72d-19dc2eb95945">WriteFileEx</a> function in which it was specified has completed. The function returns and the completion routine is called only if <i>bAlertable</i> is <b>TRUE</b>, and the calling thread is the thread that initiated the read or write operation. An APC is queued when you call <a href="https://msdn.microsoft.com/5b141372-7c95-4eb2-987b-64fdf7d0783d">QueueUserAPC</a>.




## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Common error codes include the following:

<ul>
<li>If <i>dwMilliseconds</i> is zero and the operation is still in progress,  <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_IO_INCOMPLETE</b>.</li>
<li>If <i>dwMilliseconds</i> is nonzero, and an I/O completion routine or APC is queued, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>WAIT_IO_COMPLETION</b>. </li>
<li>If <i>dwMilliseconds</i> is nonzero and the specified timeout interval elapses, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>WAIT_TIMEOUT</b>. </li>
</ul>



## -remarks



The <b>GetOverlappedResultEx</b> function differs from <a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a> in the following ways: The <i>dwMilliseconds</i> parameter can specify a timeout interval for the operation, and the <i>bAlertable</i> parameter can specify that the calling thread should perform an alertable wait. 

The results reported by the 
<b>GetOverlappedResultEx</b> function are those of the specified handle's last overlapped operation to which the specified 
<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure was provided, and for which the operation's results were pending. A pending operation is indicated when the function that started the operation returns FALSE, and the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function returns <b>ERROR_IO_PENDING</b>. When an I/O operation is pending, the function that started the operation resets the <b>hEvent</b> member of the 
<b>OVERLAPPED</b> structure to the nonsignaled state. Then when the pending operation has been completed, the system sets the event object to the signaled state.

Specify a manual-reset event object in the 
<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure. If an auto-reset event object is used, the event handle must not be specified in any other wait operation in the interval between starting the overlapped operation and the call to 
<b>GetOverlappedResultEx</b>. For example, the event object is sometimes specified in one of the wait functions to wait for the operation's completion. When the wait function returns, the system sets an auto-reset event's state to nonsignaled, and a subsequent call to 
<b>GetOverlappedResultEx</b> with the <i>dwMilliseconds</i> parameter set to <b>INFINITE</b> causes the function to be blocked indefinitely.

If the <b>hEvent</b> member of the 
<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure is <b>NULL</b>, the system uses the state of the <i>hFile</i> handle to signal when the operation has been completed. Use of file, named pipe, or communications-device handles for this purpose is discouraged. It is safer to use an event object because of the confusion that can occur when multiple simultaneous overlapped operations are performed on the same file, named pipe, or communications device. In this situation, there is no way to know which operation caused the object's state to be signaled.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa363791(v=VS.85).aspx">CancelIo</a>



<a href="https://msdn.microsoft.com/50f6680f-900e-4411-a849-ec9a911c9e32">ConnectNamedPipe</a>



<a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>



<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>



<a href="https://msdn.microsoft.com/db44990e-5a0f-4153-8ff6-79dd7cda48af">Overlapped Input and Output</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa365467(v=VS.85).aspx">ReadFile</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>



<a href="https://msdn.microsoft.com/79afcb18-babb-453e-8618-81b43ecb24c4">TransactNamedPipe</a>



<a href="https://msdn.microsoft.com/79e955c0-8756-4d6f-bce6-49e8e44d0d3f">WaitCommEvent</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa365747(v=VS.85).aspx">WriteFile</a>
 

 

