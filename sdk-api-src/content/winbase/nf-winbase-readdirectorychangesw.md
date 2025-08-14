---
UID: NF:winbase.ReadDirectoryChangesW
title: ReadDirectoryChangesW function (winbase.h)
description: Retrieves information that describes the changes within the specified directory.
helpviewer_keywords: ["FILE_NOTIFY_CHANGE_ATTRIBUTES","FILE_NOTIFY_CHANGE_CREATION","FILE_NOTIFY_CHANGE_DIR_NAME","FILE_NOTIFY_CHANGE_FILE_NAME","FILE_NOTIFY_CHANGE_LAST_ACCESS","FILE_NOTIFY_CHANGE_LAST_WRITE","FILE_NOTIFY_CHANGE_SECURITY","FILE_NOTIFY_CHANGE_SIZE","ReadDirectoryChangesW","ReadDirectoryChangesW function [Files]","_win32_readdirectorychangesw","base.readdirectorychangesw","fs.readdirectorychangesw","winbase/ReadDirectoryChangesW"]
old-location: fs\readdirectorychangesw.htm
tech.root: fs
ms.assetid: 14dfc93d-557e-43d0-be45-8414cfd92c29
ms.date: 12/05/2018
ms.keywords: FILE_NOTIFY_CHANGE_ATTRIBUTES, FILE_NOTIFY_CHANGE_CREATION, FILE_NOTIFY_CHANGE_DIR_NAME, FILE_NOTIFY_CHANGE_FILE_NAME, FILE_NOTIFY_CHANGE_LAST_ACCESS, FILE_NOTIFY_CHANGE_LAST_WRITE, FILE_NOTIFY_CHANGE_SECURITY, FILE_NOTIFY_CHANGE_SIZE, ReadDirectoryChangesW, ReadDirectoryChangesW function [Files], _win32_readdirectorychangesw, base.readdirectorychangesw, fs.readdirectorychangesw, winbase/ReadDirectoryChangesW
req.header: winbase.h
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
 - ReadDirectoryChangesW
 - winbase/ReadDirectoryChangesW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-file-l2-1-4.dll
 - api-ms-win-core-file-l2-1-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-File-l2-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l2-1-1.dll
 - API-MS-Win-Core-File-l2-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
api_name:
 - ReadDirectoryChangesW
---

# ReadDirectoryChangesW function


## -description

Retrieves information that describes the changes within the specified directory. The 
    function does not report changes to the specified directory itself.

To track changes on a volume, see 
    <a href="/windows/desktop/FileIO/change-journals">change journals</a>.

## -parameters

### -param hDirectory [in]

A handle to the directory to be monitored. This directory must be opened with the 
      <b>FILE_LIST_DIRECTORY</b> access right, or an access right such as <b>GENERIC_READ</b> that includes the <b>FILE_LIST_DIRECTORY</b> access right.

### -param lpBuffer [out]

A pointer to the <b>DWORD</b>-aligned formatted buffer in which the read results are 
      to be returned. The structure of this buffer is defined by the 
      <a href="/windows/desktop/api/winnt/ns-winnt-file_notify_information">FILE_NOTIFY_INFORMATION</a> structure. This 
      buffer is filled either synchronously or asynchronously, depending on how the directory is opened and what value 
      is given to the <i>lpOverlapped</i> parameter. For more information, see the Remarks 
      section.

### -param nBufferLength [in]

The size of the buffer that is pointed to by the <i>lpBuffer</i> parameter, in 
      bytes.

### -param bWatchSubtree [in]

If this parameter is <b>TRUE</b>, the function monitors the directory tree rooted at the 
      specified directory. If this parameter is <b>FALSE</b>, the function monitors only the 
      directory specified by the <i>hDirectory</i> parameter.

### -param dwNotifyFilter [in]

The filter criteria that the function checks to determine if the wait operation has completed. This 
      parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_NOTIFY_CHANGE_FILE_NAME"></a><a id="file_notify_change_file_name"></a><dl>
<dt><b>FILE_NOTIFY_CHANGE_FILE_NAME</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Any file name change in the watched directory or subtree causes a change notification wait operation to 
        return. Changes include renaming, creating, or deleting a file.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_NOTIFY_CHANGE_DIR_NAME"></a><a id="file_notify_change_dir_name"></a><dl>
<dt><b>FILE_NOTIFY_CHANGE_DIR_NAME</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Any directory-name change in the watched directory or subtree causes a change notification wait operation 
        to return. Changes include creating or deleting a directory.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_NOTIFY_CHANGE_ATTRIBUTES"></a><a id="file_notify_change_attributes"></a><dl>
<dt><b>FILE_NOTIFY_CHANGE_ATTRIBUTES</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Any attribute change in the watched directory or subtree causes a change notification wait operation to 
        return.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_NOTIFY_CHANGE_SIZE"></a><a id="file_notify_change_size"></a><dl>
<dt><b>FILE_NOTIFY_CHANGE_SIZE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Any file-size change in the watched directory or subtree causes a change notification wait operation to 
        return. The operating system detects a change in file size only when the file is written to the disk. For 
        operating systems that use extensive caching, detection occurs only when the cache is sufficiently 
        flushed.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_NOTIFY_CHANGE_LAST_WRITE"></a><a id="file_notify_change_last_write"></a><dl>
<dt><b>FILE_NOTIFY_CHANGE_LAST_WRITE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Any change to the last write-time of files in the watched directory or subtree causes a change 
        notification wait operation to return. The operating system detects a change to the last write-time only when 
        the file is written to the disk. For operating systems that use extensive caching, detection occurs only when 
        the cache is sufficiently flushed.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_NOTIFY_CHANGE_LAST_ACCESS"></a><a id="file_notify_change_last_access"></a><dl>
<dt><b>FILE_NOTIFY_CHANGE_LAST_ACCESS</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Any change to the last access time of files in the watched directory or subtree causes a change 
        notification wait operation to return.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_NOTIFY_CHANGE_CREATION"></a><a id="file_notify_change_creation"></a><dl>
<dt><b>FILE_NOTIFY_CHANGE_CREATION</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Any change to the creation time of files in the watched directory or subtree causes a change notification 
        wait operation to return.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_NOTIFY_CHANGE_SECURITY"></a><a id="file_notify_change_security"></a><dl>
<dt><b>FILE_NOTIFY_CHANGE_SECURITY</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Any security-descriptor change in the watched directory or subtree causes a change notification wait 
        operation to return.

</td>
</tr>
</table>

### -param lpBytesReturned [out, optional]

For synchronous calls, this parameter receives the number of bytes transferred into the 
      <i>lpBuffer</i> parameter. For asynchronous calls, this parameter is undefined. You must use 
      an asynchronous notification technique to retrieve the number of bytes transferred.

### -param lpOverlapped [in, out, optional]

A pointer to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure that supplies 
      data to be used during asynchronous operation. Otherwise, this value is <b>NULL</b>. The 
      <b>Offset</b> and <b>OffsetHigh</b> members of this structure are not 
      used.

### -param lpCompletionRoutine [in, optional]

A pointer to a completion routine to be called when the operation has been completed or canceled and the 
      calling thread is in an alertable wait state. For more information about this completion routine, see 
      <a href="/windows/desktop/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine">FileIOCompletionRoutine</a>.

## -returns

If the function succeeds, the return value is nonzero. For synchronous calls, this means that the operation 
       succeeded. For asynchronous calls, this indicates that the operation was successfully queued.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If the network redirector or the target file system does not support this operation, the function fails with 
       <b>ERROR_INVALID_FUNCTION</b>.

## -remarks

To obtain a handle to a directory, use the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> 
    function with the <b>FILE_FLAG_BACKUP_SEMANTICS</b> flag.

A call to <b>ReadDirectoryChangesW</b> can be 
    completed synchronously or asynchronously. To specify asynchronous completion, open the directory with 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> as shown above, but additionally specify the 
    <b>FILE_FLAG_OVERLAPPED</b> attribute in the <i>dwFlagsAndAttributes</i> 
    parameter. Then specify an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure when you 
    call <b>ReadDirectoryChangesW</b>.

When you first call **ReadDirectoryChangesW**, the system allocates a buffer to store change information. This buffer is associated with the directory handle until it is closed and its size does not change during its lifetime. Directory changes that occur between calls to this function are added to the buffer and then returned with the next call. If the buffer overflows, **ReadDirectoryChangesW** will still return **true**, but the entire contents of the buffer are discarded and the *lpBytesReturned* parameter will be zero, which indicates that your buffer was too small to hold all of the changes that occurred.

Upon successful synchronous completion, the <i>lpBuffer</i> parameter is a formatted buffer 
    and the number of bytes written to the buffer is available in <i>lpBytesReturned</i>. If the 
    number of bytes transferred is zero, the buffer was either too large for the system to allocate or too small to 
    provide detailed information on all the changes that occurred in the directory or subtree. In this case, you 
    should compute the changes by enumerating the directory or subtree.

For asynchronous completion, you can receive notification in one of three ways:

<ul>
<li>Using the <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> function. To 
      receive notification through 
      <b>GetOverlappedResult</b>, do not specify a completion 
      routine in the <i>lpCompletionRoutine</i> parameter. Be sure to set the 
      <b>hEvent</b> member of the 
      <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure to a unique event.</li>
<li>Using the <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> 
      function. To receive notification through 
      <b>GetQueuedCompletionStatus</b>, do not specify 
      a completion routine in <i>lpCompletionRoutine</i>. Associate the directory handle 
      <i>hDirectory</i> with a completion port by calling the 
      <a href="/windows/desktop/FileIO/createiocompletionport">CreateIoCompletionPort</a> function.</li>
<li>Using a completion routine. To receive notification through a completion routine, do not associate the 
      directory with a completion port. Specify a completion routine in <i>lpCompletionRoutine</i>. 
      This routine is called whenever the operation has been completed or canceled while the thread is in an alertable 
      wait state. The <b>hEvent</b> member of the 
      <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure is not used by the system, so you 
      can use it yourself.</li>
</ul>
 For more information, see 
     <a href="/windows/desktop/FileIO/synchronous-and-asynchronous-i-o">Synchronous and Asynchronous I/O</a>.

<b>ReadDirectoryChangesW</b> fails with 
    <b>ERROR_INVALID_PARAMETER</b> when the buffer length is greater than 64 KB and the application 
    is monitoring a directory over the network. This is due to a packet size limitation with the underlying file 
    sharing protocols.

<b>ReadDirectoryChangesW</b> fails with 
    <b>ERROR_NOACCESS</b> when the buffer is not aligned on a <b>DWORD</b> 
    boundary.

<b>ReadDirectoryChangesW</b> fails with
<b>ERROR_NOTIFY_ENUM_DIR</b>
when the system was unable to record all the changes to the directory.
In this case, you should compute the changes by enumerating the directory or subtree.

If you opened the file using the short name, you can receive change notifications for the short name.

In Windows 8 and Windows Server 2012, this function is supported by the following 
    technologies.

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
If there is a transaction bound to the directory handle, then the notifications follow the appropriate 
      transaction isolation rules.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/FileIO/createiocompletionport">CreateIoCompletionPort</a>



<a href="/windows/desktop/FileIO/directory-management-functions">Directory Management Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-file_notify_information">FILE_NOTIFY_INFORMATION</a>



<a href="/windows/desktop/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine">FileIOCompletionRoutine</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>