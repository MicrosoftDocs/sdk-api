---
UID: NF:winbase.OpenFileById
title: OpenFileById function
author: windows-sdk-content
description: Opens the file that matches the specified identifier.
old-location: fs\openfilebyid.htm
old-project: FileIO
ms.assetid: caa757a2-fc3f-4883-8d3e-b98d28f92517
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: FILE_FLAG_BACKUP_SEMANTICS, FILE_FLAG_NO_BUFFERING, FILE_FLAG_OPEN_NO_RECALL, FILE_FLAG_OPEN_REPARSE_POINT, FILE_FLAG_OVERLAPPED, FILE_FLAG_RANDOM_ACCESS, FILE_FLAG_SEQUENTIAL_SCAN, FILE_FLAG_WRITE_THROUGH, FILE_SHARE_DELETE, FILE_SHARE_READ, FILE_SHARE_WRITE, OpenFileById, OpenFileById function [Files], fileextd/OpenFileById, fs.openfilebyid, winbase/OpenFileById
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-File-l2-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l2-1-2.dll
api_name:
 - OpenFileById
product: Windows
targetos: Windows
req.lib: Kernel32.lib; FileExtd.lib on Windows Server 2003 and Windows XP
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# OpenFileById function


## -description


Opens the file that matches the specified identifier.


## -parameters




### -param hVolumeHint

TBD


### -param lpFileId

TBD


### -param dwDesiredAccess [in]

The access to the object. Access can be read, write, or both.

For more information, see 
      <a href="https://msdn.microsoft.com/991d7d94-fae7-406f-b2e3-dee811279366">File Security and Access
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
       <a href="https://msdn.microsoft.com/094cac29-c66d-409e-8928-878dc693d393">Creating and Opening Files</a>.

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


### -param dwFlagsAndAttributes

TBD




#### - dwFlags [in]

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
         <a href="https://msdn.microsoft.com/b8e47d04-07c1-4d57-8209-6b0c397476e5">Changing Privileges in a Token</a>.

You must set this flag to obtain a handle to a directory. A directory handle can be passed to some 
         functions  instead of a file handle. For more information, see 
         <a href="https://msdn.microsoft.com/841c7daa-360c-4d96-8a14-6dcfa159a875">Directory Handles</a>.

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
         the metadata to disk, use the <a href="https://msdn.microsoft.com/0d9ea467-6d5d-44b2-8e87-f2ecdd510fe6">FlushFileBuffers</a> 
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
         <a href="https://msdn.microsoft.com/a720dd89-c47c-4e48-bbc6-f2e02dfc4ed2">VirtualAlloc</a> to allocate the buffers. It allocates 
         memory that is aligned on addresses that are integer multiples of the operating system's memory page size. 
         Because both memory page and volume sector sizes are powers of 2, this memory is also aligned on addresses 
         that are integer multiples of a volume sector size. Memory pages are 4-8 KB in size; sectors are 512 bytes 
         (hard disks) or 2048 bytes (CD), and therefore, volume sectors can never be larger than memory pages.

An application can determine a volume sector size by calling the 
         <a href="https://msdn.microsoft.com/4fe14c49-3fd6-48b7-92de-a0c867b2e042">GetDiskFreeSpace</a> function.

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
When this flag is used, normal <a href="https://msdn.microsoft.com/3abb3a08-9a00-43eb-9792-82eab1a25f06">reparse point</a> 
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
         specified to the call in the <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure is 
         set to the signaled state. Operations that take a significant amount of time to process return 
         <b>ERROR_IO_PENDING</b>.

If this flag is specified, the file can be used for simultaneous read and write operations. The system does 
         not maintain the file pointer, therefore you must pass the file position to the read and write functions in 
         the <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>  structure or update the file 
         pointer.

If this flag is not specified, then I/O operations are serialized, even if the calls to the read and write 
         functions specify an <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure.

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
 


#### - hFile [in]

A handle to any file on a volume or share on which the file to be opened is stored.


#### - lpFileID [in]

A pointer to a <a href="https://msdn.microsoft.com/9092a701-3b47-4c4c-8221-54fa3220d322">FILE_ID_DESCRIPTOR</a> that identifies 
       the file to open.


## -returns



If the function succeeds, the return value is an open handle to a specified file.

If the function fails, the return value is <b>INVALID_HANDLE_VALUE</b>. To get extended 
       error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Use the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function to close an object handle 
    that <b>OpenFileById</b> returns.

If you call <b>OpenFileById</b> on a file that is pending 
    deletion as a result of a previous call to <a href="https://msdn.microsoft.com/0b947a85-816b-4374-a8f8-c369e366a17d">DeleteFile</a>, the 
    function fails. The operating system delays file deletion until all handles to the file are closed. 
    <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns 
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




<a href="https://msdn.microsoft.com/library/windows/hardware/ff540466">ACCESS_MASK</a>



<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/0b947a85-816b-4374-a8f8-c369e366a17d">DeleteFile</a>



<a href="https://msdn.microsoft.com/9092a701-3b47-4c4c-8221-54fa3220d322">FILE_ID_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>



<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>



<a href="https://msdn.microsoft.com/800f4d40-252a-44fe-b10d-348c22d69355">OpenFile</a>



<a href="https://msdn.microsoft.com/4ad4580d-c002-44a4-a5f6-757e83ed8732">ReadFile</a>



<a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a>
 

 

