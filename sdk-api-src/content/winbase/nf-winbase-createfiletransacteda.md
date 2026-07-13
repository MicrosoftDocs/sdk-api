---
UID: NF:winbase.CreateFileTransactedA
title: CreateFileTransactedA function (winbase.h)
description: Creates or opens a file, file stream, or directory as a transacted operation. (ANSI)
helpviewer_keywords: ["0", "CREATE_ALWAYS", "CREATE_NEW", "CreateFileTransactedA", "FILE_ATTRIBUTE_ARCHIVE", "FILE_ATTRIBUTE_ENCRYPTED", "FILE_ATTRIBUTE_HIDDEN", "FILE_ATTRIBUTE_NORMAL", "FILE_ATTRIBUTE_OFFLINE", "FILE_ATTRIBUTE_READONLY", "FILE_ATTRIBUTE_SYSTEM", "FILE_ATTRIBUTE_TEMPORARY", "FILE_FLAG_BACKUP_SEMANTICS", "FILE_FLAG_DELETE_ON_CLOSE", "FILE_FLAG_NO_BUFFERING", "FILE_FLAG_OPEN_NO_RECALL", "FILE_FLAG_OPEN_REPARSE_POINT", "FILE_FLAG_OVERLAPPED", "FILE_FLAG_POSIX_SEMANTICS", "FILE_FLAG_RANDOM_ACCESS", "FILE_FLAG_SEQUENTIAL_SCAN", "FILE_FLAG_SESSION_AWARE", "FILE_FLAG_WRITE_THROUGH", "FILE_SHARE_DELETE", "FILE_SHARE_READ", "FILE_SHARE_WRITE", "OPEN_ALWAYS", "OPEN_EXISTING", "SECURITY_ANONYMOUS", "SECURITY_CONTEXT_TRACKING", "SECURITY_DELEGATION", "SECURITY_EFFECTIVE_ONLY", "SECURITY_IDENTIFICATION", "SECURITY_IMPERSONATION", "TRUNCATE_EXISTING", "TXFS_MINIVERSION_COMMITTED_VIEW", "TXFS_MINIVERSION_DEFAULT_VIEW", "TXFS_MINIVERSION_DIRTY_VIEW", "winbase/CreateFileTransactedA"]
old-location: fs\createfiletransacted.htm
tech.root: fs
ms.assetid: 0cbc081d-8787-409b-84bc-a6a28d8f83a0
ms.date: 12/05/2018
ms.keywords: 0, CREATE_ALWAYS, CREATE_NEW, CreateFileTransacted, CreateFileTransacted function [Files], CreateFileTransactedA, CreateFileTransactedW, FILE_ATTRIBUTE_ARCHIVE, FILE_ATTRIBUTE_ENCRYPTED, FILE_ATTRIBUTE_HIDDEN, FILE_ATTRIBUTE_NORMAL, FILE_ATTRIBUTE_OFFLINE, FILE_ATTRIBUTE_READONLY, FILE_ATTRIBUTE_SYSTEM, FILE_ATTRIBUTE_TEMPORARY, FILE_FLAG_BACKUP_SEMANTICS, FILE_FLAG_DELETE_ON_CLOSE, FILE_FLAG_NO_BUFFERING, FILE_FLAG_OPEN_NO_RECALL, FILE_FLAG_OPEN_REPARSE_POINT, FILE_FLAG_OVERLAPPED, FILE_FLAG_POSIX_SEMANTICS, FILE_FLAG_RANDOM_ACCESS, FILE_FLAG_SEQUENTIAL_SCAN, FILE_FLAG_SESSION_AWARE, FILE_FLAG_WRITE_THROUGH, FILE_SHARE_DELETE, FILE_SHARE_READ, FILE_SHARE_WRITE, OPEN_ALWAYS, OPEN_EXISTING, SECURITY_ANONYMOUS, SECURITY_CONTEXT_TRACKING, SECURITY_DELEGATION, SECURITY_EFFECTIVE_ONLY, SECURITY_IDENTIFICATION, SECURITY_IMPERSONATION, TRUNCATE_EXISTING, TXFS_MINIVERSION_COMMITTED_VIEW, TXFS_MINIVERSION_DEFAULT_VIEW, TXFS_MINIVERSION_DIRTY_VIEW, fs.createfiletransacted, winbase/CreateFileTransacted, winbase/CreateFileTransactedA, winbase/CreateFileTransactedW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateFileTransactedW (Unicode) and CreateFileTransactedA (ANSI)
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
 - CreateFileTransactedA
 - winbase/CreateFileTransactedA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-Ms-Win-Core-Kernel32-Legacy-Ansi-L1-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - CreateFileTransacted
 - CreateFileTransactedA
 - CreateFileTransactedW
---

# CreateFileTransactedA function


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Creates or opens a file, file stream, or directory as a transacted operation. The function 
    returns a handle that can be used to access the object.

To perform this operation as a nontransacted 
    operation or to access objects other than files (for example, named pipes, physical devices, mailslots), use the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function.

For more information about transactions, see the Remarks section of this topic.

## -parameters

### -param lpFileName [in]

The name of an object to be created or opened.

The object must reside on the local computer; otherwise, 
       the function fails and the last error code is set to 
       <b>ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE</b>.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

To create a file stream, specify the name of the file, a colon, and then the name of the stream. For more 
       information, see <a href="/windows/desktop/FileIO/file-streams">File Streams</a>.

### -param dwDesiredAccess [in]

The access to the object, which can be  summarized as read, write, both or neither (zero). The most commonly 
       used values are <b>GENERIC_READ</b>, <b>GENERIC_WRITE</b>, or both 
       (<b>GENERIC_READ</b> | <b>GENERIC_WRITE</b>). For more information, see 
       <a href="/windows/desktop/SecAuthZ/generic-access-rights">Generic Access Rights</a> and 
       <a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

If this parameter is zero, the application can query  file, directory, or device attributes without accessing 
       that file or device. For more information, see the Remarks section of this topic.

You cannot request an access mode that conflicts with the sharing mode that is specified in an open request 
       that has an open handle. For more information, see 
       <a href="/windows/desktop/FileIO/creating-and-opening-files">Creating and Opening Files</a>.

### -param dwShareMode [in]

The sharing mode of an object, which can be read, write, both, delete, all of these, or none (refer to the 
       following table).

If this parameter is zero and 
       <b>CreateFileTransacted</b> succeeds, the object cannot 
       be shared and cannot be opened again until the handle is closed. For more information, see the Remarks section 
       of this topic.

You cannot request a sharing mode that conflicts with the access mode that is specified in an open request 
       that has an open handle, because that would result in the following sharing violation: 
       <b>ERROR_SHARING_VIOLATION</b>. For more information, see 
       <a href="/windows/desktop/FileIO/creating-and-opening-files">Creating and Opening Files</a>.

To enable a process to share an object while another process has the object open, use a combination of one or 
       more of the following values to specify the  access mode they can request to open the object.

<div class="alert"><b>Note</b>  The sharing options for each open handle remain in effect until that handle is closed, regardless of 
       process context.</div>
<div> </div>
<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Disables subsequent open operations on an object to request any type of access to that object.

</td>
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

A pointer to a <a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> 
       structure that contains an optional 
       <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">security descriptor</a> and also determines whether 
       or not the returned handle can be inherited by child processes. The parameter can be 
       <b>NULL</b>.

If the <i>lpSecurityAttributes</i> parameter is <b>NULL</b>, the handle 
       returned by <b>CreateFileTransacted</b> cannot be 
       inherited by any child processes your application may create and the object associated with the returned handle 
       gets a default security descriptor.

The <b>bInheritHandle</b> member of the structure specifies whether the returned handle 
       can be inherited.

The  <b>lpSecurityDescriptor</b> member of the structure specifies 
       a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">security descriptor</a> for an object, but may 
       also be <b>NULL</b>.

If <b>lpSecurityDescriptor</b> member is <b>NULL</b>, the object 
       associated with the returned handle is assigned a default security descriptor.

<b>CreateFileTransacted</b> ignores the 
       <b>lpSecurityDescriptor</b> member when opening an existing file, but continues to use the 
       <b>bInheritHandle</b> member.

For more information, see the Remarks section of this topic.

### -param dwCreationDisposition [in]

An action to take on files that exist and  do not exist.

For more information, see the Remarks section of this topic.

This parameter must be one of the following values, which cannot be combined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CREATE_ALWAYS"></a><a id="create_always"></a><dl>
<dt><b>CREATE_ALWAYS</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Creates a new file, always.

If the specified  file exists and is writable, the function truncates the file, the function succeeds, and 
         last-error code is set to <b>ERROR_ALREADY_EXISTS</b> (183).

If the specified file does not exist and is a valid path, a new file is created, the function succeeds, and 
         the last-error code is set to zero.

For more information, see the Remarks section of this topic.

</td>
</tr>
<tr>
<td width="40%"><a id="CREATE_NEW"></a><a id="create_new"></a><dl>
<dt><b>CREATE_NEW</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Creates a new file, only if it does not already exist.

If the specified file exists, the function fails and the last-error code is set to 
         <b>ERROR_FILE_EXISTS</b> (80).

If the specified file does not exist and is a valid path to a writable location, a new file is created.

</td>
</tr>
<tr>
<td width="40%"><a id="OPEN_ALWAYS"></a><a id="open_always"></a><dl>
<dt><b>OPEN_ALWAYS</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Opens a file, always.

If the specified file exists, the function succeeds and the last-error code is set to 
         <b>ERROR_ALREADY_EXISTS</b> (183).

If the specified file does not exist and is a valid path to a writable location, the function creates a 
         file and the last-error code is set to zero.

</td>
</tr>
<tr>
<td width="40%"><a id="OPEN_EXISTING"></a><a id="open_existing"></a><dl>
<dt><b>OPEN_EXISTING</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Opens a file or device, only if it exists.

If the specified file does not exist, the function fails and the last-error code is set to 
         <b>ERROR_FILE_NOT_FOUND</b> (2).

For more information, see the Remarks section of this topic.

</td>
</tr>
<tr>
<td width="40%"><a id="TRUNCATE_EXISTING"></a><a id="truncate_existing"></a><dl>
<dt><b>TRUNCATE_EXISTING</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Opens a file and truncates it so that its size is zero bytes, only if it exists.

If the specified file does not exist, the function fails and the last-error code is set to 
         <b>ERROR_FILE_NOT_FOUND</b> (2).

The calling process must open the file with the <b>GENERIC_WRITE</b> bit set as part of 
         the <i>dwDesiredAccess</i> parameter.

</td>
</tr>
</table>

### -param dwFlagsAndAttributes [in]

The file attributes and flags, <b>FILE_ATTRIBUTE_NORMAL</b> being the most common default 
       value.

This parameter can include any combination of the available file attributes 
       (<b>FILE_ATTRIBUTE_*</b>). All other file attributes override 
       <b>FILE_ATTRIBUTE_NORMAL</b>.

This parameter can also contain combinations of flags (<b>FILE_FLAG_*</b>) for control of 
       buffering behavior, access modes, and other special-purpose flags. These combine with any 
       <b>FILE_ATTRIBUTE_*</b> values.

This parameter can also contain Security Quality of Service (SQOS) information by specifying the 
       <b>SECURITY_SQOS_PRESENT</b> flag. Additional SQOS-related flags information is presented in 
       the table following the attributes and flags tables.

<div class="alert"><b>Note</b>  <p class="note">When <b>CreateFileTransacted</b> opens an existing 
        file, it generally combines the file flags with the file attributes of the existing file, and ignores any file 
        attributes supplied as part of <i>dwFlagsAndAttributes</i>. Special cases are detailed in 
        <a href="/windows/desktop/FileIO/creating-and-opening-files">Creating and Opening Files</a>.

</div>
<div> </div>
The following file attributes and flags are used only for file objects, not other types of objects that 
       <b>CreateFileTransacted</b> opens (additional 
       information can be found in the Remarks section of this topic). For more advanced access to file attributes, 
       see <a href="/windows/desktop/api/fileapi/nf-fileapi-setfileattributesa">SetFileAttributes</a>. For a complete list of all 
       file attributes with their values and descriptions, see 
       <a href="/windows/desktop/FileIO/file-attribute-constants">File Attribute Constants</a>.

<table>
<tr>
<th>Attribute</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_ATTRIBUTE_ARCHIVE"></a><a id="file_attribute_archive"></a><dl>
<dt><b>FILE_ATTRIBUTE_ARCHIVE</b></dt>
<dt>32 (0x20)</dt>
</dl>
</td>
<td width="60%">
The file should be archived. Applications use this attribute to mark files for backup or removal.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ATTRIBUTE_ENCRYPTED"></a><a id="file_attribute_encrypted"></a><dl>
<dt><b>FILE_ATTRIBUTE_ENCRYPTED</b></dt>
<dt>16384 (0x4000)</dt>
</dl>
</td>
<td width="60%">
The file or directory is encrypted. For a file, this means that all data in the file is encrypted. For a 
         directory, this means that encryption is the default for newly created files and subdirectories. For more 
         information, see <a href="/windows/desktop/FileIO/file-encryption">File Encryption</a>.

This flag has no effect if <b>FILE_ATTRIBUTE_SYSTEM</b> is also specified.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ATTRIBUTE_HIDDEN"></a><a id="file_attribute_hidden"></a><dl>
<dt><b>FILE_ATTRIBUTE_HIDDEN</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
The file is hidden. Do not include it in an ordinary directory listing.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ATTRIBUTE_NORMAL"></a><a id="file_attribute_normal"></a><dl>
<dt><b>FILE_ATTRIBUTE_NORMAL</b></dt>
<dt>128 (0x80)</dt>
</dl>
</td>
<td width="60%">
The file does not have other attributes set. This attribute is valid only if used alone.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ATTRIBUTE_OFFLINE"></a><a id="file_attribute_offline"></a><dl>
<dt><b>FILE_ATTRIBUTE_OFFLINE</b></dt>
<dt>4096 (0x1000)</dt>
</dl>
</td>
<td width="60%">
The data of a file is not immediately available. This attribute indicates that file data is physically 
         moved to offline storage. This attribute is used by Remote Storage, the hierarchical storage management 
         software. Applications should not arbitrarily change this attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ATTRIBUTE_READONLY"></a><a id="file_attribute_readonly"></a><dl>
<dt><b>FILE_ATTRIBUTE_READONLY</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
The file is read only. Applications can read the file, but cannot write to or delete it.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ATTRIBUTE_SYSTEM"></a><a id="file_attribute_system"></a><dl>
<dt><b>FILE_ATTRIBUTE_SYSTEM</b></dt>
<dt>4 (0x4)</dt>
</dl>
</td>
<td width="60%">
The file is part of or used exclusively by an operating system.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ATTRIBUTE_TEMPORARY"></a><a id="file_attribute_temporary"></a><dl>
<dt><b>FILE_ATTRIBUTE_TEMPORARY</b></dt>
<dt>256 (0x100)</dt>
</dl>
</td>
<td width="60%">
The file is being used for temporary storage.  File systems avoid writing data back to mass storage 
         if sufficient cache memory is available, because an application deletes a temporary file after a handle is 
         closed. In that case, the system can entirely avoid writing the data.  Otherwise, the data is written after 
         the handle is closed.

</td>
</tr>
</table>
 

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_BACKUP_SEMANTICS"></a><a id="file_flag_backup_semantics"></a><dl>
<dt><b>FILE_FLAG_BACKUP_SEMANTICS</b></dt>
<dt>0x02000000</dt>
</dl>
</td>
<td width="60%">
The file is being opened or created for a backup or restore operation. The system ensures that the 
         calling process overrides file security checks when the process has <b>SE_BACKUP_NAME</b> 
         and <b>SE_RESTORE_NAME</b> privileges. For more information, see 
         <a href="/windows/desktop/SecBP/changing-privileges-in-a-token">Changing Privileges in a Token</a>.

You must set this flag to obtain a handle to a directory. A directory handle can be passed to some 
         functions instead of a file handle. For more information, see 
         <a href="/windows/desktop/FileIO/obtaining-a-handle-to-a-directory">Directory Handles</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_DELETE_ON_CLOSE"></a><a id="file_flag_delete_on_close"></a><dl>
<dt><b>FILE_FLAG_DELETE_ON_CLOSE</b></dt>
<dt>0x04000000</dt>
</dl>
</td>
<td width="60%">
The file is to be deleted immediately after the last transacted writer handle to the file is closed, 
         provided that the transaction is still active. If a file has been marked for deletion and a transacted writer 
         handle is still open after the transaction completes, the file will not be deleted.

If there are existing open handles to a file, the call fails unless they were all opened with the 
         <b>FILE_SHARE_DELETE</b> share mode.

Subsequent open requests for the file fail, unless the <b>FILE_SHARE_DELETE</b> share 
         mode is specified.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_NO_BUFFERING"></a><a id="file_flag_no_buffering"></a><dl>
<dt><b>FILE_FLAG_NO_BUFFERING</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
The file is being opened with no system caching. This flag does not affect hard disk caching or memory 
         mapped files. When combined with <b>FILE_FLAG_OVERLAPPED</b>, the flag gives maximum 
         asynchronous performance, because the I/O does not rely on the synchronous operations of the memory manager. 
         However, some I/O operations take more time, because data is not being held in the cache. Also, the file 
         metadata may still be cached. To flush the metadata to disk, use the 
         <a href="/windows/desktop/api/fileapi/nf-fileapi-flushfilebuffers">FlushFileBuffers</a> function.

An application must meet certain requirements when working with files that are opened with 
         <b>FILE_FLAG_NO_BUFFERING</b>:

<ul>
<li>File access must begin at byte offsets within a file that are integer multiples of the volume sector 
          size.</li>
<li>File access must be for numbers of bytes that are integer multiples of the volume sector size. For 
          example, if the sector size is 512 bytes, an application can request reads and writes of 512, 1024, 1536, 
          or 2048 bytes, but not of 335, 981, or 7171 bytes.</li>
<li>Buffer addresses for read and write operations should be sector aligned, which means aligned on 
          addresses in memory that are integer multiples of the volume sector size. Depending on the disk, this 
          requirement may not be enforced.</li>
</ul>
One way to align buffers on integer multiples of the volume sector size is to use 
         <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a> to allocate the buffers. It allocates 
         memory that is aligned on addresses that are integer multiples of the operating system's memory page size. 
         Because both memory page and volume sector sizes are powers of 2, this memory is also aligned on addresses 
         that are integer multiples of a volume sector size. Memory pages are 4 or 8 KB in size; sectors are 512 bytes 
         (hard disks), 2048 bytes (CD), or 4096 bytes (hard disks), and therefore, volume sectors can never be larger 
         than memory pages.

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
Normal <a href="/windows/desktop/FileIO/reparse-points">reparse point</a> processing will not occur; 
         <b>CreateFileTransacted</b> will attempt to open the 
         reparse point. When a file is opened, a file handle is returned, whether or not the filter that controls the 
         reparse point is operational. This flag cannot be used with the <b>CREATE_ALWAYS</b> 
         flag. If the file is not a reparse point, then this flag is ignored.

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
         specified in the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure is set to the 
         signaled state. Operations that take a significant amount of time to process return 
         <b>ERROR_IO_PENDING</b>.

If this flag is specified, the file can be used for simultaneous read and write operations. The system does 
         not maintain the file pointer, therefore you must pass the file position to the read and write functions in 
         the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure or update the file 
         pointer.

If this flag is not specified, then I/O operations are serialized, even if the calls to the read and write 
         functions specify an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_POSIX_SEMANTICS"></a><a id="file_flag_posix_semantics"></a><dl>
<dt><b>FILE_FLAG_POSIX_SEMANTICS</b></dt>
<dt>0x01000000</dt>
</dl>
</td>
<td width="60%">
The file is to be accessed according to POSIX rules. This includes allowing multiple files with names, 
         differing only in case, for file systems that support that naming. Use care when using this option, because 
         files created with this flag may not be accessible by applications that are written for MS-DOS or 16-bit 
         Windows.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_RANDOM_ACCESS"></a><a id="file_flag_random_access"></a><dl>
<dt><b>FILE_FLAG_RANDOM_ACCESS</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
The file is to be accessed randomly. The system can use this as a hint to optimize file caching.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_SESSION_AWARE"></a><a id="file_flag_session_aware"></a><dl>
<dt><b>FILE_FLAG_SESSION_AWARE</b></dt>
<dt>0x00800000</dt>
</dl>
</td>
<td width="60%">
The file or device is being opened with session awareness. If this flag is not specified, then per-session 
         devices (such as a device using RemoteFX USB Redirection) cannot be opened by processes running in session 0. 
         This flag has no effect for callers not in session 0. This flag is supported only on server editions of 
         Windows.

<b>Windows Server 2008 R2 and Windows Server 2008:  </b>This flag is not supported before Windows Server 2012.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_SEQUENTIAL_SCAN"></a><a id="file_flag_sequential_scan"></a><dl>
<dt><b>FILE_FLAG_SEQUENTIAL_SCAN</b></dt>
<dt>0x08000000</dt>
</dl>
</td>
<td width="60%">
The file is to be accessed sequentially from beginning to end. The system can use this as a hint to 
         optimize file caching. If an application moves the file pointer for random access, optimum caching may not 
         occur. However, correct operation is still guaranteed.

Specifying this flag can increase performance for applications that read large files using sequential 
         access. Performance gains can be even more noticeable for applications that read large files mostly 
         sequentially, but occasionally skip over small ranges of bytes.

This flag  has no effect if the file system does not support cached I/O and 
         <b>FILE_FLAG_NO_BUFFERING</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_WRITE_THROUGH"></a><a id="file_flag_write_through"></a><dl>
<dt><b>FILE_FLAG_WRITE_THROUGH</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
Write operations will not go through any intermediate cache, they will go directly to disk.

If <b>FILE_FLAG_NO_BUFFERING</b> is not also specified, so that system caching is in 
         effect, then the data is written to the system cache, but is flushed to disk without delay.

If <b>FILE_FLAG_NO_BUFFERING</b> is also specified, so that system caching is not in 
         effect, then the data is immediately flushed to disk without going through the system cache. The operating 
         system also requests a write-through the hard disk cache to persistent media. However, not all hardware 
         supports this write-through capability.

</td>
</tr>
</table>
 

The <i>dwFlagsAndAttributes</i> parameter can also specify Security Quality of Service 
       information. For more information, see 
       <a href="/windows/desktop/SecAuthZ/impersonation-levels">Impersonation Levels</a>. When the calling 
       application specifies the <b>SECURITY_SQOS_PRESENT</b> flag as part of 
       <i>dwFlagsAndAttributes</i>, it can also contain one or more of the following values.

<table>
<tr>
<th>Security flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SECURITY_ANONYMOUS"></a><a id="security_anonymous"></a><dl>
<dt><b>SECURITY_ANONYMOUS</b></dt>
</dl>
</td>
<td width="60%">
Impersonates a client at the Anonymous impersonation level.

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
Impersonates a client at the Delegation impersonation level.

</td>
</tr>
<tr>
<td width="40%"><a id="SECURITY_EFFECTIVE_ONLY"></a><a id="security_effective_only"></a><dl>
<dt><b>SECURITY_EFFECTIVE_ONLY</b></dt>
</dl>
</td>
<td width="60%">
Only the enabled aspects of the client's security context are available to the server. If you do not 
         specify this flag, all aspects of the client's security context are available.

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
Impersonates a client at the Identification impersonation level.

</td>
</tr>
<tr>
<td width="40%"><a id="SECURITY_IMPERSONATION"></a><a id="security_impersonation"></a><dl>
<dt><b>SECURITY_IMPERSONATION</b></dt>
</dl>
</td>
<td width="60%">
Impersonate a client at the impersonation level. This is the default behavior if no other flags are 
         specified along with the <b>SECURITY_SQOS_PRESENT</b> flag.

</td>
</tr>
</table>

### -param hTemplateFile [in, optional]

A valid handle to a template file with the <b>GENERIC_READ</b> access right. The template 
       file supplies file attributes and extended attributes for the file that is being created. This parameter can be 
       <b>NULL</b>.

When opening an existing file, 
       <b>CreateFileTransacted</b> ignores the template 
       file.

When opening a new EFS-encrypted file, the file inherits the DACL from its parent directory.

### -param hTransaction [in]

A handle to the transaction. This handle is returned by the 
       <a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a> function.

### -param pusMiniVersion [in, optional]

The miniversion to be opened. If the transaction specified in <i>hTransaction</i> is not 
       the transaction that is modifying the file, this parameter should be <b>NULL</b>. Otherwise, 
       this parameter can be a miniversion identifier returned by the 
       <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_txfs_create_miniversion">FSCTL_TXFS_CREATE_MINIVERSION</a> control 
       code, or one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TXFS_MINIVERSION_COMMITTED_VIEW"></a><a id="txfs_miniversion_committed_view"></a><dl>
<dt><b>TXFS_MINIVERSION_COMMITTED_VIEW</b></dt>
<dt>0x0000</dt>
</dl>
</td>
<td width="60%">
The view of the file as of its last commit.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_MINIVERSION_DIRTY_VIEW"></a><a id="txfs_miniversion_dirty_view"></a><dl>
<dt><b>TXFS_MINIVERSION_DIRTY_VIEW</b></dt>
<dt>0xFFFF</dt>
</dl>
</td>
<td width="60%">
The view of the file as it is being modified by the transaction.

</td>
</tr>
<tr>
<td width="40%"><a id="TXFS_MINIVERSION_DEFAULT_VIEW"></a><a id="txfs_miniversion_default_view"></a><dl>
<dt><b>TXFS_MINIVERSION_DEFAULT_VIEW</b></dt>
<dt>0xFFFE</dt>
</dl>
</td>
<td width="60%">
Either the committed or dirty view of the file, depending on the context. A transaction that is modifying 
        the file gets the dirty view, while a transaction that is not modifying the file gets the committed 
        view.

</td>
</tr>
</table>

### -param lpExtendedParameter

This parameter is reserved and must be <b>NULL</b>.

## -returns

If the function succeeds, the return value is an open handle to the specified file, device, named pipe, or 
       mail slot.

If the function fails, the return value is <b>INVALID_HANDLE_VALUE</b>. To get extended 
       error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

When using the handle returned by 
     <b>CreateFileTransacted</b>, use the transacted version 
     of file I/O functions instead of the standard file I/O functions where appropriate. For more information, see 
     <a href="/windows/desktop/FileIO/programming-considerations-for-transacted-fileio-">Programming Considerations for 
     Transactional NTFS</a>.

When opening a transacted handle to a directory, that handle must have 
     <b>FILE_WRITE_DATA</b> (<b>FILE_ADD_FILE</b>) and 
     <b>FILE_APPEND_DATA</b> (<b>FILE_ADD_SUBDIRECTORY</b>) permissions. These 
     are included in <b>FILE_GENERIC_WRITE</b> permissions. You should open directories with fewer 
     permissions if you are just using the handle to create files or subdirectories; otherwise, sharing violations can 
     occur.

You cannot open a file with <b>FILE_EXECUTE</b> access level when that file is a part of 
     another transaction (that is, another application opened it by calling 
     <b>CreateFileTransacted</b>).  This means that 
     <b>CreateFileTransacted</b> fails if the access level 
     <b>FILE_EXECUTE</b> or <b>FILE_ALL_ACCESS</b> is specified

When a non-transacted application calls 
     <b>CreateFileTransacted</b> with 
     <b>MAXIMUM_ALLOWED</b> specified for <i>lpSecurityAttributes</i>, a handle 
     is opened with the same access level every time.  When a transacted application calls 
     <b>CreateFileTransacted</b> with 
     <b>MAXIMUM_ALLOWED</b> specified for <i>lpSecurityAttributes</i>, a handle 
     is opened with a differing amount of access based on whether the file is locked by a transaction. For example, 
     if the calling application has <b>FILE_EXECUTE</b> access level for a file, the application 
     only obtains this access if the file that is being opened is either not locked by a transaction, or is locked by 
     a transaction and the application is already a transacted reader for that file.

See <a href="/windows/desktop/FileIO/transactional-ntfs-portal">Transactional NTFS</a> for a complete 
     description of transacted operations.

Use the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to close an object handle 
     returned by <b>CreateFileTransacted</b> when the handle 
     is no longer needed, and prior to committing or rolling back the transaction.

Some file systems, such as the NTFS file system, support compression or encryption for individual files and 
     directories. On volumes that are formatted for that kind of file system, a new file inherits the compression and 
     encryption attributes of its directory.

You cannot use <b>CreateFileTransacted</b> to control 
     compression on a file or directory. For more information, see 
     <a href="/windows/desktop/FileIO/file-compression-and-decompression">File Compression and Decompression</a>, and 
     <a href="/windows/desktop/FileIO/file-encryption">File Encryption</a>.

Symbolic link behavior—If the call to this function creates a new file, there is no change 
     in behavior.

If <b>FILE_FLAG_OPEN_REPARSE_POINT</b> is specified:

<ul>
<li>If an existing file is opened and it is a symbolic link, the handle returned is a handle to the symbolic 
       link.</li>
<li>If <b>TRUNCATE_EXISTING</b> or <b>FILE_FLAG_DELETE_ON_CLOSE</b> are 
       specified, the file affected is a symbolic link.</li>
</ul>
If <b>FILE_FLAG_OPEN_REPARSE_POINT</b> is not specified:

<ul>
<li>If an existing file is opened and it is a symbolic link, the handle returned is a handle to the 
       target.</li>
<li>If <b>CREATE_ALWAYS</b>, <b>TRUNCATE_EXISTING</b>, or 
       <b>FILE_FLAG_DELETE_ON_CLOSE</b> are specified, the file affected is the target.</li>
</ul>
A multi-sector write is not guaranteed to be atomic unless you are using a transaction (that is, the handle 
    created is a transacted handle).  A single-sector write is atomic. Multi-sector writes that are cached may not 
    always be written to the disk; therefore, specify <b>FILE_FLAG_WRITE_THROUGH</b> to ensure that 
    an entire multi-sector write is written to the disk without caching.

As stated previously, if the <i>lpSecurityAttributes</i> parameter is 
     <b>NULL</b>, the handle returned by 
     <b>CreateFileTransacted</b> cannot be inherited by any 
     child processes your application may create. The following information regarding this parameter also applies:

<ul>
<li>If <b>bInheritHandle</b> is not <b>FALSE</b>, which is any nonzero 
      value, then the handle can be inherited. Therefore it is critical this structure member be properly initialized 
      to <b>FALSE</b> if you do not intend the handle to be inheritable.</li>
<li>The access control lists (ACL) in the default security descriptor for a file or directory are inherited 
      from its parent directory.</li>
<li>The target file system must support security on files and directories for the 
      <b>lpSecurityDescriptor</b>  to have an effect on them, which can be determined by using 
      <a href="/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa">GetVolumeInformation</a>
</li>
</ul>
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
No

</td>
</tr>
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
No

</td>
</tr>
</table>
 

Note that SMB 3.0 does not support TxF.

<h3><a id="Files"></a><a id="files"></a><a id="FILES"></a>Files</h3>
If you try to create a file on a floppy drive that does not have a floppy disk or a CD-ROM drive that does not 
      have a CD, the system displays a message for the user to insert a disk or a CD. To prevent the system from 
      displaying this message, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode">SetErrorMode</a> function 
      with <b>SEM_FAILCRITICALERRORS</b>.

For more information, see 
      <a href="/windows/desktop/FileIO/creating-and-opening-files">Creating and Opening Files</a>.

If you rename or delete a file and then restore it shortly afterward, the system searches the cache for file 
      information to restore. Cached information includes its short/long name pair and creation time.

If you call <b>CreateFileTransacted</b> on a file that 
      is pending deletion as a result of a previous call to 
      <a href="/windows/desktop/api/fileapi/nf-fileapi-deletefilea">DeleteFile</a>, the function fails. The operating system 
      delays file deletion until all handles to the file are closed.
      <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns 
      <b>ERROR_ACCESS_DENIED</b>.

The <i>dwDesiredAccess</i> parameter can 
      be zero, allowing the application to query  file attributes without accessing the file if the application is 
      running with adequate security settings. This is useful to test for the existence of a file without opening it 
      for read and/or write access, or to obtain other statistics about the file or directory. See 
      <a href="/windows/desktop/FileIO/obtaining-and-setting-file-information">Obtaining and Setting File Information</a> 
      and <a href="/windows/desktop/api/fileapi/nf-fileapi-getfileinformationbyhandle">GetFileInformationByHandle</a>.

When an application creates a file across a network, it is better to use 
      <b>GENERIC_READ</b> | <b>GENERIC_WRITE</b> than to use 
      <b>GENERIC_WRITE</b> alone. The resulting code is faster, because the redirector can use the 
      cache manager and send fewer SMBs with more data. This combination also avoids an issue where writing to a file 
      across a network can occasionally return <b>ERROR_ACCESS_DENIED</b>.

<h3><a id="File_Streams"></a><a id="file_streams"></a><a id="FILE_STREAMS"></a>File Streams</h3>
On NTFS file systems, you can use 
      <b>CreateFileTransacted</b> to create separate streams 
      within a file.

For more information, see 
      <a href="/windows/desktop/FileIO/file-streams">File Streams</a>.

<h3><a id="Directories"></a><a id="directories"></a><a id="DIRECTORIES"></a>Directories</h3>
An application cannot create a directory by using 
      <b>CreateFileTransacted</b>, therefore only the 
      <b>OPEN_EXISTING</b> value is valid for <i>dwCreationDisposition</i> for 
      this use case. To create a directory, the application must call 
      <a href="/windows/desktop/api/winbase/nf-winbase-createdirectorytransacteda">CreateDirectoryTransacted</a>, 
      <a href="/windows/desktop/api/fileapi/nf-fileapi-createdirectorya">CreateDirectory</a> or 
      <a href="/windows/desktop/api/winbase/nf-winbase-createdirectoryexa">CreateDirectoryEx</a>.

To open a directory using <b>CreateFileTransacted</b>, 
      specify the <b>FILE_FLAG_BACKUP_SEMANTICS</b> flag as part of 
      <i>dwFlagsAndAttributes</i>. Appropriate security checks still apply when this flag is used 
      without <b>SE_BACKUP_NAME</b> and <b>SE_RESTORE_NAME</b> privileges.

When using <b>CreateFileTransacted</b> to open a 
      directory during defragmentation of a FAT or FAT32 file system volume, do not specify the 
      <b>MAXIMUM_ALLOWED</b> access right. Access to the directory is denied if this is done. 
      Specify the <b>GENERIC_READ</b> access right instead.

For more information, see 
      <a href="/windows/desktop/FileIO/about-directory-management">About Directory Management</a>.





> [!NOTE]
> The winbase.h header defines CreateFileTransacted as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/winbase/nf-winbase-copyfiletransacteda">CopyFileTransacted</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createdirectorytransacteda">CreateDirectoryTransacted</a>



<a href="/windows/desktop/api/winbase/nf-winbase-deletefiletransacteda">DeleteFileTransacted</a>



<a href="/windows/desktop/FileIO/file-compression-and-decompression">File Compression and Decompression</a>



<a href="/windows/desktop/FileIO/file-encryption">File Encryption</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>



<a href="/windows/desktop/FileIO/file-streams">File Streams</a>



<a href="/windows/desktop/api/winbase/nf-winbase-findfirstfiletransacteda">FindFirstFileTransacted</a>



<b>Functions</b>



<a href="/windows/desktop/api/winbase/nf-winbase-getfileattributestransacteda">GetFileAttributesTransacted</a>



<a href="/windows/desktop/api/winbase/nf-winbase-movefiletransacteda">MoveFileTransacted</a>



<b>Overview Topics</b>



<a href="/windows/desktop/FileIO/programming-considerations-for-transacted-fileio-">Programming Considerations for Transactional NTFS</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a>



<a href="/windows/desktop/FileIO/transactional-ntfs-portal">Transactional NTFS (TxF)</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a>
