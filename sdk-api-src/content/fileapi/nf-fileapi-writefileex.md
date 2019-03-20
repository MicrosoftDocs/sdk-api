---
UID: NF:fileapi.WriteFileEx
title: WriteFileEx function (fileapi.h)
author: windows-sdk-content
description: Writes data to the specified file or input/output (I/O) device. It reports its completion status asynchronously, calling the specified completion routine when writing is completed or canceled and the calling thread is in an alertable wait state.
old-location: fs\writefileex.htm
tech.root: FileIO
ms.assetid: 6995c4ee-ba91-41d5-b72d-19dc2eb95945
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WriteFileEx, WriteFileEx function [Files], _win32_writefileex, base.writefileex, fileapi/WriteFileEx, fs.writefileex, winbase/WriteFileEx
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
 - WriteFileEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WriteFileEx function


## -description


Writes data to the specified file or input/output (I/O) device. It reports its completion status asynchronously, calling the specified completion routine when writing is completed or canceled and the calling thread is in an alertable wait state.

To write data to a file or device synchronously, use the <a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a> function.


## -parameters




### -param hFile [in]

A handle to the file or I/O device (for example, a file, file stream, physical disk, volume,  console buffer, tape drive, 
    socket, communications resource, mailslot, or  pipe). 
       

This parameter can be any handle opened with the <b>FILE_FLAG_OVERLAPPED</b> flag by the 
        <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function, or a socket handle returned by the 
        <a href="https://msdn.microsoft.com/6bf6e6c4-6268-479c-86a6-52e90cf317db">socket</a> or 
        <a href="https://msdn.microsoft.com/72246263-4806-4ab2-9b26-89a1782a954b">accept</a> function. 

Do not associate an I/O completion port with this handle. For more information, see the Remarks section.

This handle also must have the <b>GENERIC_WRITE</b> access 
      right. For more information on access rights, see 
      <a href="https://msdn.microsoft.com/991d7d94-fae7-406f-b2e3-dee811279366">File Security and Access Rights</a>.


### -param lpBuffer [in, optional]

A pointer to the buffer containing the data to be written to the file or device.
     

This buffer must remain valid for the duration of the write operation. The caller must not use this buffer 
      until the write operation is completed.


### -param nNumberOfBytesToWrite [in]

The number of bytes to be written to the file or device.
      

A value of zero specifies a null write operation. The behavior of a null write operation depends on the 
       underlying file system.

Pipe write operations across a network are limited to 65,535 bytes per write. For more information regarding  pipes, see the Remarks section.


### -param lpOverlapped [in, out]

A pointer to an <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> data structure that 
      supplies data to be used during the overlapped (asynchronous) write operation.
      

For files that support byte offsets, you must specify a byte offset at which to start writing to the file. 
       You specify this offset by setting the <b>Offset</b> and 
       <b>OffsetHigh</b> members of the 
       <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure. For files or devices that do not support 
       byte offsets, <b>Offset</b> and <b>OffsetHigh</b> are ignored.

To write to the end of file, specify both the <b>Offset</b> and <b>OffsetHigh</b> members of the <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure as 0xFFFFFFFF. This is functionally equivalent to previously calling the <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function to open <i>hFile</i> using <b>FILE_APPEND_DATA</b> access.

The <b>WriteFileEx</b> function ignores the 
       <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure's 
       <b>hEvent</b> member. An application is free to use that member for its own purposes in the 
       context of a <b>WriteFileEx</b> call. 
       <b>WriteFileEx</b> signals completion of its writing operation 
       by calling, or queuing a call to, the completion routine pointed to by 
       <i>lpCompletionRoutine</i>, so it does not need an event handle.

The <b>WriteFileEx</b> function does use the 
       <b>Internal</b> and <b>InternalHigh</b> members of the 
       <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure. You should not change the value 
       of these members.

The <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> data structure must remain valid for 
       the duration of the write operation. It should not be a variable that can go out of scope while the write 
       operation is pending completion.


### -param lpCompletionRoutine [in]

A pointer to a completion routine to be called when the write operation has been completed and the calling 
      thread is in an alertable wait state. For more information about this completion routine, see 
      <a href="https://msdn.microsoft.com/574eccda-03eb-4e8a-9d74-cfaecc7312ce">FileIOCompletionRoutine</a>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If the <b>WriteFileEx</b> function succeeds, the calling 
       thread has an asynchronous I/O operation pending: the overlapped write operation to the file. 
       When this I/O operation finishes, and the calling thread is blocked in an alertable wait state, the 
       operating system calls the function pointed to by <i>lpCompletionRoutine</i>, and the wait 
       completes with a return code of <b>WAIT_IO_COMPLETION</b>.

If the function succeeds and the file-writing operation finishes, but the calling thread is not in an 
       alertable wait state, the system queues the call to *<i>lpCompletionRoutine</i>, holding the 
       call until the calling thread enters an alertable wait state. For more information about 
       alertable wait states and overlapped input/output operations, see <a href="https://msdn.microsoft.com/0930bf12-6d5f-4f2c-914d-53e6e862d3bd">About Synchronization</a>.




## -remarks



When using <b>WriteFileEx</b> you should check 
    <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> even when the function returns "success" to 
    check for conditions that are "successes" but have some outcome you might want to know about. For example, a 
    buffer overflow when calling <b>WriteFileEx</b> will return 
    <b>TRUE</b>, but <b>GetLastError</b> will 
    report the overflow with <b>ERROR_MORE_DATA</b>. If the function call is successful and there 
    are no warning conditions, <b>GetLastError</b> will return 
    <b>ERROR_SUCCESS</b>.

The <b>WriteFileEx</b> function will fail if the <i>hFile</i> parameter is associated with an <a href="https://msdn.microsoft.com/213c48e8-bb21-43ed-9c00-2a5cf8ac25f0">I/O completion port</a>. To perform writes using this type of handle, use the <a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a> function.

The <b>WriteFileEx</b> function may fail if there are too many outstanding asynchronous I/O requests. In the event of such a failure, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> can return <b>ERROR_INVALID_USER_BUFFER</b> or <b>ERROR_NOT_ENOUGH_MEMORY</b>.

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

I/O operations that are canceled complete with the error 
     <b>ERROR_OPERATION_ABORTED</b>.

If part of the file specified by <i>hFile</i> is locked by another process, and the specified write operation overlaps the locked 
    portion, <b>WriteFileEx</b> fails.

When writing to a file, the last write time is not fully updated until all handles used for writing have been 
    closed. Therefore, to ensure an accurate last write time, close the file handle immediately after writing to the 
    file.

Accessing the output buffer while a write operation is using the buffer may lead to corruption of the data 
    written from that buffer. Applications must not write to, reallocate, or free the output buffer that a write 
    operation is using until the write operation completes.

Note that the time stamps may not be updated correctly for a remote file. To ensure consistent results, use 
    unbuffered I/O.

The system interprets zero bytes to write as specifying a null write operation and 
<a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a> does not truncate or extend the file. To truncate or extend a file, use the 
<a href="https://msdn.microsoft.com/2a579609-144a-4b77-8605-87aecf1f0957">SetEndOfFile</a> function.

An application uses the 
    <a href="https://msdn.microsoft.com/530b5340-f8b2-4e00-a3ca-87a7c7372482">WaitForSingleObjectEx</a>, 
    <a href="https://msdn.microsoft.com/47a167fb-4714-4353-b924-a161f367673c">WaitForMultipleObjectsEx</a>, 
    <a href="https://msdn.microsoft.com/1774b721-3ad4-492e-96af-b71de9066f0c">MsgWaitForMultipleObjectsEx</a>, 
    <a href="https://msdn.microsoft.com/en-us/library/ms686293(v=VS.85).aspx">SignalObjectAndWait</a>, and 
    <a href="https://msdn.microsoft.com/a73cff94-ad63-4110-9f01-6469481c3d55">SleepEx</a> functions to enter an alertable wait state. For more information about alertable wait 
    states and overlapped I/O operations, see <a href="https://msdn.microsoft.com/0930bf12-6d5f-4f2c-914d-53e6e862d3bd">About Synchronization</a>.

If you write directly to a volume that has a mounted file system, you must first obtain exclusive access to the volume. Otherwise, you risk causing data corruption or system instability, because your application's writes may conflict with other changes coming from the file system and leave the contents of the volume in an inconsistent state. To prevent these problems, the following changes have been made in Windows Vista and later:

<ul>
<li>A write on a volume handle will succeed if the volume does not have a mounted file system, or if one of the following conditions is true:<ul>
<li>The sectors to be written to are boot sectors.</li>
<li>The sectors to be written to reside outside of file system space.</li>
<li>You have explicitly locked or dismounted the volume by using <a href="https://msdn.microsoft.com/b59b5c5e-6719-47a8-8810-14b60204e5ed">FSCTL_LOCK_VOLUME</a> or <a href="https://msdn.microsoft.com/8828760c-9635-4c69-9867-c2f5314841e6">FSCTL_DISMOUNT_VOLUME</a>.</li>
<li>The volume has no actual file system. (In other words, it has a RAW file system mounted.)</li>
</ul>
</li>
<li>A write on a disk handle will succeed if one of the following conditions is true:<ul>
<li>The sectors to be written to do not fall within a volume's extents.</li>
<li>The sectors to be written to fall within a mounted volume, but you have explicitly locked or dismounted the volume by using <a href="https://msdn.microsoft.com/b59b5c5e-6719-47a8-8810-14b60204e5ed">FSCTL_LOCK_VOLUME</a> or <a href="https://msdn.microsoft.com/8828760c-9635-4c69-9867-c2f5314841e6">FSCTL_DISMOUNT_VOLUME</a>.</li>
<li>The sectors to be written to fall within a volume that has no mounted file system other than RAW.</li>
</ul>
</li>
</ul>
There are strict requirements for successfully working with files opened with <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> using <b>FILE_FLAG_NO_BUFFERING</b>. For details see <a href="https://msdn.microsoft.com/ae1e5d0f-9b55-4aae-8402-b9c8e33d9363">File Buffering</a>.

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
If there is a transaction bound to the file handle, then the file write is transacted. For more information, see <a href="https://msdn.microsoft.com/52341315-0412-4a87-aca0-9adea7aae62f">About Transactional NTFS</a>.


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



<a href="https://msdn.microsoft.com/6c1a4de1-6cae-4c35-bfba-0bc252fadbd9">ReadFileEx</a>



<a href="https://msdn.microsoft.com/2a579609-144a-4b77-8605-87aecf1f0957">SetEndOfFile</a>



<a href="https://msdn.microsoft.com/b88f5577-9124-433c-a7e8-a7f713b7b27d">SetErrorMode</a>



<a href="https://msdn.microsoft.com/en-us/library/ms686293(v=VS.85).aspx">SignalObjectAndWait</a>



<a href="https://msdn.microsoft.com/a73cff94-ad63-4110-9f01-6469481c3d55">SleepEx</a>



<a href="https://msdn.microsoft.com/47a167fb-4714-4353-b924-a161f367673c">WaitForMultipleObjectsEx</a>



<a href="https://msdn.microsoft.com/530b5340-f8b2-4e00-a3ca-87a7c7372482">WaitForSingleObjectEx</a>



<a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a>
 

 

