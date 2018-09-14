---
UID: NF:fileapi.ReadFileEx
title: ReadFileEx function
author: windows-sdk-content
description: Reads data from the specified file or input/output (I/O) device. It reports its completion status asynchronously, calling the specified completion routine when reading is completed or canceled and the calling thread is in an alertable wait state.
old-location: fs\readfileex.htm
tech.root: FileIO
ms.assetid: 6c1a4de1-6cae-4c35-bfba-0bc252fadbd9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ReadFileEx, ReadFileEx function [Files], _win32_readfileex, base.readfileex, fileapi/ReadFileEx, fs.readfileex, winbase/ReadFileEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ReadFileEx function


## -description


Reads data from the specified file or input/output (I/O) device. It reports its completion status 
    asynchronously, calling the specified completion routine when reading is completed or canceled and the calling 
    thread is in an alertable wait state.

To read data from a file or device synchronously, use the 
    <a href="https://msdn.microsoft.com/4ad4580d-c002-44a4-a5f6-757e83ed8732">ReadFile</a> function.


## -parameters




### -param hFile [in]

A handle to the file or I/O device (for example, a file, file stream, physical disk, volume, console buffer, 
       tape drive, socket, communications resource, mailslot, or pipe).

This parameter can be any handle opened with the <b>FILE_FLAG_OVERLAPPED</b> flag by the 
       <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function, or a socket handle returned by the 
       <a href="https://msdn.microsoft.com/6bf6e6c4-6268-479c-86a6-52e90cf317db">socket</a> or 
       <a href="https://msdn.microsoft.com/72246263-4806-4ab2-9b26-89a1782a954b">accept</a> function.

This handle also must have the <b>GENERIC_READ</b> access right. For more information on 
       access rights, see 
       <a href="https://msdn.microsoft.com/991d7d94-fae7-406f-b2e3-dee811279366">File Security and Access Rights</a>.


### -param lpBuffer [out, optional]

A pointer to a buffer that receives the data read from the file or device.

This buffer must remain valid for the duration of the read operation. The application should not use this 
       buffer until the read operation is completed.


### -param nNumberOfBytesToRead [in]

The number of bytes to be read.


### -param lpOverlapped [in, out]

A pointer to an <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> data structure that 
       supplies data to be used during the asynchronous (overlapped) file read operation.

For files that support byte offsets, you must specify a byte offset at which to start reading from the file. 
       You specify this offset by setting the <b>Offset</b> and 
       <b>OffsetHigh</b> members of the 
       <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure. For files or devices that do not 
       support byte offsets, <b>Offset</b> and <b>OffsetHigh</b> are 
       ignored.

The <b>ReadFileEx</b> function ignores the 
       <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure's 
       <b>hEvent</b> member. An application is free to use that member for its own purposes in the 
       context of a <b>ReadFileEx</b> call. 
       <b>ReadFileEx</b> signals completion of its read operation by 
       calling, or queuing a call to, the completion routine pointed to by 
       <i>lpCompletionRoutine</i>, so it does not need an event handle.

The <b>ReadFileEx</b> function does use the 
       <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure's 
       <b>Internal</b> and <b>InternalHigh</b> members. An application should 
       not set these members.

The <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> data structure must remain valid for 
       the duration of the read operation. It should not be a variable that can go out of scope while the read 
       operation is pending completion.


### -param lpCompletionRoutine [in]

A pointer to the completion routine to be called when the read operation is complete and the calling thread 
      is in an alertable wait state. For more information about the completion routine, see 
      <a href="https://msdn.microsoft.com/574eccda-03eb-4e8a-9d74-cfaecc7312ce">FileIOCompletionRoutine</a>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If the function succeeds, the calling thread has an asynchronous I/O operation pending: the overlapped read 
       operation from the file. When this I/O operation completes, and the calling thread is blocked in an alertable 
       wait state, the system calls the function pointed to by <i>lpCompletionRoutine</i>, and the 
       wait state completes with a return code of <b>WAIT_IO_COMPLETION</b>.

If the function succeeds, and the file reading operation completes, but the calling thread is not in an 
       alertable wait state, the system queues the completion routine call, holding the call until the calling thread 
       enters an alertable wait state. For information about alertable waits and overlapped input/output operations, 
       see <a href="https://msdn.microsoft.com/0930bf12-6d5f-4f2c-914d-53e6e862d3bd">About Synchronization</a>.

If <b>ReadFileEx</b> attempts to read past the 
       end-of-file (EOF), the call to 
       <a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a> for that operation returns 
       <b>FALSE</b> and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> 
       returns <b>ERROR_HANDLE_EOF</b>.




## -remarks



When using <b>ReadFileEx</b> you should check 
    <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> even when the function returns "success" to 
    check for conditions that are "successes" but have some outcome you might want to know about. For example, a 
    buffer overflow when calling <b>ReadFileEx</b> will return 
    <b>TRUE</b>, but <b>GetLastError</b> will 
    report the overflow with <b>ERROR_MORE_DATA</b>. If the function call is successful and there 
    are no warning conditions, <b>GetLastError</b> will return 
    <b>ERROR_SUCCESS</b>.

The <b>ReadFileEx</b> function may fail if there are too many 
    outstanding asynchronous I/O requests. In the event of such a failure, 
    <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> can return 
    <b>ERROR_INVALID_USER_BUFFER</b> or <b>ERROR_NOT_ENOUGH_MEMORY</b>.

To cancel all pending asynchronous I/O operations, use either:

<ul>
<li>
<a href="https://msdn.microsoft.com/b28162dc-0da8-41c6-9901-29381d2d72c4">CancelIo</a>—this function only cancels 
      operations issued by the calling thread for the specified file handle.</li>
<li>
<a href="https://msdn.microsoft.com/a2ce13b8-7da6-4848-848d-901d9667c2e3">CancelIoEx</a>—this function 
      cancels all operations issued by the threads for the specified file handle.</li>
</ul>
Use <a href="https://msdn.microsoft.com/f362c8b2-2193-443e-bb69-78f8b4147117">CancelSynchronousIo</a> to cancel pending 
     synchronous I/O operations.

I/O operations that are canceled complete with the error <b>ERROR_OPERATION_ABORTED</b>.

If part of the file specified by <i>hFile</i> is locked by another process, and the read 
    operation specified in a call to <b>ReadFileEx</b> overlaps the 
    locked portion, the call to <b>ReadFileEx</b> fails.

When attempting to read data from a mailslot whose buffer is too small, 
    <b>ReadFileEx</b> returns <b>FALSE</b>, and 
    <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns 
    <b>ERROR_INSUFFICIENT_BUFFER</b>.

Accessing the input buffer while a read operation is using the buffer may lead to corruption of the data read 
    into that buffer. Applications must not read from, write to, reallocate, or free the input buffer that a read 
    operation is using until the read operation completes.

An application uses the 
    <a href="https://msdn.microsoft.com/1774b721-3ad4-492e-96af-b71de9066f0c">MsgWaitForMultipleObjectsEx</a>, 
    <a href="https://msdn.microsoft.com/530b5340-f8b2-4e00-a3ca-87a7c7372482">WaitForSingleObjectEx</a>, 
    <a href="https://msdn.microsoft.com/47a167fb-4714-4353-b924-a161f367673c">WaitForMultipleObjectsEx</a>, and 
    <a href="https://msdn.microsoft.com/a73cff94-ad63-4110-9f01-6469481c3d55">SleepEx</a> functions to enter an alertable wait state. For more 
    information about alertable waits and overlapped input/output, see 
    <a href="https://msdn.microsoft.com/0930bf12-6d5f-4f2c-914d-53e6e862d3bd">About Synchronization</a>.

There are strict requirements for successfully working with files opened with 
    <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> using 
    <b>FILE_FLAG_NO_BUFFERING</b>. For details see 
    <a href="https://msdn.microsoft.com/ae1e5d0f-9b55-4aae-8402-b9c8e33d9363">File Buffering</a>.

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
      <a href="https://msdn.microsoft.com/52341315-0412-4a87-aca0-9adea7aae62f">About Transactional NTFS</a>.


#### Examples

For an example, see 
    <a href="https://msdn.microsoft.com/8b73485c-c6f7-44df-9e53-308df2c752e7">Named Pipe Server Using Completion Routines</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/b28162dc-0da8-41c6-9901-29381d2d72c4">CancelIo</a>



<a href="https://msdn.microsoft.com/a2ce13b8-7da6-4848-848d-901d9667c2e3">CancelIoEx</a>



<a href="https://msdn.microsoft.com/f362c8b2-2193-443e-bb69-78f8b4147117">CancelSynchronousIo</a>



<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/574eccda-03eb-4e8a-9d74-cfaecc7312ce">FileIOCompletionRoutine</a>



<a href="https://msdn.microsoft.com/1774b721-3ad4-492e-96af-b71de9066f0c">MsgWaitForMultipleObjectsEx</a>



<a href="https://msdn.microsoft.com/4ad4580d-c002-44a4-a5f6-757e83ed8732">ReadFile</a>



<a href="https://msdn.microsoft.com/b88f5577-9124-433c-a7e8-a7f713b7b27d">SetErrorMode</a>



<a href="https://msdn.microsoft.com/a73cff94-ad63-4110-9f01-6469481c3d55">SleepEx</a>



<a href="https://msdn.microsoft.com/47a167fb-4714-4353-b924-a161f367673c">WaitForMultipleObjectsEx</a>



<a href="https://msdn.microsoft.com/530b5340-f8b2-4e00-a3ca-87a7c7372482">WaitForSingleObjectEx</a>



<a href="https://msdn.microsoft.com/6995c4ee-ba91-41d5-b72d-19dc2eb95945">WriteFileEx</a>
 

 

