---
UID: NF:ioapiset.GetOverlappedResultEx
title: GetOverlappedResultEx function (ioapiset.h)
description: Retrieves the results of an overlapped operation on the specified file, named pipe, or communications device within the specified time-out interval. The calling thread can perform an alertable wait.
helpviewer_keywords: ["GetOverlappedResultEx","GetOverlappedResultEx function","base.getoverlappedresultex","ioapiset/GetOverlappedResultEx"]
old-location: base\getoverlappedresultex.htm
tech.root: backup
ms.assetid: 2f77f7fe-bdde-4c52-8571-fe0ab533aa7f
ms.date: 12/05/2018
ms.keywords: GetOverlappedResultEx, GetOverlappedResultEx function, base.getoverlappedresultex, ioapiset/GetOverlappedResultEx
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetOverlappedResultEx
 - ioapiset/GetOverlappedResultEx
dev_langs:
 - c++
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
---

# GetOverlappedResultEx function


## -description

Retrieves the results of an overlapped operation on the specified file, named pipe, or communications device within the  specified time-out interval.  The calling thread can perform an alertable wait.

## -parameters

### -param hFile [in]

A handle to the file, named pipe, or communications device. This is the same handle that was specified when the overlapped operation was started by a call to the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a>, 
<a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a>, 
<a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe">ConnectNamedPipe</a>, 
<a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe">TransactNamedPipe</a>, 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>, or 
<a href="/windows/desktop/api/winbase/nf-winbase-waitcommevent">WaitCommEvent</a> function.

### -param lpOverlapped [in]

A pointer to an 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure that was specified when the overlapped operation was started.

### -param lpNumberOfBytesTransferred [out]

A pointer to a variable that receives the number of bytes that were actually transferred by a read or write operation. For a 
<a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe">TransactNamedPipe</a> operation, this is the number of bytes that were read from the pipe. For a 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> operation, this is the number of bytes of output data returned by the device driver. For a 
<a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe">ConnectNamedPipe</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-waitcommevent">WaitCommEvent</a> operation, this value is undefined.

### -param dwMilliseconds [in]

The time-out interval, in milliseconds. 

If <i>dwMilliseconds</i> is zero and the operation is still in progress, the function  returns immediately and the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns <b>ERROR_IO_INCOMPLETE</b>.

If <i>dwMilliseconds</i> is nonzero and the operation is still in progress, the function waits until the object is signaled, an I/O completion routine or APC is queued, or the interval elapses before returning. Use <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to get extended error information.

If <i>dwMilliseconds</i> is <b>INFINITE</b>, the function returns only when the object is signaled or an I/O completion routine or APC is queued.

The <i>dwMilliseconds</i> value does not include time spent in low-power states. For example, the timeout does not continue counting down while the computer is asleep.

### -param bAlertable [in]

If this parameter is <b>TRUE</b> and the calling thread is in the waiting state, the function returns when the system queues an I/O completion routine or APC. The calling thread then runs the routine or function. Otherwise, the function does not return, and the completion routine or APC function is not executed.



A completion routine is queued when the <a href="/windows/desktop/api/fileapi/nf-fileapi-readfileex">ReadFileEx</a> or <a href="/windows/desktop/api/fileapi/nf-fileapi-writefileex">WriteFileEx</a> function in which it was specified has completed. The function returns and the completion routine is called only if <i>bAlertable</i> is <b>TRUE</b>, and the calling thread is the thread that initiated the read or write operation. An APC is queued when you call <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc">QueueUserAPC</a>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Common error codes include the following:

<ul>
<li>If <i>dwMilliseconds</i> is zero and the operation is still in progress,  <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_IO_INCOMPLETE</b>.</li>
<li>If <i>dwMilliseconds</i> is nonzero, and an I/O completion routine or APC is queued, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>WAIT_IO_COMPLETION</b>. </li>
<li>If <i>dwMilliseconds</i> is nonzero and the specified timeout interval elapses, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>WAIT_TIMEOUT</b>. </li>
</ul>

## -remarks

The <b>GetOverlappedResultEx</b> function differs from <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> in the following ways: The <i>dwMilliseconds</i> parameter can specify a timeout interval for the operation, and the <i>bAlertable</i> parameter can specify that the calling thread should perform an alertable wait. 

The results reported by the 
<b>GetOverlappedResultEx</b> function are those of the specified handle's last overlapped operation to which the specified 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure was provided, and for which the operation's results were pending. A pending operation is indicated when the function that started the operation returns FALSE, and the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns <b>ERROR_IO_PENDING</b>. When an I/O operation is pending, the function that started the operation resets the <b>hEvent</b> member of the 
<b>OVERLAPPED</b> structure to the nonsignaled state. Then when the pending operation has been completed, the system sets the event object to the signaled state.

Specify a manual-reset event object in the 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. If an auto-reset event object is used, the event handle must not be specified in any other wait operation in the interval between starting the overlapped operation and the call to 
<b>GetOverlappedResultEx</b>. For example, the event object is sometimes specified in one of the wait functions to wait for the operation's completion. When the wait function returns, the system sets an auto-reset event's state to nonsignaled, and a subsequent call to 
<b>GetOverlappedResultEx</b> with the <i>dwMilliseconds</i> parameter set to <b>INFINITE</b> causes the function to be blocked indefinitely.

If the <b>hEvent</b> member of the 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure is <b>NULL</b>, the system uses the state of the <i>hFile</i> handle to signal when the operation has been completed. Use of file, named pipe, or communications-device handles for this purpose is discouraged. It is safer to use an event object because of the confusion that can occur when multiple simultaneous overlapped operations are performed on the same file, named pipe, or communications device. In this situation, there is no way to know which operation caused the object's state to be signaled.

## -see-also

<a href="/windows/desktop/FileIO/cancelio">CancelIo</a>



<a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe">ConnectNamedPipe</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/desktop/Sync/synchronization-and-overlapped-input-and-output">Overlapped Input and Output</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>



<a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe">TransactNamedPipe</a>



<a href="/windows/desktop/api/winbase/nf-winbase-waitcommevent">WaitCommEvent</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a>
