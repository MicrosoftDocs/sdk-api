---
UID: NF:fileapi.ReadFileEx
title: ReadFileEx function (fileapi.h)
description: Reads data from the specified file or input/output (I/O) device. It reports its completion status asynchronously, calling the specified completion routine when reading is completed or canceled and the calling thread is in an alertable wait state.
helpviewer_keywords: ["ReadFileEx","ReadFileEx function [Files]","_win32_readfileex","base.readfileex","fileapi/ReadFileEx","fs.readfileex","winbase/ReadFileEx"]
old-location: fs\readfileex.htm
tech.root: fs
ms.assetid: 6c1a4de1-6cae-4c35-bfba-0bc252fadbd9
ms.date: 12/05/2018
ms.keywords: ReadFileEx, ReadFileEx function [Files], _win32_readfileex, base.readfileex, fileapi/ReadFileEx, fs.readfileex, winbase/ReadFileEx
req.header: fileapi.h
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
 - ReadFileEx
 - fileapi/ReadFileEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-file-l1-2-5.dll
 - api-ms-win-core-file-l1-2-4.dll
 - api-ms-win-core-file-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-File-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-0.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - ReadFileEx
---

# ReadFileEx function


## -description

Reads data from the specified file or input/output (I/O) device. It reports its completion status 
    asynchronously, calling the specified completion routine when reading is completed or canceled and the calling 
    thread is in an alertable wait state.

To read data from a file or device synchronously, use the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a> function.

## -parameters

### -param hFile [in]

A handle to the file or I/O device (for example, a file, file stream, physical disk, volume, console buffer, 
       tape drive, socket, communications resource, mailslot, or pipe).

This parameter can be any handle opened with the <b>FILE_FLAG_OVERLAPPED</b> flag by the 
       <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function, or a socket handle returned by the 
       <a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a> or 
       <a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a> function.

This handle also must have the <b>GENERIC_READ</b> access right. For more information on 
       access rights, see 
       <a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

### -param lpBuffer [out, optional]

A pointer to a buffer that receives the data read from the file or device.

This buffer must remain valid for the duration of the read operation. The application should not use this 
       buffer until the read operation is completed.

### -param nNumberOfBytesToRead [in]

The number of bytes to be read.

### -param lpOverlapped [in, out]

A pointer to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> data structure that 
       supplies data to be used during the asynchronous (overlapped) file read operation.

For files that support byte offsets, you must specify a byte offset at which to start reading from the file. 
       You specify this offset by setting the <b>Offset</b> and 
       <b>OffsetHigh</b> members of the 
       <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. For files or devices that do not 
       support byte offsets, <b>Offset</b> and <b>OffsetHigh</b> are 
       ignored.

The <b>ReadFileEx</b> function ignores the 
       <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure's 
       <b>hEvent</b> member. An application is free to use that member for its own purposes in the 
       context of a <b>ReadFileEx</b> call. 
       <b>ReadFileEx</b> signals completion of its read operation by 
       calling, or queuing a call to, the completion routine pointed to by 
       <i>lpCompletionRoutine</i>, so it does not need an event handle.

The <b>ReadFileEx</b> function does use the 
       <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure's 
       <b>Internal</b> and <b>InternalHigh</b> members. An application should 
       not set these members.

The <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> data structure must remain valid for 
       the duration of the read operation. It should not be a variable that can go out of scope while the read 
       operation is pending completion.

### -param lpCompletionRoutine [in]

A pointer to the completion routine to be called when the read operation is complete and the calling thread 
      is in an alertable wait state. For more information about the completion routine, see 
      <a href="/windows/desktop/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine">FileIOCompletionRoutine</a>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If the function succeeds, the calling thread has an asynchronous I/O operation pending: the overlapped read 
       operation from the file. When this I/O operation completes, and the calling thread is blocked in an alertable 
       wait state, the system calls the function pointed to by <i>lpCompletionRoutine</i>, and the 
       wait state completes with a return code of <b>WAIT_IO_COMPLETION</b>.

If the function succeeds, and the file reading operation completes, but the calling thread is not in an 
       alertable wait state, the system queues the completion routine call, holding the call until the calling thread 
       enters an alertable wait state. For information about alertable waits and overlapped input/output operations, 
       see <a href="/windows/desktop/Sync/about-synchronization">About Synchronization</a>.

## -remarks

When using <b>ReadFileEx</b> you should check 
    <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> even when the function returns "success" to 
    check for conditions that are "successes" but have some outcome you might want to know about. For example, a 
    buffer overflow when calling <b>ReadFileEx</b> will return 
    <b>TRUE</b>, but <b>GetLastError</b> will 
    report the overflow with <b>ERROR_MORE_DATA</b>. If the function call is successful and there 
    are no warning conditions, <b>GetLastError</b> will return 
    <b>ERROR_SUCCESS</b>.

The <b>ReadFileEx</b> function may fail if there are too many 
    outstanding asynchronous I/O requests. In the event of such a failure, 
    <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> can return 
    <b>ERROR_INVALID_USER_BUFFER</b> or <b>ERROR_NOT_ENOUGH_MEMORY</b>.

To cancel all pending asynchronous I/O operations, use either:

<ul>
<li>
<a href="/windows/desktop/FileIO/cancelio">CancelIo</a>—this function only cancels 
      operations issued by the calling thread for the specified file handle.</li>
<li>
<a href="/windows/desktop/FileIO/cancelioex-func">CancelIoEx</a>—this function 
      cancels all operations issued by the threads for the specified file handle.</li>
</ul>
Use <a href="/windows/desktop/FileIO/cancelsynchronousio-func">CancelSynchronousIo</a> to cancel pending 
     synchronous I/O operations.

I/O operations that are canceled complete with the error <b>ERROR_OPERATION_ABORTED</b>.

If part of the file specified by <i>hFile</i> is locked by another process, and the read 
    operation specified in a call to <b>ReadFileEx</b> overlaps the 
    locked portion, the call to <b>ReadFileEx</b> fails.

When attempting to read data from a mailslot whose buffer is too small, 
    <b>ReadFileEx</b> returns <b>FALSE</b>, and 
    <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns 
    <b>ERROR_INSUFFICIENT_BUFFER</b>.

Accessing the input buffer while a read operation is using the buffer may lead to corruption of the data read 
    into that buffer. Applications must not read from, write to, reallocate, or free the input buffer that a read 
    operation is using until the read operation completes.

If a read operation on a file begins at or beyond the end of the file, then the read operation fails with the error **ERROR_HANDLE_EOF**. If a read operation on a file begins before the end of the file, but the read operation extends past the end of the file, then the read operation succeeds, and the number of bytes read is the number of bytes that were read before the end of file was reached.

An application uses the 
    <a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex">MsgWaitForMultipleObjectsEx</a>, 
    <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex">WaitForSingleObjectEx</a>, 
    <a href="/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex">WaitForMultipleObjectsEx</a>, and 
    <a href="/windows/desktop/api/synchapi/nf-synchapi-sleepex">SleepEx</a> functions to enter an alertable wait state. For more 
    information about alertable waits and overlapped input/output, see 
    <a href="/windows/desktop/Sync/about-synchronization">About Synchronization</a>.

There are strict requirements for successfully working with files opened with 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> using 
    <b>FILE_FLAG_NO_BUFFERING</b>. For details see 
    <a href="/windows/desktop/FileIO/file-buffering">File Buffering</a>.

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
 

<h3><a id="Transacted_Operations"></a><a id="transacted_operations"></a><a id="TRANSACTED_OPERATIONS"></a>Transacted Operations</h3>
If there is a transaction bound to the file handle, then the function returns data from the transacted view of 
      the file. A transacted read handle is guaranteed to show the same view of a file for the duration of the handle. 
      For additional information, see 
      <a href="/windows/desktop/FileIO/about-transactional-ntfs">About Transactional NTFS</a>.


#### Examples

For an example, see 
    <a href="/windows/desktop/ipc/named-pipe-server-using-completion-routines">Named Pipe Server Using Completion Routines</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/FileIO/cancelio">CancelIo</a>



<a href="/windows/desktop/FileIO/cancelioex-func">CancelIoEx</a>



<a href="/windows/desktop/FileIO/cancelsynchronousio-func">CancelSynchronousIo</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine">FileIOCompletionRoutine</a>



<a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex">MsgWaitForMultipleObjectsEx</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode">SetErrorMode</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-sleepex">SleepEx</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex">WaitForMultipleObjectsEx</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex">WaitForSingleObjectEx</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefileex">WriteFileEx</a>