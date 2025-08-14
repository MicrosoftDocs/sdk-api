---
UID: NF:winbase.ReOpenFile
title: ReOpenFile function (winbase.h)
description: Reopens the specified file system object with different access rights, sharing mode, and flags.
helpviewer_keywords: ["FILE_FLAG_BACKUP_SEMANTICS","FILE_FLAG_DELETE_ON_CLOSE","FILE_FLAG_NO_BUFFERING","FILE_FLAG_OPEN_NO_RECALL","FILE_FLAG_OPEN_REPARSE_POINT","FILE_FLAG_OVERLAPPED","FILE_FLAG_POSIX_SEMANTICS","FILE_FLAG_RANDOM_ACCESS","FILE_FLAG_SEQUENTIAL_SCAN","FILE_FLAG_WRITE_THROUGH","FILE_SHARE_DELETE","FILE_SHARE_READ","FILE_SHARE_WRITE","ReOpenFile","ReOpenFile function [Files]","SECURITY_ANONYMOUS","SECURITY_CONTEXT_TRACKING","SECURITY_DELEGATION","SECURITY_EFFECTIVE_ONLY","SECURITY_IDENTIFICATION","SECURITY_IMPERSONATION","base.reopenfile","fs.reopenfile","winbase/ReOpenFile"]
old-location: fs\reopenfile.htm
tech.root: fs
ms.assetid: 56d8a4b1-e3b5-4134-8d21-bf40761e9dcc
ms.date: 12/05/2018
ms.keywords: FILE_FLAG_BACKUP_SEMANTICS, FILE_FLAG_DELETE_ON_CLOSE, FILE_FLAG_NO_BUFFERING, FILE_FLAG_OPEN_NO_RECALL, FILE_FLAG_OPEN_REPARSE_POINT, FILE_FLAG_OVERLAPPED, FILE_FLAG_POSIX_SEMANTICS, FILE_FLAG_RANDOM_ACCESS, FILE_FLAG_SEQUENTIAL_SCAN, FILE_FLAG_WRITE_THROUGH, FILE_SHARE_DELETE, FILE_SHARE_READ, FILE_SHARE_WRITE, ReOpenFile, ReOpenFile function [Files], SECURITY_ANONYMOUS, SECURITY_CONTEXT_TRACKING, SECURITY_DELEGATION, SECURITY_EFFECTIVE_ONLY, SECURITY_IDENTIFICATION, SECURITY_IMPERSONATION, base.reopenfile, fs.reopenfile, winbase/ReOpenFile
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - ReOpenFile
 - winbase/ReOpenFile
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
 - ReOpenFile
---

# ReOpenFile function


## -description

Reopens the specified file system object with different access rights, sharing mode, and 
    flags.

## -parameters

### -param hOriginalFile [in]

A handle to the object to be reopened. The object must have been created by the 
       <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function.

### -param dwDesiredAccess [in]

The required access to the object. For a list of values, see 
	      <a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>. You 
	      cannot request an access mode that conflicts with the sharing mode specified in a previous open request whose 
	      handle is still open.

If this parameter is zero (0), the application can query device attributes without accessing the device. This 
       is useful if an application wants to determine the size of a floppy disk drive and the formats it supports 
       without requiring a floppy in the drive.

### -param dwShareMode [in]

The sharing mode of the object. You cannot request a sharing mode that conflicts with the access mode 
       specified in a previous open request whose handle is still open.

If this parameter is zero (0) and <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> succeeds, 
       the object cannot be shared and cannot be opened again until the handle is closed.

To enable other processes to share the object while your process has it open, use a combination of one or 
       more of the following values to specify the type of access they can request when they open the object. These 
       sharing options remain in effect until you close the handle to the object.

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
Enables subsequent open operations on the object to request delete access. Otherwise, other processes 
         cannot open the object if they request delete access.

If the object has already been opened with delete access, the sharing mode must include this flag.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SHARE_READ"></a><a id="file_share_read"></a><dl>
<dt><b>FILE_SHARE_READ</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Enables subsequent open operations on the object to request read access. Otherwise, other processes cannot 
         open the object if they request read access.

If the object has already been opened with read access, the sharing mode must include this flag.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SHARE_WRITE"></a><a id="file_share_write"></a><dl>
<dt><b>FILE_SHARE_WRITE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Enables subsequent open operations on the object to request write access. Otherwise, other processes cannot 
         open the object if they request write access.

If the object has already been opened with write access, the sharing mode must include this flag.

</td>
</tr>
</table>

### -param dwFlagsAndAttributes [in]

The file flags. This parameter can be one or more of the following values.

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
Indicates that the file is being opened or created for a backup or restore operation. The system ensures 
         that the calling process overrides file security checks, provided it has the 
         <b>SE_BACKUP_NAME</b> and <b>SE_RESTORE_NAME</b> privileges. For more 
         information, see 
         <a href="/windows/desktop/SecBP/changing-privileges-in-a-token">Changing Privileges in a Token</a>.

You can also set this flag to obtain a handle to a directory. Where indicated, a directory handle can be 
         passed to some functions in place of a file handle.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_DELETE_ON_CLOSE"></a><a id="file_flag_delete_on_close"></a><dl>
<dt><b>FILE_FLAG_DELETE_ON_CLOSE</b></dt>
<dt>0x04000000</dt>
</dl>
</td>
<td width="60%">
Indicates that the operating system is to delete the file immediately after all of its handles have been 
         closed, not just the specified handle but also any other open or duplicated handles.

Subsequent open requests for the file fail, unless <b>FILE_SHARE_DELETE</b> is used.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_NO_BUFFERING"></a><a id="file_flag_no_buffering"></a><dl>
<dt><b>FILE_FLAG_NO_BUFFERING</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
Instructs the system to open the file with no intermediate buffering or caching. When combined with 
         <b>FILE_FLAG_OVERLAPPED</b>, the flag gives maximum asynchronous performance, because the 
         I/O does not rely on the synchronous operations of the memory manager. However, some I/O operations take 
         longer, because data is not being held in the cache.

An application must meet specific requirements when working with files opened with 
         <b>FILE_FLAG_NO_BUFFERING</b>:

<ul>
<li>File access must begin at byte offsets within the file that are integer multiples of the volume sector 
          size.</li>
<li>File access must be for numbers of bytes that are integer multiples of the volume sector size. For 
          example, if the sector size is 512 bytes, an application can request reads and writes of 512, 1024, 1536, or 
          2048 bytes, but not of 335, 981, or 7171 bytes.</li>
<li>Buffer addresses for read and write operations should be sector aligned (aligned on addresses in memory 
          that are integer multiples of the volume sector size). Depending on the disk, this requirement may not be 
          enforced.</li>
</ul>
One way to align buffers on integer multiples of the volume sector size is to use 
         <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a> to allocate the buffers. It allocates 
         memory that is aligned on addresses that are integer multiples of the operating system memory page size. 
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
Indicates that the file data is requested, but it should continue to reside in remote storage. It should 
         not be transported back to local storage. This flag is intended for use by remote storage systems.

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
         processing does not occur, and <b>ReOpenFile</b> attempts to 
         open the reparse point. When a file is opened, a file handle is returned, whether or not the filter that 
         controls the reparse point is operational. This flag cannot be used with the 
         <b>CREATE_ALWAYS</b> flag. If the file is not a reparse point, then this flag is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_OVERLAPPED"></a><a id="file_flag_overlapped"></a><dl>
<dt><b>FILE_FLAG_OVERLAPPED</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
Instructs the system to initialize the object, so that operations that take a significant amount of time to
        process return <b>ERROR_IO_PENDING</b>. When the operation is finished, the specified event is set to the signaled
        state.

When you specify <b>FILE_FLAG_OVERLAPPED</b>, the file read and write functions 
         <b>must</b> specify an 
         <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. That is, when 
         <b>FILE_FLAG_OVERLAPPED</b> is specified, an application <b>must</b> 
         perform overlapped reading and writing.

When <b>FILE_FLAG_OVERLAPPED</b> is specified, the system does not maintain the file 
         pointer. The file position must be passed as part of the <i>lpOverlapped</i> parameter 
         (pointing to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure) to the file 
         read and write functions.

This flag also enables more than one operation to be performed simultaneously with the handle (a 
         simultaneous read and write operation, for example).

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_POSIX_SEMANTICS"></a><a id="file_flag_posix_semantics"></a><dl>
<dt><b>FILE_FLAG_POSIX_SEMANTICS</b></dt>
<dt>0x01000000</dt>
</dl>
</td>
<td width="60%">
Indicates that the file is to be accessed according to POSIX rules. This includes allowing multiple files 
         with names, differing only in case, for file systems that support such naming. Use care when using this 
         option because files created with this flag may not be accessible by applications written for MS-DOS or 
         16-bit Windows.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_RANDOM_ACCESS"></a><a id="file_flag_random_access"></a><dl>
<dt><b>FILE_FLAG_RANDOM_ACCESS</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
Indicates that the file is accessed randomly. The system can use this as a hint to optimize file 
         caching.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_SEQUENTIAL_SCAN"></a><a id="file_flag_sequential_scan"></a><dl>
<dt><b>FILE_FLAG_SEQUENTIAL_SCAN</b></dt>
<dt>0x08000000</dt>
</dl>
</td>
<td width="60%">
Indicates that the file is to be accessed sequentially from beginning to end. The system can use this as a 
         hint to optimize file caching. If an application moves the file pointer for random access, optimum caching 
         may not occur; however, correct operation is still guaranteed.

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
Instructs the system to write through any intermediate cache and go directly to disk. The system can still 
         cache write operations, but cannot lazily flush them.

</td>
</tr>
</table>
 

If the handle represents the client side of a named pipe, the <i>dwFlags</i> parameter can 
       also contain Security Quality of Service information. For more information, see 
       <a href="/windows/desktop/SecAuthZ/impersonation-levels">Impersonation Levels</a>. When the calling 
       application specifies the <b>SECURITY_SQOS_PRESENT</b> flag, the 
       <i>dwFlags</i> parameter can contain one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SECURITY_ANONYMOUS"></a><a id="security_anonymous"></a><dl>
<dt><b>SECURITY_ANONYMOUS</b></dt>
</dl>
</td>
<td width="60%">
Impersonate the client at the Anonymous impersonation level.

</td>
</tr>
<tr>
<td width="40%"><a id="SECURITY_CONTEXT_TRACKING"></a><a id="security_context_tracking"></a><dl>
<dt><b>SECURITY_CONTEXT_TRACKING</b></dt>
</dl>
</td>
<td width="60%">
The security tracking mode is dynamic. If this flag is not specified, the security tracking mode is 
         static.

</td>
</tr>
<tr>
<td width="40%"><a id="SECURITY_DELEGATION"></a><a id="security_delegation"></a><dl>
<dt><b>SECURITY_DELEGATION</b></dt>
</dl>
</td>
<td width="60%">
Impersonate the client at the Delegation impersonation level.

</td>
</tr>
<tr>
<td width="40%"><a id="SECURITY_EFFECTIVE_ONLY"></a><a id="security_effective_only"></a><dl>
<dt><b>SECURITY_EFFECTIVE_ONLY</b></dt>
</dl>
</td>
<td width="60%">
Only the enabled aspects of the client security context are available to the server. If you do not specify 
         this flag, all aspects of the client security context are available.

This allows the client to limit the groups and privileges that a server can use while impersonating the 
         client.

</td>
</tr>
<tr>
<td width="40%"><a id="SECURITY_IDENTIFICATION"></a><a id="security_identification"></a><dl>
<dt><b>SECURITY_IDENTIFICATION</b></dt>
</dl>
</td>
<td width="60%">
Impersonate the client at the Identification impersonation level.

</td>
</tr>
<tr>
<td width="40%"><a id="SECURITY_IMPERSONATION"></a><a id="security_impersonation"></a><dl>
<dt><b>SECURITY_IMPERSONATION</b></dt>
</dl>
</td>
<td width="60%">
Impersonate the client at the Impersonation impersonation level.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is an open handle to the specified file.

If the function fails, the return value is <b>INVALID_HANDLE_VALUE</b>. To get extended 
       error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <i>dwFlags</i> parameter cannot contain any of the file attribute flags 
    (<b>FILE_ATTRIBUTE_*</b>). These can only be specified when the file is created.

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

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>