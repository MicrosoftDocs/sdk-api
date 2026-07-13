---
UID: NF:winbase.OpenFileById
title: OpenFileById function (winbase.h)
description: Opens the file that matches the specified identifier.
helpviewer_keywords: ["FILE_FLAG_BACKUP_SEMANTICS","FILE_FLAG_NO_BUFFERING","FILE_FLAG_OPEN_NO_RECALL","FILE_FLAG_OPEN_REPARSE_POINT","FILE_FLAG_OVERLAPPED","FILE_FLAG_RANDOM_ACCESS","FILE_FLAG_SEQUENTIAL_SCAN","FILE_FLAG_WRITE_THROUGH","FILE_SHARE_DELETE","FILE_SHARE_READ","FILE_SHARE_WRITE","OpenFileById","OpenFileById function [Files]","fileextd/OpenFileById","fs.openfilebyid","winbase/OpenFileById"]
old-location: fs\openfilebyid.htm
tech.root: fs
ms.assetid: caa757a2-fc3f-4883-8d3e-b98d28f92517
ms.date: 12/05/2018
ms.keywords: FILE_FLAG_BACKUP_SEMANTICS, FILE_FLAG_NO_BUFFERING, FILE_FLAG_OPEN_NO_RECALL, FILE_FLAG_OPEN_REPARSE_POINT, FILE_FLAG_OVERLAPPED, FILE_FLAG_RANDOM_ACCESS, FILE_FLAG_SEQUENTIAL_SCAN, FILE_FLAG_WRITE_THROUGH, FILE_SHARE_DELETE, FILE_SHARE_READ, FILE_SHARE_WRITE, OpenFileById, OpenFileById function [Files], fileextd/OpenFileById, fs.openfilebyid, winbase/OpenFileById
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib; FileExtd.lib on Windows Server 2003 and Windows XP
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows SDK on Windows Server 2003 and Windows XP.
ms.custom: 19H1
f1_keywords:
 - OpenFileById
 - winbase/OpenFileById
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
 - API-MS-Win-Core-File-l2-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l2-1-2.dll
api_name:
 - OpenFileById
---

# OpenFileById function


## -description

Opens the file that matches the specified identifier.

## -parameters

### -param hVolumeHint [in]

A handle to any file on a volume or share on which the file to be opened is stored.

### -param lpFileId [in]

A pointer to a <a href="/windows/desktop/api/winbase/ns-winbase-file_id_descriptor">FILE_ID_DESCRIPTOR</a> that identifies 
       the file to open.

### -param dwDesiredAccess [in]

The access to the object. Access can be read, write, or both.

For more information, see 
      <a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access
      Rights</a>. You cannot request an access mode that conflicts with the sharing mode that is specified in an
      open request that has an open handle.

If this parameter is zero (0), the application can query file and device attributes without accessing a
      device. This is useful for an application to determine the size of a floppy disk drive and the formats it
      supports without requiring a floppy in a drive. It can also be used to test for the existence of a file or
      directory without opening them for read or write access.

### -param dwShareMode [in]

The sharing mode of an object, which can be read, write, both, or none.

You cannot request a sharing mode that conflicts with the access mode that is specified in an open request 
       that has an open handle, because that would result in the following sharing violation: 
       (<b>ERROR_SHARING_VIOLATION</b>). For more information, see 
       <a href="/windows/desktop/FileIO/creating-and-opening-files">Creating and Opening Files</a>.

If this parameter is zero (0) and <b>OpenFileById</b> 
       succeeds, the object cannot be shared and cannot be opened again until the handle is closed. For more 
       information, see the Remarks section of this topic.

The sharing options remain in effect until you close the handle to an object.

To enable a processes to share an object while another process has the object open, use a combination of one 
       or more of the following values to specify the access mode they can request to open the object.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_SHARE_DELETE"></a><a id="file_share_delete"></a><dl>
<dt><b>FILE_SHARE_DELETE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Enables subsequent open operations on an object to request delete access.

Otherwise, other processes cannot open the object if they request delete access.

If this flag is not specified, but the object has been opened for delete access, the function fails.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SHARE_READ"></a><a id="file_share_read"></a><dl>
<dt><b>FILE_SHARE_READ</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Enables subsequent open operations on an object to request read access.

Otherwise, other processes cannot open the object if they request read access.

If this flag is not specified, but the object has been opened for read access, the function fails.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SHARE_WRITE"></a><a id="file_share_write"></a><dl>
<dt><b>FILE_SHARE_WRITE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Enables subsequent open operations on an object to request write access.

Otherwise, other processes cannot open the object if they request write access.

If this flag is not specified, but the object has been opened for write access or has a file mapping with 
         write access, the function fails.

</td>
</tr>
</table>

### -param lpSecurityAttributes [in, optional]

Reserved.

### -param dwFlagsAndAttributes [in]

The file flags.

When <b>OpenFileById</b> opens a file, it combines the file 
       flags with existing file attributes, and ignores any supplied file attributes. This parameter can include any 
       combination of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_BACKUP_SEMANTICS"></a><a id="file_flag_backup_semantics"></a><dl>
<dt><b>FILE_FLAG_BACKUP_SEMANTICS</b></dt>
<dt>0x02000000</dt>
</dl>
</td>
<td width="60%">
A file is being opened for a backup or restore operation. The system ensures that the calling process 
         overrides file security checks when the process has <b>SE_BACKUP_NAME</b> and 
         <b>SE_RESTORE_NAME</b> privileges. For more information, see 
         <a href="/windows/desktop/SecBP/changing-privileges-in-a-token">Changing Privileges in a Token</a>.

You must set this flag to obtain a handle to a directory. A directory handle can be passed to some 
         functions  instead of a file handle. For more information, see 
         <a href="/windows/desktop/FileIO/obtaining-a-handle-to-a-directory">Directory Handles</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_NO_BUFFERING"></a><a id="file_flag_no_buffering"></a><dl>
<dt><b>FILE_FLAG_NO_BUFFERING</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
The system opens a file with no system caching. This flag does not affect hard disk caching. When combined 
         with <b>FILE_FLAG_OVERLAPPED</b>, the flag gives maximum asynchronous performance, because 
         the I/O does not rely on the synchronous operations of the memory manager. However, some I/O operations take 
         more time, because data is not being held in the cache. Also, the file metadata may still be cached. To flush 
         the metadata to disk, use the <a href="/windows/desktop/api/fileapi/nf-fileapi-flushfilebuffers">FlushFileBuffers</a> 
         function.

An application must meet certain requirements when working with files that are opened with 
         <b>FILE_FLAG_NO_BUFFERING</b>:

<ul>
<li>File access must begin at byte offsets within a file that are integer multiples of the volume sector 
          size.</li>
<li>File access must be for numbers of bytes that are integer multiples of the volume sector size. For 
          example, if the sector size is 512 bytes, an application can request reads and writes of 512, 1024, 1536, or 
          2048 bytes, but not of 335, 981, or 7171 bytes.</li>
<li>Buffer addresses for read and write operations should be sector aligned, which means aligned on 
          addresses in memory that are integer multiples of the volume sector size. Depending on the disk, this 
          requirement may not be enforced.</li>
</ul>
One way to align buffers on integer multiples of the volume sector size is to use 
         <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a> to allocate the buffers. It allocates 
         memory that is aligned on addresses that are integer multiples of the operating system's memory page size. 
         Because both memory page and volume sector sizes are powers of 2, this memory is also aligned on addresses 
         that are integer multiples of a volume sector size. Memory pages are 4-8 KB in size; sectors are 512 bytes 
         (hard disks) or 2048 bytes (CD), and therefore, volume sectors can never be larger than memory pages.

An application can determine a volume sector size by calling the 
         <a href="/windows/desktop/api/fileapi/nf-fileapi-getdiskfreespacea">GetDiskFreeSpace</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_OPEN_NO_RECALL"></a><a id="file_flag_open_no_recall"></a><dl>
<dt><b>FILE_FLAG_OPEN_NO_RECALL</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
The file data is requested, but it should continue to be located in remote storage. It should not be 
         transported back to local storage. This flag is for use by remote storage systems.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_OPEN_REPARSE_POINT"></a><a id="file_flag_open_reparse_point"></a><dl>
<dt><b>FILE_FLAG_OPEN_REPARSE_POINT</b></dt>
<dt>0x00200000</dt>
</dl>
</td>
<td width="60%">
When this flag is used, normal <a href="/windows/desktop/FileIO/reparse-points">reparse point</a> 
         processing does not occur, and <b>OpenFileById</b> attempts 
         to open the reparse point. When a file is opened, a file handle is returned, whether or not the filter that 
         controls the reparse point is operational. This flag cannot be used with the 
         <b>CREATE_ALWAYS</b> flag. If the file is not a reparse point, then this flag is 
         ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_OVERLAPPED"></a><a id="file_flag_overlapped"></a><dl>
<dt><b>FILE_FLAG_OVERLAPPED</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
The file is being opened or created for asynchronous I/O. When the operation is complete, the event 
         specified to the call in the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure is 
         set to the signaled state. Operations that take a significant amount of time to process return 
         <b>ERROR_IO_PENDING</b>.

If this flag is specified, the file can be used for simultaneous read and write operations. The system does 
         not maintain the file pointer, therefore you must pass the file position to the read and write functions in 
         the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>  structure or update the file 
         pointer.

If this flag is not specified, then I/O operations are serialized, even if the calls to the read and write 
         functions specify an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_RANDOM_ACCESS"></a><a id="file_flag_random_access"></a><dl>
<dt><b>FILE_FLAG_RANDOM_ACCESS</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
A file is accessed randomly. The system can use this as a hint to optimize file caching.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_SEQUENTIAL_SCAN"></a><a id="file_flag_sequential_scan"></a><dl>
<dt><b>FILE_FLAG_SEQUENTIAL_SCAN</b></dt>
<dt>0x08000000</dt>
</dl>
</td>
<td width="60%">
A file is accessed sequentially from beginning to end. The system can use this as a hint to optimize file 
         caching. If an application moves the file pointer for random access, optimum caching may not occur. However, 
         correct operation is still guaranteed.

Specifying this flag can increase performance for applications that read large files using sequential 
         access. Performance gains can be even more noticeable for applications that read large files mostly 
         sequentially, but occasionally skip over small ranges of bytes.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_WRITE_THROUGH"></a><a id="file_flag_write_through"></a><dl>
<dt><b>FILE_FLAG_WRITE_THROUGH</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
The system writes through any intermediate cache and goes directly to disk.

If <b>FILE_FLAG_NO_BUFFERING</b> is not also specified, so that system caching is in 
         effect, then the data is written to the system cache, but is flushed to disk without delay.

If <b>FILE_FLAG_NO_BUFFERING</b> is also specified, so that system caching is not in 
         effect, then the data is immediately flushed to disk without going through the system cache. The operating 
         system also requests a write-through the hard disk cache to persistent media. However, not all hardware 
         supports this write-through capability.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is an open handle to a specified file.

If the function fails, the return value is <b>INVALID_HANDLE_VALUE</b>. To get extended 
       error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Use the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to close an object handle 
    that <b>OpenFileById</b> returns.

If you call <b>OpenFileById</b> on a file that is pending 
    deletion as a result of a previous call to <a href="/windows/desktop/api/fileapi/nf-fileapi-deletefilea">DeleteFile</a>, the 
    function fails. The operating system delays file deletion until all handles to the file are closed. 
    <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns 
    <b>ERROR_ACCESS_DENIED</b>.

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
No

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
No

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

<a href="/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a>



<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-deletefilea">DeleteFile</a>



<a href="/windows/desktop/api/winbase/ns-winbase-file_id_descriptor">FILE_ID_DESCRIPTOR</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/desktop/api/winbase/nf-winbase-openfile">OpenFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a>