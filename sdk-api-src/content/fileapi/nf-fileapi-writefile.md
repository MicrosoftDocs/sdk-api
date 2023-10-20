---
UID: NF:fileapi.WriteFile
title: WriteFile function (fileapi.h)
description: Writes data to the specified file or input/output (I/O) device.
helpviewer_keywords: ["WriteFile","WriteFile function [Files]","_win32_writefile","base.writefile","fileapi/WriteFile","fs.writefile","winbase/WriteFile"]
old-location: fs\writefile.htm
tech.root: fs
ms.assetid: 9d6fa723-fe3e-4052-b0b3-2686eee076a7
ms.date: 12/05/2018
ms.keywords: WriteFile, WriteFile function [Files], _win32_writefile, base.writefile, fileapi/WriteFile, fs.writefile, winbase/WriteFile
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
 - WriteFile
 - fileapi/WriteFile
dev_langs:
 - c++
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
 - WriteFile
---

# WriteFile function


## -description

Writes data to the specified file or input/output (I/O) device.

This function is designed for both synchronous and asynchronous operation. For a similar function designed 
    solely for asynchronous operation, see <a href="/windows/desktop/api/fileapi/nf-fileapi-writefileex">WriteFileEx</a>.

## -parameters

### -param hFile [in]

A handle to the file or I/O device (for example, a file, file stream, physical disk, volume,  console buffer, 
       tape drive, socket, communications resource, mailslot, or  pipe).

The <i>hFile</i> parameter must have been created with the write access. For more 
       information, see 
       <a href="/windows/desktop/SecAuthZ/generic-access-rights">Generic Access Rights</a> and 
       <a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

For asynchronous write operations, <i>hFile</i> can be any handle opened with the 
       <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function using the 
       <b>FILE_FLAG_OVERLAPPED</b> flag or a socket handle returned by the 
       <a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a> or 
       <a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a> function.

### -param lpBuffer [in]

A pointer to the buffer containing the data to be written to the file or device.

This buffer must remain valid for the duration of the write operation. The caller must not use this buffer 
        until the write operation is completed.

### -param nNumberOfBytesToWrite [in]

The number of bytes to be written to the file or device.

A value of zero specifies a null write operation. The behavior of a null write operation depends on the 
        underlying file system or communications technology.

<b>Windows Server 2003 and Windows XP:  </b>Pipe write operations across a network are limited in size per write. The amount varies per platform. 
         For x86 platforms it's 63.97 MB. For x64 platforms it's 31.97 MB. For Itanium it's 63.95 MB. For more 
         information regarding pipes, see the Remarks section.

### -param lpNumberOfBytesWritten [out, optional]

A pointer to the variable that receives the number of bytes written when using a synchronous 
        <i>hFile</i> parameter. <b>WriteFile</b> sets 
        this value to zero before doing any work or error checking. Use <b>NULL</b> for this 
        parameter if this is an asynchronous operation to avoid potentially erroneous results.

This parameter can be <b>NULL</b> only when the <i>lpOverlapped</i> 
        parameter is not <b>NULL</b>.
        
<b>Windows 8 and later:  </b>This parameter can be <b>NULL</b> even if the <i>lpOverlapped</i> parameter is <b>NULL</b>.

For more information, see the Remarks section.

### -param lpOverlapped [in, out, optional]

A pointer to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure is 
       required if the <i>hFile</i> parameter was opened with 
       <b>FILE_FLAG_OVERLAPPED</b>, otherwise this parameter can be 
       <b>NULL</b>.

For an <i>hFile</i> that supports byte offsets, if you use this parameter you must specify 
       a byte offset at which to start writing to the file or device. This offset is specified by setting the 
       <b>Offset</b> and <b>OffsetHigh</b> members of the 
       <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. For an 
       <i>hFile</i> that does not support byte offsets, <b>Offset</b> and 
       <b>OffsetHigh</b> are ignored.

To write to the end of file, specify both the <b>Offset</b> and 
       <b>OffsetHigh</b> members of the 
       <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure as 0xFFFFFFFF. This is 
       functionally equivalent to previously calling the 
       <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function to open 
       <i>hFile</i> using <b>FILE_APPEND_DATA</b> access.

For more information about different combinations of <i>lpOverlapped</i> and 
       <b>FILE_FLAG_OVERLAPPED</b>, see the Remarks section and the 
       <a href="/">Synchronization and File Position</a> section.

## -returns

If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, or is completing asynchronously, the return value is zero 
       (<b>FALSE</b>). To get extended error information, call the 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> code 
       <b>ERROR_IO_PENDING</b> is not a failure; it designates the write operation is pending 
       completion asynchronously. For more information, see Remarks.</div>
<div> </div>

## -remarks

The <b>WriteFile</b> function returns when one of the following 
     conditions occur:

<ul>
<li>The number of bytes requested is written.</li>
<li>A read operation releases buffer space on the read end of the pipe (if the write was blocked). For more 
      information, see the <a href="/">Pipes</a> section.</li>
<li>An asynchronous handle is being used and the write is occurring asynchronously.</li>
<li>An error occurs.</li>
</ul>
The <b>WriteFile</b> function may fail with 
    <b>ERROR_INVALID_USER_BUFFER</b> or <b>ERROR_NOT_ENOUGH_MEMORY</b> whenever 
    there are too many outstanding asynchronous I/O requests.

To cancel all pending asynchronous I/O operations, use either:

<ul>
<li>
<a href="/windows/desktop/FileIO/cancelio">CancelIo</a>—this function cancels only 
      operations issued by the calling thread for the specified file handle.</li>
<li>
<a href="/windows/desktop/FileIO/cancelioex-func">CancelIoEx</a>—this function 
      cancels all operations issued by the threads for the specified file handle.</li>
</ul>
Use the <a href="/windows/desktop/FileIO/cancelsynchronousio-func">CancelSynchronousIo</a> function to 
     cancel pending synchronous I/O operations.

I/O operations that are canceled complete with the error <b>ERROR_OPERATION_ABORTED</b>.

The <b>WriteFile</b> function may fail with 
    <b>ERROR_NOT_ENOUGH_QUOTA</b>, which means the calling process's buffer could not be 
    page-locked. For more information, see 
    <a href="/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsize">SetProcessWorkingSetSize</a>.

If part of the file is locked by another process and the write operation overlaps the locked portion, 
    <b>WriteFile</b> fails.

When writing to a file, the last write time is not fully updated until all handles used for writing have been 
    closed. Therefore, to ensure an accurate last write time, close the file handle immediately after writing to the 
    file.

Accessing the output buffer while a write operation is using the buffer may lead to corruption of the data 
    written from that buffer. Applications must not write to, reallocate, or free the output buffer that a write 
    operation is using until the write operation completes. This can be particularly problematic when using an 
    asynchronous file handle. Additional information regarding synchronous versus asynchronous file handles can be 
    found later in the <a href="#synchronization-and-file-position">Synchronization and File Position</a> 
    section and 
    <a href="/windows/desktop/FileIO/synchronous-and-asynchronous-i-o">Synchronous and Asynchronous I/O</a>.

Note that the time stamps may not be updated correctly for a remote file. To ensure consistent results, use 
    unbuffered I/O.

The system interprets zero bytes to write as specifying a null write operation and 
    <b>WriteFile</b> does not truncate or extend the file. To truncate or 
    extend a file, use the <a href="/windows/desktop/api/fileapi/nf-fileapi-setendoffile">SetEndOfFile</a> 
    function.

Characters can be written to the screen buffer using 
    <b>WriteFile</b> with a handle to console output. The exact behavior 
    of the function is determined by the console mode. The data is written to the current cursor position. The cursor 
    position is updated after the write operation. For more information about console handles, see 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>.

When writing to a communications device, the behavior of 
    <b>WriteFile</b> is determined by the current communication time-out 
    as set and retrieved by using the <a href="/windows/desktop/api/winbase/nf-winbase-setcommtimeouts">SetCommTimeouts</a> and 
    <a href="/windows/desktop/api/winbase/nf-winbase-getcommtimeouts">GetCommTimeouts</a> functions. Unpredictable results can 
    occur if you fail to set the time-out values. For more information about communication time-outs, see 
    <a href="/windows/desktop/api/winbase/ns-winbase-commtimeouts">COMMTIMEOUTS</a>.

Although a single-sector write is atomic, a multi-sector write is not guaranteed to be atomic unless you are 
    using a transaction (that is, the handle created is a transacted handle; for example, a handle created using 
    <a href="/windows/desktop/api/winbase/nf-winbase-createfiletransacteda">CreateFileTransacted</a>). Multi-sector 
    writes that are cached may not always be written to the disk right away; therefore, specify 
    <b>FILE_FLAG_WRITE_THROUGH</b> in 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> to ensure that an entire multi-sector write is 
    written to the disk without potential caching delays.

If you write directly to a volume that has a mounted file system, you must first obtain exclusive access to 
    the volume. Otherwise, you risk causing data corruption or system instability, because your application's writes 
    may conflict with other changes coming from the file system and leave the contents of the volume in an 
    inconsistent state. To prevent these problems, the following changes have been made in Windows Vista 
    and later:

<ul>
<li>A write on a volume handle will succeed if the volume does not have a mounted file system, or if one of the 
      following conditions is true:
      <ul>
<li>The sectors to be written to are boot sectors.</li>
<li>The sectors to be written to reside outside of file system space.</li>
<li>You have explicitly locked or dismounted the volume by using 
        <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_lock_volume">FSCTL_LOCK_VOLUME</a> or 
        <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_dismount_volume">FSCTL_DISMOUNT_VOLUME</a>.</li>
<li>The volume has no actual file system. (In other words, it has a RAW file system mounted.)</li>
</ul>
</li>
<li>A write on a disk handle will succeed if one of the following conditions is true:
      <ul>
<li>The sectors to be written to do not fall within a volume's extents.</li>
<li>The sectors to be written to fall within a mounted volume, but you have explicitly locked or dismounted 
        the volume by using <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_lock_volume">FSCTL_LOCK_VOLUME</a> or 
        <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_dismount_volume">FSCTL_DISMOUNT_VOLUME</a>.</li>
<li>The sectors to be written to fall within a volume that has no mounted file system other than RAW.</li>
</ul>
</li>
</ul>
There are strict requirements for successfully working with files opened with 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> using 
    <b>FILE_FLAG_NO_BUFFERING</b>. For details see 
    <a href="/windows/desktop/FileIO/file-buffering">File Buffering</a>.

If <i>hFile</i> was opened with <b>FILE_FLAG_OVERLAPPED</b>, the 
     following conditions are in effect:

<ul>
<li>The <i>lpOverlapped</i> parameter must point to a valid and unique 
      <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure, otherwise the function can 
      incorrectly report that the write operation is complete.</li>
<li>The <i>lpNumberOfBytesWritten</i> parameter should be set to 
      <b>NULL</b>. To get the number of bytes written, use the 
      <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> function. If the 
      <i>hFile</i> parameter is associated with an I/O completion port, you can also get the number 
      of bytes written by calling the 
      <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> function.</li>
</ul>
In Windows Server 2012, this function is supported by the following technologies.

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
 

<h3><a id="synchronization_and_file_position"></a><a id="SYNCHRONIZATION_AND_FILE_POSITION"></a>Synchronization and File Position</h3>
If <i>hFile</i> is opened with <b>FILE_FLAG_OVERLAPPED</b>, it is an 
      asynchronous file handle; otherwise it is synchronous. The rules for using the 
      <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure are slightly different for each, 
      as previously noted.

<div class="alert"><b>Note</b>  If a  file or device is opened for asynchronous I/O, subsequent calls to functions such as 
      <b>WriteFile</b> using that handle generally return immediately, 
      but can also behave synchronously with respect to blocked execution. For more information, see 
      <a href="https://support.microsoft.com/kb/156932">http://support.microsoft.com/kb/156932</a>.</div>
<div> </div>
Considerations for working with asynchronous file handles:

<ul>
<li><b>WriteFile</b> may return before the write operation is 
       complete. In this scenario, <b>WriteFile</b> returns 
       <b>FALSE</b> and the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> 
       function returns <b>ERROR_IO_PENDING</b>, which allows the calling process to continue while 
       the system completes the write operation.</li>
<li>The <i>lpOverlapped</i> parameter must 
       not be <b>NULL</b> and should be used with the following facts in mind: 
       <ul>
<li>Although the event specified in the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> 
         structure is set and reset automatically by the system, the offset that is specified in the 
         <b>OVERLAPPED</b> structure is not automatically 
         updated.</li>
<li><b>WriteFile</b> resets the event to a nonsignaled state 
         when it begins the I/O operation.</li>
<li>The event specified in the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure 
         is set to a signaled state when the write operation is complete; until that time, the write operation is 
         considered pending.</li>
<li>Because the write operation starts at the offset that is specified in the 
         <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure, and 
         <b>WriteFile</b> may return before the system-level write 
         operation is complete (write pending), neither the offset nor any other part of the structure should be 
         modified, freed, or reused by the application until the event is signaled (that is, the write 
         completes).</li>
</ul>
</li>
</ul>
Considerations for working with synchronous file handles:

<ul>
<li>If <i>lpOverlapped</i> is <b>NULL</b>, the write operation starts at 
       the current file position and <b>WriteFile</b> does not return 
       until the operation is complete, and the system updates the file pointer before 
       <b>WriteFile</b> returns.</li>
<li>If <i>lpOverlapped</i> is not <b>NULL</b>, the write operation 
       starts at the offset that is specified in the 
       <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure and 
       <b>WriteFile</b> does not return until the write operation is 
       complete. The system updates the <b>OVERLAPPED</b> Internal and InternalHigh fields 
       and the file pointer before <b>WriteFile</b> returns.</li>
</ul>
For more information, see <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> and 
      <a href="/windows/desktop/FileIO/synchronous-and-asynchronous-i-o">Synchronous and Asynchronous I/O</a>.

<h3><a id="pipes"></a><a id="PIPES"></a>Pipes</h3>
If an anonymous pipe is being used and the read handle has been closed, when 
      <b>WriteFile</b> attempts to write using the pipe's corresponding 
      write handle, the function returns <b>FALSE</b> and 
      <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns 
      <b>ERROR_BROKEN_PIPE</b>.

If the pipe buffer is full when an application uses the 
      <b>WriteFile</b> function to write to a pipe, the write operation 
      may not finish immediately. The write operation will be completed when a read operation (using the 
      <a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a> function) makes more system buffer space available 
      for the pipe.

When writing to a non-blocking, byte-mode pipe handle with insufficient buffer space, 
      <b>WriteFile</b> returns <b>TRUE</b> with 
      *<i>lpNumberOfBytesWritten</i> &lt; <i>nNumberOfBytesToWrite</i>.

For more information about pipes, see <a href="/windows/desktop/ipc/pipes">Pipes</a>.

<h3><a id="transacted_operations"></a><a id="TRANSACTED_OPERATIONS"></a>Transacted Operations</h3>
If there is a transaction bound to the file handle, then the file write is transacted. For more information, 
      see <a href="/windows/desktop/FileIO/about-transactional-ntfs">About Transactional NTFS</a>.


#### Examples

For some examples, see 
     <a href="/windows/desktop/FileIO/creating-and-using-a-temporary-file">Creating and Using a Temporary File</a> 
     and 
     <a href="/windows/desktop/FileIO/opening-a-file-for-reading-or-writing">Opening a File for Reading or Writing</a>.

<div class="code"></div>
The following C++ example shows how to align sectors for unbuffered file writes. The 
     <i>Size</i> variable is the size of the original data block you are interested in writing to 
     the file. For additional rules regarding unbuffered file I/O, see 
     <a href="/windows/desktop/FileIO/file-buffering">File Buffering</a>.


```cpp
#include <windows.h>

#define ROUND_UP_SIZE(Value,Pow2) ((SIZE_T) ((((ULONG)(Value)) + (Pow2) - 1) & (~(((LONG)(Pow2)) - 1))))

#define ROUND_UP_PTR(Ptr,Pow2)  ((void *) ((((ULONG_PTR)(Ptr)) + (Pow2) - 1) & (~(((LONG_PTR)(Pow2)) - 1))))

int main()
{
   // Sample data
   unsigned long bytesPerSector = 65536; // obtained from the GetFreeDiskSpace function.
   unsigned long size = 15536; // Buffer size of your data to write.
   
   // Ensure you have one more sector than Size would require.
   size_t sizeNeeded = bytesPerSector + ROUND_UP_SIZE(size, bytesPerSector);
   
   // Replace this statement with any allocation routine.
   auto buffer = new uint8_t[SizeNeeded];
   
   // Actual alignment happens here.
   auto bufferAligned = ROUND_UP_PTR(buffer, bytesPerSector);

   // ... Add code using bufferAligned here.
   
   // Replace with corresponding free routine.
   delete buffer;
}

```

## -see-also

<a href="/windows/desktop/FileIO/cancelio">CancelIo</a>



<a href="/windows/desktop/FileIO/cancelioex-func">CancelIoEx</a>



<a href="/windows/desktop/FileIO/cancelsynchronousio-func">CancelSynchronousIo</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createfiletransacteda">CreateFileTransacted</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-setendoffile">SetEndOfFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefileex">WriteFileEx</a>
