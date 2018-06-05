---
UID: NF:fileapi.ReadFile
title: ReadFile function
author: windows-sdk-content
description: Reads data from the specified file or input/output (I/O) device. Reads occur at the position specified by the file pointer if supported by the device.
old-location: fs\readfile.htm
old-project: FileIO
ms.assetid: 4ad4580d-c002-44a4-a5f6-757e83ed8732
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: ReadFile, ReadFile function [Files], _win32_readfile, base.readfile, fileapi/ReadFile, fs.readfile, winbase/ReadFile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: STREAM_INFO_LEVELS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-File-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-File-l1-2-0.dll
-	API-MS-Win-Core-File-l1-2-1.dll
-	API-MS-Win-Core-File-l1-2-2.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	MinKernelBase.dll
api_name:
-	ReadFile
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Internet Explorer 5
---

# ReadFile function


## -description


Reads data from the specified file or input/output (I/O) device. Reads occur at the position specified 
    by the file pointer if supported by the device.

This function is designed for both synchronous and asynchronous operations. For a similar function designed 
    solely for asynchronous operation, see <a href="https://msdn.microsoft.com/6c1a4de1-6cae-4c35-bfba-0bc252fadbd9">ReadFileEx</a>.


## -parameters




### -param hFile [in]

A handle to the device (for example, a file, file stream, physical disk, volume,  console buffer, tape drive, 
       socket, communications resource, mailslot, or  pipe).

The <i>hFile</i> parameter must have been created with read access. For more information, 
       see <a href="https://msdn.microsoft.com/e18cede9-9bf7-4866-850b-5d7fa43a5b0f">Generic Access Rights</a> and 
       <a href="https://msdn.microsoft.com/991d7d94-fae7-406f-b2e3-dee811279366">File Security and Access Rights</a>.

For asynchronous read operations, <i>hFile</i> can be any handle that is opened with the 
       <b>FILE_FLAG_OVERLAPPED</b> flag by the 
       <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function, or a socket handle returned by the 
       <a href="https://msdn.microsoft.com/6bf6e6c4-6268-479c-86a6-52e90cf317db">socket</a> or 
       <a href="https://msdn.microsoft.com/72246263-4806-4ab2-9b26-89a1782a954b">accept</a> function.


### -param lpBuffer [out]

A pointer to the buffer that receives the data read from a file or device.

This buffer must remain valid for the duration of the read operation. The caller must not use this buffer 
       until the read operation is completed.


### -param nNumberOfBytesToRead [in]

The maximum number of bytes to be read.


### -param lpNumberOfBytesRead [out, optional]

A pointer to the variable that receives the number of bytes read when using a synchronous 
       <i>hFile</i> parameter. <b>ReadFile</b> sets 
       this value to zero  before doing any work or error checking. Use <b>NULL</b> for this 
       parameter if this is an asynchronous operation to avoid potentially erroneous results.

This parameter can be <b>NULL</b> only when the <i>lpOverlapped</i> 
       parameter is not <b>NULL</b>.

For more information, see the Remarks section.


### -param lpOverlapped [in, out, optional]

A pointer to an <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure is 
       required if the <i>hFile</i> parameter was opened with 
       <b>FILE_FLAG_OVERLAPPED</b>, otherwise it can be <b>NULL</b>.

If <i>hFile</i> is opened with <b>FILE_FLAG_OVERLAPPED</b>, the 
       <i>lpOverlapped</i> parameter must point to a 
       valid and unique <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure, otherwise the 
       function can incorrectly report that the read operation is complete.

For an <i>hFile</i> that supports byte offsets, if you use this parameter you must specify 
       a byte offset at which to start reading from the file or device. This offset is specified by setting the 
       <b>Offset</b> and <b>OffsetHigh</b> members of the 
       <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure. For an 
       <i>hFile</i> that does not support byte offsets, <b>Offset</b> and 
       <b>OffsetHigh</b> are ignored.

For more information about different combinations of <i>lpOverlapped</i> and 
       <b>FILE_FLAG_OVERLAPPED</b>, see the Remarks section and the 
       <a href="https://docs.microsoft.com/">Synchronization and File Position</a> section.


## -returns



If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, or is completing asynchronously, the return value is zero 
       (<b>FALSE</b>). To get extended error information, call the 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.
       <div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> code 
        <b>ERROR_IO_PENDING</b> is not a failure; it designates the read operation is pending 
        completion asynchronously. For more information, see Remarks.</div>
<div> </div>





## -remarks



The <b>ReadFile</b> function returns when one of the following 
     conditions occur:
     <ul>
<li>The number of bytes requested is read.</li>
<li>A write operation completes on the write end of the 
       pipe.</li>
<li>An asynchronous handle is being used and the read is occurring asynchronously.</li>
<li>An error occurs.</li>
</ul>


The <b>ReadFile</b> function may fail with 
    <b>ERROR_INVALID_USER_BUFFER</b> or <b>ERROR_NOT_ENOUGH_MEMORY</b> whenever 
    there are too many outstanding asynchronous I/O requests.

To cancel all pending asynchronous I/O operations, use either:
     <ul>
<li>
<a href="https://msdn.microsoft.com/b28162dc-0da8-41c6-9901-29381d2d72c4">CancelIo</a>—this function only 
       cancels operations issued by the calling thread for the specified file handle.</li>
<li>
<a href="https://msdn.microsoft.com/a2ce13b8-7da6-4848-848d-901d9667c2e3">CancelIoEx</a>—this function 
       cancels all operations issued by the threads for the specified file handle.</li>
</ul>


Use <a href="https://msdn.microsoft.com/f362c8b2-2193-443e-bb69-78f8b4147117">CancelSynchronousIo</a> to cancel pending 
     synchronous I/O operations.

I/O operations that are canceled complete with the error <b>ERROR_OPERATION_ABORTED</b>.

The <b>ReadFile</b> function may fail with 
    <b>ERROR_NOT_ENOUGH_QUOTA</b>, which means the calling process's buffer could not be 
    page-locked. For additional information, see 
    <a href="https://msdn.microsoft.com/8bc0053c-f687-43b5-a435-df1e813a5204">SetProcessWorkingSetSize</a>.

If part of a file is locked by another process and the read operation overlaps the locked portion, this 
    function fails.

Accessing the input buffer while a read operation is using the buffer may lead to corruption of the data read 
    into that buffer. Applications must not read from, write to, reallocate, or free the input buffer that a read 
    operation is using until the read operation completes. This can be particularly problematic when using an 
    asynchronous file handle. Additional information regarding synchronous versus asynchronous file handles can be 
    found in the <a href="https://docs.microsoft.com/">Synchronization and File Position</a> section and 
    in the <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> reference topic.

Characters can be read from the console input buffer by using 
    <b>ReadFile</b> with a handle to console input. The console mode 
    determines the exact behavior of the <b>ReadFile</b> function. By 
    default, the console mode is <b>ENABLE_LINE_INPUT</b>, which indicates that 
    <b>ReadFile</b> should read until it reaches a carriage return. If you 
    press Ctrl+C, the call succeeds, but <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns 
    <b>ERROR_OPERATION_ABORTED</b>. For more information, see 
    <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>.

When reading from a communications device, the behavior of 
    <b>ReadFile</b> is determined by the current communication time-out as 
    set and retrieved by using the <a href="https://msdn.microsoft.com/71aa6ab3-d56c-43bc-9932-5b4e61fc4b30">SetCommTimeouts</a> and 
    <a href="https://msdn.microsoft.com/a5375b2e-0992-4e47-a20f-8a793addeef6">GetCommTimeouts</a> functions. Unpredictable results can 
    occur if you fail to set the time-out values. For more information about communication time-outs, see 
    <a href="https://msdn.microsoft.com/259aa110-b2c3-4583-a3f9-805a42025a81">COMMTIMEOUTS</a>.

If <b>ReadFile</b> attempts to read from a mailslot that has a 
    buffer that is too small, the function returns <b>FALSE</b> and 
    <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns 
    <b>ERROR_INSUFFICIENT_BUFFER</b>.

There are strict requirements for successfully working with files opened with 
    <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> using the 
    <b>FILE_FLAG_NO_BUFFERING</b> flag. For details see 
    <a href="https://msdn.microsoft.com/ae1e5d0f-9b55-4aae-8402-b9c8e33d9363">File Buffering</a>.

If <i>hFile</i> was opened with <b>FILE_FLAG_OVERLAPPED</b>, the 
     following conditions are in effect:
     <ul>
<li>The <i>lpOverlapped</i> parameter must point to a valid and unique 
       <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure, otherwise the 
       function can incorrectly report that the read operation is complete.</li>
<li>The <i>lpNumberOfBytesRead</i> parameter should be set to 
       <b>NULL</b>. Use the 
       <a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a> function to get the actual 
       number of bytes read. If the <i>hFile</i> parameter is associated with an I/O completion 
       port, you can also get the number of bytes read by calling the 
       <a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a> function.</li>
</ul>


<h3><a id="synchronization_and_file_position"></a><a id="SYNCHRONIZATION_AND_FILE_POSITION"></a>Synchronization and File Position</h3>
If <i>hFile</i> is opened with <b>FILE_FLAG_OVERLAPPED</b>, it is an 
      asynchronous file handle; otherwise it is synchronous. The rules for using the 
      <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure are slightly different for each, 
      as previously noted.

<div class="alert"><b>Note</b>  If a file or device is opened for asynchronous I/O, subsequent calls to functions such as 
      <b>ReadFile</b> using that handle generally return immediately, but 
      can also behave synchronously with respect to blocked execution. For more information see 
      <a href="Http://go.microsoft.com/fwlink/p/?linkid=116863">http://support.microsoft.com/kb/156932</a>.</div>
<div> </div>
Considerations for working with asynchronous file handles:

<ul>
<li><b>ReadFile</b> may return before the read operation is 
       complete. In this scenario, <b>ReadFile</b> returns 
       <b>FALSE</b> and the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> 
       function returns <b>ERROR_IO_PENDING</b>, which allows the calling process to continue while 
       the system completes the read operation.</li>
<li>The <i>lpOverlapped</i> parameter must not be <b>NULL</b> and should 
       be used with the following facts in mind:
       <ul>
<li>Although the event specified in the <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> 
         structure is set and reset automatically by the system, the offset that is specified in the 
         <b>OVERLAPPED</b> structure is not automatically 
         updated.</li>
<li><b>ReadFile</b> resets the event to a nonsignaled state when 
         it begins the I/O operation.</li>
<li>The event specified in the <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure 
         is set to a signaled state when the read operation is complete; until that time, the read operation is 
         considered pending.</li>
<li>Because the read operation starts at the offset that is specified in the 
         <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure, and 
         <b>ReadFile</b> may return before the system-level read operation 
         is complete (read pending), neither the offset nor any other part of the structure should be modified, freed, 
         or reused by the application until the event is signaled (that is, the read completes).</li>
<li>If end-of-file (EOF) is detected during asynchronous operations, the call to 
         <a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a> for that operation 
         returns <b>FALSE</b> and 
         <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns 
         <b>ERROR_HANDLE_EOF</b>.</li>
</ul>
</li>
</ul>
Considerations for working with synchronous file handles:

<ul>
<li>If <i>lpOverlapped</i> is <b>NULL</b>, the read operation starts at 
       the current file position and <b>ReadFile</b> does not return until 
       the operation is complete, and the system updates the file pointer before 
       <b>ReadFile</b> returns.</li>
<li>If <i>lpOverlapped</i> is not <b>NULL</b>, the read operation starts 
       at the offset that is specified in the 
       <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure and 
       <b>ReadFile</b> does not return until the read operation is 
       complete. The system updates the <b>OVERLAPPED</b> offset 
       before <b>ReadFile</b> returns.</li>
<li>When a synchronous read operation reaches the end of a file, 
       <b>ReadFile</b> returns <b>TRUE</b> and sets 
       <code>*lpNumberOfBytesRead</code> to zero.</li>
</ul>
For more information, see <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> and 
      <a href="https://msdn.microsoft.com/ade51d98-cc9d-4b33-9c52-559a9cb14707">Synchronous and Asynchronous I/O</a>.

<h3><a id="pipes"></a><a id="PIPES"></a>Pipes</h3>
If an anonymous pipe is being used and the  write handle has been closed, when 
      <b>ReadFile</b> attempts to read using the pipe's corresponding read 
      handle, the function returns <b>FALSE</b> and 
      <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns 
      <b>ERROR_BROKEN_PIPE</b>.

If a named pipe is being read in message mode and the next message is longer than the 
      <i>nNumberOfBytesToRead</i> parameter specifies, 
      <b>ReadFile</b> returns <b>FALSE</b> and 
      <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns 
      <b>ERROR_MORE_DATA</b>. The remainder of the message can be read by a subsequent call to the 
      <b>ReadFile</b> or 
      <a href="https://msdn.microsoft.com/125e0fbb-9013-4194-bc0b-1b8ea7db799e">PeekNamedPipe</a>function.

If the <i>lpNumberOfBytesRead</i> parameter is zero when 
      <b>ReadFile</b> returns <b>TRUE</b> on a pipe, 
      the other end of the pipe called the <a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a> function with 
      <i>nNumberOfBytesToWrite</i> set to zero.

For more information about pipes, see <a href="https://msdn.microsoft.com/7cb8cbe4-eec8-4dda-9cb7-8d37abcee6f4">Pipes</a>.

<h3><a id="transacted_operations"></a><a id="TRANSACTED_OPERATIONS"></a>Transacted Operations</h3>
If there is a transaction bound to the file handle, then the function returns data from the transacted view of 
      the file. A transacted read handle is guaranteed to show the same view of a file for the duration of the 
      handle. For more information, see 
      <a href="https://msdn.microsoft.com/52341315-0412-4a87-aca0-9adea7aae62f">About Transactional NTFS</a>.

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
 


#### Examples

For a code example that shows you how to test for end-of-file, see 
     <a href="https://msdn.microsoft.com/93fa9e29-1ff1-496d-9551-99ae88ba7253">Testing for the End of  a File</a>. For other 
     examples, see 
     <a href="https://msdn.microsoft.com/6254c67d-5d34-499d-b1a4-8cac526dd294">Creating and Using a Temporary File</a> and 
     <a href="https://msdn.microsoft.com/04e089a7-c559-4a35-a38b-e1acdf3438d1">Opening a File for Reading or Writing</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/b28162dc-0da8-41c6-9901-29381d2d72c4">CancelIo</a>



<a href="https://msdn.microsoft.com/a2ce13b8-7da6-4848-848d-901d9667c2e3">CancelIoEx</a>



<a href="https://msdn.microsoft.com/f362c8b2-2193-443e-bb69-78f8b4147117">CancelSynchronousIo</a>



<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/a5375b2e-0992-4e47-a20f-8a793addeef6">GetCommTimeouts</a>



<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a>



<a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>



<a href="https://msdn.microsoft.com/125e0fbb-9013-4194-bc0b-1b8ea7db799e">PeekNamedPipe</a>



<a href="https://msdn.microsoft.com/6c1a4de1-6cae-4c35-bfba-0bc252fadbd9">ReadFileEx</a>



<a href="https://msdn.microsoft.com/71aa6ab3-d56c-43bc-9932-5b4e61fc4b30">SetCommTimeouts</a>



<a href="https://msdn.microsoft.com/b88f5577-9124-433c-a7e8-a7f713b7b27d">SetErrorMode</a>



<a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a>
 

 

