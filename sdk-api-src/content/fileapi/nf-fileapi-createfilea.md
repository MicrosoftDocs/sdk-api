---
UID: NF:fileapi.CreateFileA
title: CreateFileA function (fileapi.h)
description: Creates or opens a file or I/O device. The most commonly used I/O devices are as follows:\_file, file stream, directory, physical disk, volume, console buffer, tape drive, communications resource, mailslot, and pipe. (ANSI)
helpviewer_keywords: ["0", "CREATE_ALWAYS", "CREATE_NEW", "CreateFileA", "FILE_ATTRIBUTE_ARCHIVE", "FILE_ATTRIBUTE_ENCRYPTED", "FILE_ATTRIBUTE_HIDDEN", "FILE_ATTRIBUTE_NORMAL", "FILE_ATTRIBUTE_OFFLINE", "FILE_ATTRIBUTE_READONLY", "FILE_ATTRIBUTE_SYSTEM", "FILE_ATTRIBUTE_TEMPORARY", "FILE_FLAG_BACKUP_SEMANTICS", "FILE_FLAG_DELETE_ON_CLOSE", "FILE_FLAG_NO_BUFFERING", "FILE_FLAG_OPEN_NO_RECALL", "FILE_FLAG_OPEN_REPARSE_POINT", "FILE_FLAG_OVERLAPPED", "FILE_FLAG_POSIX_SEMANTICS", "FILE_FLAG_RANDOM_ACCESS", "FILE_FLAG_SEQUENTIAL_SCAN", "FILE_FLAG_SESSION_AWARE", "FILE_FLAG_WRITE_THROUGH", "FILE_SHARE_DELETE", "FILE_SHARE_READ", "FILE_SHARE_WRITE", "OPEN_ALWAYS", "OPEN_EXISTING", "SECURITY_ANONYMOUS", "SECURITY_CONTEXT_TRACKING", "SECURITY_DELEGATION", "SECURITY_EFFECTIVE_ONLY", "SECURITY_IDENTIFICATION", "SECURITY_IMPERSONATION", "TRUNCATE_EXISTING", "fileapi/CreateFileA"]
old-location: fs\createfile.htm
tech.root: fs
ms.assetid: 80a96083-4de9-4422-9705-b8ad2b6cbd1b
ms.date: 08/16/2022
ms.keywords: 0, CREATE_ALWAYS, CREATE_NEW, CreateFile, CreateFile function [Files], CreateFileA, CreateFileW, FILE_ATTRIBUTE_ARCHIVE, FILE_ATTRIBUTE_ENCRYPTED, FILE_ATTRIBUTE_HIDDEN, FILE_ATTRIBUTE_NORMAL, FILE_ATTRIBUTE_OFFLINE, FILE_ATTRIBUTE_READONLY, FILE_ATTRIBUTE_SYSTEM, FILE_ATTRIBUTE_TEMPORARY, FILE_FLAG_BACKUP_SEMANTICS, FILE_FLAG_DELETE_ON_CLOSE, FILE_FLAG_NO_BUFFERING, FILE_FLAG_OPEN_NO_RECALL, FILE_FLAG_OPEN_REPARSE_POINT, FILE_FLAG_OVERLAPPED, FILE_FLAG_POSIX_SEMANTICS, FILE_FLAG_RANDOM_ACCESS, FILE_FLAG_SEQUENTIAL_SCAN, FILE_FLAG_SESSION_AWARE, FILE_FLAG_WRITE_THROUGH, FILE_SHARE_DELETE, FILE_SHARE_READ, FILE_SHARE_WRITE, OPEN_ALWAYS, OPEN_EXISTING, SECURITY_ANONYMOUS, SECURITY_CONTEXT_TRACKING, SECURITY_DELEGATION, SECURITY_EFFECTIVE_ONLY, SECURITY_IDENTIFICATION, SECURITY_IMPERSONATION, TRUNCATE_EXISTING, _win32_createfile, base.createfile, fileapi/CreateFile, fileapi/CreateFileA, fileapi/CreateFileW, fs.createfile, winbase/CreateFile, winbase/CreateFileA, winbase/CreateFileW
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateFileW (Unicode) and CreateFileA (ANSI)
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
 - CreateFileA
 - fileapi/CreateFileA
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
 - CreateFile
 - CreateFileA
 - CreateFileW
---

# CreateFileA function


## -description

Creates or opens a file or I/O device. The most commonly used I/O devices are as follows: file, file 
    stream, directory, physical disk, volume, console buffer, tape drive, communications resource, mailslot, and 
    pipe. The function returns a handle that can be used to access the file or device for various types of 
    I/O depending on the file or device and the flags and attributes specified.

To perform this operation as a transacted operation, which results in a handle that can be used for transacted 
    I/O, use the <a href="/windows/desktop/api/winbase/nf-winbase-createfiletransacteda">CreateFileTransacted</a> function.

## -parameters

### -param lpFileName [in]

The name of the file or device to be created or opened. You may use either forward slashes (/) or backslashes (\\) in this name.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.



For information on special device names, see 
       <a href="/windows/desktop/FileIO/defining-an-ms-dos-device-name">Defining an MS-DOS Device Name</a>.

To create a file stream, specify the name of the file, a colon, and then the name of the stream. For more 
       information, see <a href="/windows/desktop/FileIO/file-streams">File Streams</a>.


### -param dwDesiredAccess [in]

The requested access to the file or device, which can be summarized as read, write, both or 0 to indicate neither).

The most commonly used values are <b>GENERIC_READ</b>, 
       <b>GENERIC_WRITE</b>, or both 
       (<code>GENERIC_READ | GENERIC_WRITE</code>). For more information, see 
       <a href="/windows/desktop/SecAuthZ/generic-access-rights">Generic Access Rights</a>, 
       <a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>, 
       <a href="/windows/desktop/FileIO/file-access-rights-constants">File Access Rights Constants</a>, and 
       <a href="/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a>.

If this parameter is zero, the application can query certain metadata such as file, directory, or device 
       attributes without accessing that file or device, even if <b>GENERIC_READ</b> access would 
       have been denied.

You cannot request an access mode that conflicts with the sharing mode that is specified by the 
       <i>dwShareMode</i> parameter in an open request that already has an open handle.

For more information, see the Remarks section of this topic and 
       <a href="/windows/desktop/FileIO/creating-and-opening-files">Creating and Opening Files</a>.

### -param dwShareMode [in]

The requested sharing mode of the file or device, which can be read, write, both, delete, all of these, or 
       none (refer to the following table). Access requests to attributes or extended attributes are not affected by 
       this flag.

If this parameter is zero and <b>CreateFile</b> succeeds, the 
       file or device cannot be shared and cannot be opened again until the handle to the file or device is closed. 
       For more information, see the Remarks section.

You cannot request a sharing mode that conflicts with the access mode that is specified in an existing 
       request that has an open handle. <b>CreateFile</b> would fail and 
       the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function would return 
       <b>ERROR_SHARING_VIOLATION</b>.

To enable a process to share a file or device while another process has the file or device open, use a 
       compatible combination of one or more of the following values. For more information about valid combinations of 
       this parameter with the <i>dwDesiredAccess</i> parameter, see 
       <a href="/windows/desktop/FileIO/creating-and-opening-files">Creating and Opening Files</a>.

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
Prevents other processes from opening a file or device if they request delete, read, or write access.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SHARE_DELETE"></a><a id="file_share_delete"></a><dl>
<dt><b>FILE_SHARE_DELETE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Enables subsequent open operations on a file or device to request delete access.

Otherwise, other processes cannot open the file or device if they request delete access.

If this flag is not specified, but the file or device has been opened for delete access, the function 
         fails.

<div class="alert"><b>Note</b>  Delete access allows both delete and rename operations.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SHARE_READ"></a><a id="file_share_read"></a><dl>
<dt><b>FILE_SHARE_READ</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Enables subsequent open operations on a file or device to request read access.

Otherwise, other processes cannot open the file or device if they request read access.

If this flag is not specified, but the file or device has been opened for read access, the function 
         fails.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SHARE_WRITE"></a><a id="file_share_write"></a><dl>
<dt><b>FILE_SHARE_WRITE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Enables subsequent open operations on a file or device to request write access.

Otherwise, other processes cannot open the file or device if they request write access.

If this flag is not specified, but the file or device has been opened for write access or has a file mapping 
         with write access, the function fails.

</td>
</tr>
</table>

### -param lpSecurityAttributes [in, optional]

A pointer to a <a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> 
       structure that contains two separate but related data members: an optional security descriptor, and a Boolean 
       value that determines whether the returned handle can be inherited by child processes.

This parameter can be <b>NULL</b>.

If this parameter is <b>NULL</b>, the handle returned by 
       <b>CreateFile</b> cannot be inherited by any child processes the 
       application may create and the file or device associated with the returned handle gets a default security 
       descriptor.

The <b>lpSecurityDescriptor</b> member of the structure specifies a 
       <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> for a file or device. If 
       this member is <b>NULL</b>, the file or device associated with the returned handle is 
       assigned a default security descriptor.

<b>CreateFile</b> ignores the 
       <b>lpSecurityDescriptor</b> member when opening an existing file or device, but continues 
       to use the <b>bInheritHandle</b> member.

The <b>bInheritHandle</b> member of the structure specifies whether the returned handle 
       can be inherited.

For more information, see the Remarks section.

### -param dwCreationDisposition [in]

An action to take on a file or device that exists or does not exist.

For devices other than files, this parameter is usually set to <b>OPEN_EXISTING</b>.

For more information, see the Remarks section.

This parameter must be one of the following values, which cannot be combined:

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

If the specified file exists and is writable, the function truncates the file, the function succeeds, and 
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

If the specified file or device does not exist, the function fails and the last-error code is set to 
         <b>ERROR_FILE_NOT_FOUND</b> (2).

For more information about devices, see the Remarks section.

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

The file or device attributes and flags, <b>FILE_ATTRIBUTE_NORMAL</b> being the most 
       common default value for files.

This parameter can include any combination of the available file attributes 
       (<b>FILE_ATTRIBUTE_\*</b>). All other file attributes override 
       <b>FILE_ATTRIBUTE_NORMAL</b>.

This parameter can also contain combinations of flags (<b>FILE_FLAG_\*</b>) for control of 
       file or device caching behavior, access modes, and other special-purpose flags. These combine with any 
       <b>FILE_ATTRIBUTE_\*</b> values.

This parameter can also contain Security Quality of Service (SQOS) information by specifying the 
       <b>SECURITY_SQOS_PRESENT</b> flag. Additional SQOS-related flags information is presented in 
       the table following the attributes and flags tables.

<div class="alert"><b>Note</b>  When <b>CreateFile</b> opens an existing file, it generally 
       combines the file flags with the file attributes of the existing file, and ignores any file attributes supplied 
       as part of <i>dwFlagsAndAttributes</i>. Special cases are detailed in 
       <a href="/windows/desktop/FileIO/creating-and-opening-files">Creating and Opening Files</a>.</div>
<div> </div>
Some of the following file attributes and flags may only apply to files and not necessarily all other types 
       of devices that <b>CreateFile</b> can open. For additional 
       information, see the Remarks section of this topic and 
       <a href="/windows/desktop/FileIO/creating-and-opening-files">Creating and Opening Files</a>.

For more advanced access to file attributes, see 
       <a href="/windows/desktop/api/fileapi/nf-fileapi-setfileattributesa">SetFileAttributes</a>. For a complete list 
       of all file attributes with their values and descriptions, see 
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

This flag is not supported on Home, Home Premium, Starter, or ARM editions of Windows.

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
The file is being used for temporary storage.

For more information, see the <a href="#caching_behavior">Caching Behavior</a> section of this 
         topic.

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
The file is being opened or created for a backup or restore operation. The system ensures that the calling 
         process overrides file security checks when the process has <b>SE_BACKUP_NAME</b> and 
         <b>SE_RESTORE_NAME</b> privileges. For more information, see 
         <a href="/windows/desktop/SecBP/changing-privileges-in-a-token">Changing Privileges in a Token</a>.

You must set this flag to obtain a handle to a directory. A directory handle can be passed to some 
         functions instead of a file handle. For more information, see the Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_DELETE_ON_CLOSE"></a><a id="file_flag_delete_on_close"></a><dl>
<dt><b>FILE_FLAG_DELETE_ON_CLOSE</b></dt>
<dt>0x04000000</dt>
</dl>
</td>
<td width="60%">
The file is to be deleted immediately after all of its handles are closed, which includes the specified 
         handle and any other open or duplicated handles.

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
The file or device is being opened with no system caching for data reads and writes. This flag does not 
         affect hard disk caching or memory mapped files.

There are strict requirements for successfully working with files opened with 
         <b>CreateFile</b> using the 
         <b>FILE_FLAG_NO_BUFFERING</b> flag, for details see 
         <a href="/windows/desktop/FileIO/file-buffering">File Buffering</a>.

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
Normal <a href="/windows/desktop/FileIO/reparse-points">reparse point</a> processing will not 
         occur; <b>CreateFile</b> will attempt to open the reparse 
         point. When a file is opened, a file handle is returned, whether or not the filter that controls the reparse 
         point is operational.

This flag cannot be used with the <b>CREATE_ALWAYS</b> flag.

If the file is not a reparse point, then this flag is ignored.

For more information, see the Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_OVERLAPPED"></a><a id="file_flag_overlapped"></a><dl>
<dt><b>FILE_FLAG_OVERLAPPED</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
The file or device is being opened or created for asynchronous I/O.

When subsequent I/O operations are completed on this handle, the event specified in the 
         <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure will be set to the 
         signaled state.

If this flag is specified, the file can be used for simultaneous read and write operations.

If this flag is not specified, then I/O operations are serialized, even if the calls to the read and write 
         functions specify an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure.

For information about considerations when using a file handle created with this flag, see the 
         <a href="#synchronous_and_asynchronous_i_o_handles">Synchronous and Asynchronous I/O Handles</a> 
         section of this topic.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_POSIX_SEMANTICS"></a><a id="file_flag_posix_semantics"></a><dl>
<dt><b>FILE_FLAG_POSIX_SEMANTICS</b></dt>
<dt>0x01000000</dt>
</dl>
</td>
<td width="60%">
Access will occur according to POSIX rules. This includes allowing multiple files with names, differing 
         only in case, for file systems that support that naming. Use care when using this option, because files 
         created with this flag may not be accessible by applications that are written for MS-DOS or 16-bit 
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
Access is intended to be random. The system can use this as a hint to optimize file caching.

This flag has no effect if the file system does not support cached I/O and 
         <b>FILE_FLAG_NO_BUFFERING</b>.

For more information, see the <a href="#caching_behavior">Caching Behavior</a> section of this 
         topic.

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
Access is intended to be sequential from beginning to end. The system can use this as a hint to optimize 
         file caching.

This flag should not be used if read-behind (that is, reverse scans) will be used.

This flag has no effect if the file system does not support cached I/O and 
         <b>FILE_FLAG_NO_BUFFERING</b>.

For more information, see the <a href="#caching_behavior">Caching Behavior</a> section of this 
         topic.

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

For additional information, see the <a href="#caching_behavior">Caching Behavior</a> section of this 
         topic.

</td>
</tr>
</table>
 

The <i>dwFlagsAndAttributes</i> parameter can also specify SQOS information. For more 
       information, see 
       <a href="/windows/desktop/SecAuthZ/impersonation-levels">Impersonation Levels</a>. When the 
       calling application specifies the <b>SECURITY_SQOS_PRESENT</b> flag as part of 
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
       file supplies file attributes and extended attributes for the file that is being created.

This parameter can be <b>NULL</b>.

When opening an existing file, <b>CreateFile</b> ignores this 
       parameter.

When opening a new encrypted file, the file inherits the discretionary access control list from its parent 
       directory. For additional information, see 
       <a href="/windows/desktop/FileIO/file-encryption">File Encryption</a>.

## -returns

If the function succeeds, the return value is an open handle to the specified file, device, named pipe, or 
       mail slot.

If the function fails, the return value is <b>INVALID_HANDLE_VALUE</b>. To get extended 
       error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>CreateFile</b> was originally developed specifically for file 
    interaction but has since been expanded and enhanced to include most other types of I/O devices and mechanisms 
    available to Windows developers. This section attempts to cover the varied issues developers may experience when 
    using <b>CreateFile</b> in different contexts and with different I/O 
    types. The text attempts to use the word <i>file</i> only when referring specifically to data stored in an 
    actual file on a file system. However, some uses of <i>file</i> may be referring more generally to an I/O 
    object that supports file-like mechanisms. This liberal use of the term <i>file</i> is particularly 
    prevalent in constant names and parameter names because of the previously mentioned historical reasons.

When an application is finished using the object handle returned by 
    <b>CreateFile</b>, use the 
    <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to close the handle. This not only 
    frees up system resources, but can have wider influence on things like sharing the file or device and committing 
    data to disk. Specifics are noted within this topic as appropriate.

<b>Windows Server 2003 and Windows XP:  </b>A sharing violation occurs if an attempt is made to open a file or directory for deletion on a remote 
     computer when the value of the <i>dwDesiredAccess</i> parameter is the 
     <b>DELETE</b> access flag (0x00010000) <b>OR</b>'ed with any other access flag, and the remote file 
     or directory has not been opened with <b>FILE_SHARE_DELETE</b>. To avoid the sharing violation 
     in this scenario, open the remote file or directory with the <b>DELETE</b> access right only, 
     or call <a href="/windows/desktop/api/fileapi/nf-fileapi-deletefilea">DeleteFile</a> without first opening the file or 
     directory for deletion.

Some file systems, such as the NTFS file system, support compression or encryption for individual files and 
     directories. On volumes that have a mounted file system with this support, a new file inherits the compression 
     and encryption attributes of its directory.

You cannot use <b>CreateFile</b> to control compression, 
     decompression, or decryption on a file or directory. For more information, see 
     <a href="/windows/desktop/FileIO/creating-and-opening-files">Creating and Opening Files</a>, 
     <a href="/windows/desktop/FileIO/file-compression-and-decompression">File Compression and Decompression</a>, 
     and <a href="/windows/desktop/FileIO/file-encryption">File Encryption</a>.

<b>Windows Server 2003 and Windows XP:  </b>For backward compatibility purposes, <b>CreateFile</b> does 
     not apply inheritance rules when you specify a security descriptor in 
     <i>lpSecurityAttributes</i>. To support inheritance, functions that later query the security 
     descriptor of this file may heuristically determine and report that inheritance is in effect. For more 
     information, see 
     <a href="/windows/desktop/SecAuthZ/automatic-propagation-of-inheritable-aces">Automatic Propagation of Inheritable ACEs</a>.

As stated previously, if the <i>lpSecurityAttributes</i> parameter is 
     <b>NULL</b>, the handle returned by 
     <b>CreateFile</b> cannot be inherited by any child processes your 
     application may create. The following information regarding this parameter also applies:

<ul>
<li>If the <b>bInheritHandle</b> member variable is not <b>FALSE</b>, 
      which is any nonzero value, then the handle can be inherited. Therefore it is critical this structure member be 
      properly initialized to <b>FALSE</b> if you do not intend the handle to be inheritable.</li>
<li>The access control lists (ACL) in the default security descriptor for a file or directory are inherited 
      from its parent directory.</li>
<li>The target file system must support security on files and directories for the 
      <b>lpSecurityDescriptor</b> member to have an effect on them, which can be determined by 
      using <a href="/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa">GetVolumeInformation</a>.</li>
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
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
See remarks

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
See remarks

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
 

Note that <b>CreateFile</b> with supersede disposition will fail if performed on a file where there is already an open alternate data stream.

<h3><a id="Symbolic_Link_Behavior"></a><a id="symbolic_link_behavior"></a><a id="SYMBOLIC_LINK_BEHAVIOR"></a>Symbolic Link Behavior</h3>
If the call to this function creates a file, there is no change in behavior. Also, consider the following 
      information regarding <b>FILE_FLAG_OPEN_REPARSE_POINT</b>:

<ul>
<li>
If <b>FILE_FLAG_OPEN_REPARSE_POINT</b> is specified:

<ul>
<li>If an existing file is opened and it is a symbolic link, the handle returned is a handle to the 
         symbolic link.</li>
<li>If <b>TRUNCATE_EXISTING</b> or <b>FILE_FLAG_DELETE_ON_CLOSE</b> 
         are specified, the file affected is a symbolic link.</li>
</ul>
</li>
<li>
If <b>FILE_FLAG_OPEN_REPARSE_POINT</b> is not specified:

<ul>
<li>If an existing file is opened and it is a symbolic link, the handle returned is a handle to the 
         target.</li>
<li>If <b>CREATE_ALWAYS</b>, <b>TRUNCATE_EXISTING</b>, or 
         <b>FILE_FLAG_DELETE_ON_CLOSE</b> are specified, the file affected is the target.</li>
</ul>
</li>
</ul>
<h3><a id="caching_behavior"></a><a id="CACHING_BEHAVIOR"></a>Caching Behavior</h3>
Several of the possible values for the <i>dwFlagsAndAttributes</i> parameter are used by 
      <b>CreateFile</b> to control or affect how the data associated 
      with the handle is cached by the system. They are:

<ul>
<li><b>FILE_FLAG_NO_BUFFERING</b></li>
<li><b>FILE_FLAG_RANDOM_ACCESS</b></li>
<li><b>FILE_FLAG_SEQUENTIAL_SCAN</b></li>
<li><b>FILE_FLAG_WRITE_THROUGH</b></li>
<li><b>FILE_ATTRIBUTE_TEMPORARY</b></li>
</ul>
If none of these flags is specified, the system uses a default general-purpose caching scheme. Otherwise, the 
      system caching behaves as specified for each flag.

Some of these flags should not be combined. For instance, combining 
      <b>FILE_FLAG_RANDOM_ACCESS</b> with <b>FILE_FLAG_SEQUENTIAL_SCAN</b> is 
      self-defeating.

Specifying the <b>FILE_FLAG_SEQUENTIAL_SCAN</b> flag can increase performance for 
      applications that read large files using sequential access. Performance gains can be even more noticeable for 
      applications that read large files mostly sequentially, but occasionally skip forward over small ranges of 
      bytes. If an application moves the file pointer for random access, optimum caching performance most likely will 
      not occur. However, correct operation is still guaranteed.

The flags <b>FILE_FLAG_WRITE_THROUGH</b> and 
      <b>FILE_FLAG_NO_BUFFERING</b> are independent and may be combined.

If <b>FILE_FLAG_WRITE_THROUGH</b> is used but 
      <b>FILE_FLAG_NO_BUFFERING</b> is not also specified, so that system caching is in effect, 
      then the data is written to the system cache but is flushed to disk without delay.

If <b>FILE_FLAG_WRITE_THROUGH</b> and <b>FILE_FLAG_NO_BUFFERING</b> are 
      both specified, so that system caching is not in effect, then the data is immediately flushed to disk without 
      going through the Windows system cache. The operating system also requests a write-through of the hard disk's 
      local hardware cache to persistent media.

<div class="alert"><b>Note</b>  Not all hard disk hardware supports this write-through capability.</div>
<div> </div>
Proper use of the <b>FILE_FLAG_NO_BUFFERING</b> flag requires special application 
      considerations. For more information, see 
      <a href="/windows/desktop/FileIO/file-buffering">File Buffering</a>.

A write-through request via <b>FILE_FLAG_WRITE_THROUGH</b> also causes NTFS to flush any 
      metadata changes, such as a time stamp update or a rename operation, that result from processing the request. 
      For this reason, the <b>FILE_FLAG_WRITE_THROUGH</b> flag is often used with the 
      <b>FILE_FLAG_NO_BUFFERING</b> flag as a replacement for calling the 
      <a href="/windows/desktop/api/fileapi/nf-fileapi-flushfilebuffers">FlushFileBuffers</a> function after each write, which can 
      cause unnecessary performance penalties. Using these flags together avoids those penalties. For general 
      information about the caching of files and metadata, see 
      <a href="/windows/desktop/FileIO/file-caching">File Caching</a>.

When <b>FILE_FLAG_NO_BUFFERING</b> is combined with 
      <b>FILE_FLAG_OVERLAPPED</b>, the flags give maximum asynchronous performance, because the I/O 
      does not rely on the synchronous operations of the memory manager. However, some I/O operations take more time, 
      because data is not being held in the cache. Also, the file metadata may still be cached (for example, when 
      creating an empty file). To ensure that the metadata is flushed to disk, use the 
      <a href="/windows/desktop/api/fileapi/nf-fileapi-flushfilebuffers">FlushFileBuffers</a> function.

Specifying the <b>FILE_ATTRIBUTE_TEMPORARY</b> attribute causes file systems to avoid 
      writing data back to mass storage if sufficient cache memory is available, because an application deletes a 
      temporary file after a handle is closed. In that case, the system can entirely avoid writing the data. Although 
      it does not directly control data caching in the same way as the previously mentioned flags, the 
      <b>FILE_ATTRIBUTE_TEMPORARY</b> attribute does tell the system to hold as much as possible in 
      the system cache without writing and therefore may be of concern for certain applications.

<h3><a id="Files"></a><a id="files"></a><a id="FILES"></a>Files</h3>
If you rename or delete a file and then restore it shortly afterward, the system searches the cache for file 
      information to restore. Cached information includes its short/long name pair and creation time.

If you call <b>CreateFile</b> on a file that is pending deletion 
      as a result of a previous call to <a href="/windows/desktop/api/fileapi/nf-fileapi-deletefilea">DeleteFile</a>, the function 
      fails. The operating system delays file deletion until all handles to the file are closed. 
      <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns 
      <b>ERROR_ACCESS_DENIED</b>.

The <i>dwDesiredAccess</i> parameter can be zero, allowing the application to query file 
      attributes without accessing the file if the application is running with adequate security settings. This is 
      useful to test for the existence of a file without opening it for read and/or write access, or to obtain other 
      statistics about the file or directory. See 
      <a href="/windows/desktop/FileIO/obtaining-and-setting-file-information">Obtaining and Setting File Information</a> 
      and <a href="/windows/desktop/api/fileapi/nf-fileapi-getfileinformationbyhandle">GetFileInformationByHandle</a>.

If <b>CREATE_ALWAYS</b> and <b>FILE_ATTRIBUTE_NORMAL</b> are 
      specified, <b>CreateFile</b> fails and sets the last error to 
      <b>ERROR_ACCESS_DENIED</b> if the file exists and has the 
      <b>FILE_ATTRIBUTE_HIDDEN</b> or <b>FILE_ATTRIBUTE_SYSTEM</b> attribute. 
      To avoid the error, specify the same attributes as the existing file.

When an application creates a file across a network, it is better to use 
      <code>GENERIC_READ | GENERIC_WRITE</code> for 
      <i>dwDesiredAccess</i> than to use <b>GENERIC_WRITE</b> alone. The 
      resulting code is faster, because the redirector can use the cache manager and send fewer SMBs with more data. 
      This combination also avoids an issue where writing to a file across a network can occasionally return 
      <b>ERROR_ACCESS_DENIED</b>.

For more information, see 
      <a href="/windows/desktop/FileIO/creating-and-opening-files">Creating and Opening Files</a>.

<h3><a id="synchronous_and_asynchronous_i_o_handles"></a><a id="SYNCHRONOUS_AND_ASYNCHRONOUS_I_O_HANDLES"></a>Synchronous and Asynchronous I/O Handles</h3>
<b>CreateFile</b> provides for creating a file or device handle 
      that is either synchronous or asynchronous. A synchronous handle behaves such that I/O function calls using that 
      handle are blocked until they complete, while an asynchronous file handle makes it possible for the system to 
      return immediately from I/O function calls, whether they completed the I/O operation or not. As stated 
      previously, this synchronous versus asynchronous behavior is determined by specifying 
      <b>FILE_FLAG_OVERLAPPED</b> within the <i>dwFlagsAndAttributes</i> 
      parameter. There are several complexities and potential pitfalls when using asynchronous I/O; for more 
      information, see 
      <a href="/windows/desktop/FileIO/synchronous-and-asynchronous-i-o">Synchronous and Asynchronous I/O</a>.

<h3><a id="File_Streams"></a><a id="file_streams"></a><a id="FILE_STREAMS"></a>File Streams</h3>
On NTFS file systems, you can use <b>CreateFile</b> to create 
      separate streams within a file. For more information, see 
      <a href="/windows/desktop/FileIO/file-streams">File Streams</a>.

<h3><a id="Directories"></a><a id="directories"></a><a id="DIRECTORIES"></a>Directories</h3>
An application cannot create a directory by using 
      <b>CreateFile</b>, therefore only the 
      <b>OPEN_EXISTING</b> value is valid for 
      <i>dwCreationDisposition</i> for this use case. To create a directory, the application must 
      call <a href="/windows/desktop/api/fileapi/nf-fileapi-createdirectorya">CreateDirectory</a> or 
      <a href="/windows/desktop/api/winbase/nf-winbase-createdirectoryexa">CreateDirectoryEx</a>.

To open a directory using <b>CreateFile</b>, specify the 
      <b>FILE_FLAG_BACKUP_SEMANTICS</b> flag as part of 
      <i>dwFlagsAndAttributes</i>. Appropriate security checks still apply when this flag is used 
      without <b>SE_BACKUP_NAME</b> and <b>SE_RESTORE_NAME</b> privileges.

When using <b>CreateFile</b> to open a directory during 
      defragmentation of a FAT or FAT32 file system volume, do not specify the 
      <b>MAXIMUM_ALLOWED</b> access right. Access to the directory is denied if this is done. 
      Specify the <b>GENERIC_READ</b> access right instead.

For more information, see 
      <a href="/windows/desktop/FileIO/about-directory-management">About Directory Management</a>.

<h3><a id="Physical_Disks_and_Volumes"></a><a id="physical_disks_and_volumes"></a><a id="PHYSICAL_DISKS_AND_VOLUMES"></a>Physical Disks and Volumes</h3>
Direct access to the disk or to a volume is restricted. 

<b>Windows Server 2003 and Windows XP:  </b>Direct access to the disk or to a volume is not restricted in this manner.

You can use the <b>CreateFile</b> function to open a physical 
      disk drive or a volume, which returns a direct access storage device (DASD) handle that can be used with the 
      <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function. This enables you to access 
      the disk or volume directly, for example such disk metadata as the partition table. However, this type of access 
      also exposes the disk drive or volume to potential data loss, because an incorrect write to a disk using this 
      mechanism could make its contents inaccessible to the operating system. To ensure data integrity, be sure to 
      become familiar with <b>DeviceIoControl</b> and how other 
      APIs behave differently with a direct access handle as opposed to a file system handle.

The following requirements must be met for such a call to succeed:

<ul>
<li>The caller must have administrative privileges. For more information, see 
       <a href="/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>.</li>
<li>The <i>dwCreationDisposition</i> parameter must have the 
       <b>OPEN_EXISTING</b> flag.</li>
<li>When opening a volume or floppy disk, the <i>dwShareMode</i> parameter must have the 
       <b>FILE_SHARE_WRITE</b> flag.</li>
</ul>
<div class="alert"><b>Note</b>  The <i>dwDesiredAccess</i> parameter can be zero, allowing the application to query 
      device attributes without accessing a device. This is useful for an application to determine the size of a 
      floppy disk drive and the formats it supports without requiring a floppy disk in a drive, for instance. It can 
      also be used for reading statistics without requiring higher-level data read/write permission.</div>
<div> </div>
When opening a physical drive <i>x</i>:, the 
      <i>lpFileName</i> string should be the following form: 
      "\\.\PhysicalDrive<i>X</i>". Hard disk numbers 
      start at zero. The following table shows some examples of physical drive strings.

<table>
<tr>
<th>String</th>
<th>Meaning</th>
</tr>
<tr>
<td>"\\.\PhysicalDrive0"</td>
<td>Opens the first physical drive.</td>
</tr>
<tr>
<td>"\\.\PhysicalDrive2"</td>
<td>Opens the third physical drive.</td>
</tr>
</table>
 

To obtain the physical drive identifier for a volume, open a handle to the volume and call the 
      <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with 
      <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_volume_get_volume_disk_extents">IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS</a>. 
      This control code returns the disk number and offset for each of the volume's one or more extents; a volume can 
      span multiple physical disks.

For an example of opening a physical drive, see 
      <a href="/windows/desktop/DevIO/calling-deviceiocontrol">Calling DeviceIoControl</a>.

When opening a volume or removable media drive (for example, a floppy disk drive or flash memory thumb drive), 
      the <i>lpFileName</i> string should be the following form: 
      "&#92;&#92;.&#92;<i>X</i>:". Do not use a trailing backslash 
      (\\), which indicates the root directory of a drive. The following table shows some examples of drive strings.

<table>
<tr>
<th>String</th>
<th>Meaning</th>
</tr>
<tr>
<td>"\\.\A:"</td>
<td>Opens floppy disk drive A.</td>
</tr>
<tr>
<td>"\\.\C:"</td>
<td>Opens the C: volume.</td>
</tr>
<tr>
<td>"\\.\C:\"</td>
<td>Opens the file system of the C: volume.</td>
</tr>
</table>
 

You can also open a volume by referring to its volume name. For more information, see 
      <a href="/windows/desktop/FileIO/naming-a-volume">Naming a Volume</a>.

A volume contains one or more mounted file systems. Volume handles can be opened as noncached at the 
      discretion of the particular file system, even when the noncached option is not specified in 
      <b>CreateFile</b>. You should assume that all Microsoft file 
      systems open volume handles as noncached. The restrictions on noncached I/O for files also apply to volumes.

A file system may or may not require buffer alignment even though the data is noncached. However, if the 
      noncached option is specified when opening a volume, buffer alignment is enforced regardless of the file system 
      on the volume. It is recommended on all file systems that you open volume handles as noncached, and follow the 
      noncached I/O restrictions.

<div class="alert"><b>Note</b>  To read or write to the last few sectors of the volume, you must call 
      <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> and specify 
      <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_allow_extended_dasd_io">FSCTL_ALLOW_EXTENDED_DASD_IO</a>. This signals 
      the file system driver not to perform any I/O boundary checks on partition read or write calls. Instead, 
      boundary checks are performed by the device driver.</div>
<div> </div>
<h3><a id="Changer_Device"></a><a id="changer_device"></a><a id="CHANGER_DEVICE"></a>Changer Device</h3>
The <b>IOCTL_CHANGER_*</b> control codes for 
      <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> accept a handle to a changer device. 
      To open a changer device, use a file name of the following form: 
      "\\.\Changer<i>x</i>" where 
      <i>x</i> is a number that indicates which device to open, starting with zero. To open 
      changer device zero in an application that is written in C or C++, use the following file name: 
      "\\.\Changer0".

<h3><a id="Tape_Drives"></a><a id="tape_drives"></a><a id="TAPE_DRIVES"></a>Tape Drives</h3>
You can open tape drives by using a file name of the following form: 
      "\\.\TAPE<i>x</i>" where 
      <i>x</i> is a number that indicates which drive to open, starting with tape drive zero. To 
      open tape drive zero in an application that is written in C or C++, use the following file name: 
      "\\.\TAPE0".

For more information, see <a href="/windows/desktop/Backup/backup">Backup</a>.

<h3><a id="Communications_Resources"></a><a id="communications_resources"></a><a id="COMMUNICATIONS_RESOURCES"></a>Communications Resources</h3>
The <b>CreateFile</b> function can create a handle to a 
      communications resource, such as the serial port COM1. For communications resources, 
      the <i>dwCreationDisposition</i> parameter must be 
      <b>OPEN_EXISTING</b>, the <i>dwShareMode</i> parameter must be zero 
      (exclusive access), and the <i>hTemplateFile</i> parameter must be 
      <b>NULL</b>. Read, write, or read/write access can be specified, and the handle can be opened 
      for overlapped I/O.

To specify a COM port number greater than 9, use the following syntax: 
      "\\\\.\COM10". This syntax works for all port numbers and hardware that 
      allows COM port numbers to be specified.

For more information about communications, see 
      <a href="/windows/desktop/DevIO/communications-resources">Communications</a>.

<h3><a id="Consoles"></a><a id="consoles"></a><a id="CONSOLES"></a>Consoles</h3>
The <b>CreateFile</b> function can create a handle to console 
      input (CONIN$). If the process has an open handle to it as a result of inheritance or 
      duplication, it can also create a handle to the active screen buffer (CONOUT$). The 
      calling process must be attached to an inherited console or one allocated by the 
      <a href="/windows/console/allocconsole">AllocConsole</a> function. For console handles, set the 
      <b>CreateFile</b> parameters as follows.

<table>
<tr>
<th>Parameters</th>
<th>Value</th>
</tr>
<tr>
<td>
<i>lpFileName</i>

</td>
<td>
Use the CONIN$ value to specify console input.

Use the CONOUT$ value to specify console output.

CONIN$ gets a handle to the console input buffer, even if the 
         <a href="/windows/console/setstdhandle">SetStdHandle</a> function redirects the standard input 
         handle. To get the standard input handle, use the 
         <a href="/windows/console/getstdhandle">GetStdHandle</a> function.

CONOUT$ gets a handle to the active screen buffer, even if 
         <a href="/windows/console/setstdhandle">SetStdHandle</a> redirects the standard output handle. To 
         get the standard output handle, use <a href="/windows/console/getstdhandle">GetStdHandle</a>.

</td>
</tr>
<tr>
<td>
<i>dwDesiredAccess</i>

</td>
<td>
<code>GENERIC_READ | GENERIC_WRITE</code> is preferred, but either one can 
         limit access.

</td>
</tr>
<tr>
<td>
<i>dwShareMode</i>

</td>
<td>
When opening CONIN$, specify 
         <b>FILE_SHARE_READ</b>. When opening CONOUT$, specify 
         <b>FILE_SHARE_WRITE</b>.

If the calling process inherits the console, or if a child process should be able to access the console, 
         this parameter must be <code>FILE_SHARE_READ | FILE_SHARE_WRITE</code>.

</td>
</tr>
<tr>
<td>
<i>lpSecurityAttributes</i>

</td>
<td>
If you want the console to be inherited, the <b>bInheritHandle</b> member of the 
         <a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure 
         must be <b>TRUE</b>.

</td>
</tr>
<tr>
<td>
<i>dwCreationDisposition</i>

</td>
<td>
You should specify <b>OPEN_EXISTING</b> when using 
         <b>CreateFile</b> to open the console.

</td>
</tr>
<tr>
<td>
<i>dwFlagsAndAttributes</i>

</td>
<td>
Ignored.

</td>
</tr>
<tr>
<td>
<i>hTemplateFile</i>

</td>
<td>
Ignored.

</td>
</tr>
</table>
 

The following table shows various settings of <i>dwDesiredAccess</i> and 
      <i>lpFileName</i>.

<table>
<tr>
<th><i>lpFileName</i></th>
<th><i>dwDesiredAccess</i></th>
<th>Result</th>
</tr>
<tr>
<td>"CON"</td>
<td><b>GENERIC_READ</b></td>
<td>Opens console for input.</td>
</tr>
<tr>
<td>"CON"</td>
<td><b>GENERIC_WRITE</b></td>
<td>Opens console for output.</td>
</tr>
<tr>
<td>"CON"</td>
<td><code>GENERIC_READ | GENERIC_WRITE</code></td>
<td>Causes <b>CreateFile</b> to fail; 
        <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns 
        <b>ERROR_FILE_NOT_FOUND</b>.</td>
</tr>
</table>
 

<h3><a id="Mailslots"></a><a id="mailslots"></a><a id="MAILSLOTS"></a>Mailslots</h3>
If <b>CreateFile</b> opens the client end of a mailslot, the 
      function returns <b>INVALID_HANDLE_VALUE</b> if the mailslot client attempts to open a local 
      mailslot before the mailslot server has created it with the 
      <a href="/windows/desktop/api/winbase/nf-winbase-createmailslota">CreateMailSlot</a> function.

For more information, see <a href="/windows/desktop/ipc/mailslots">Mailslots</a>.

<h3><a id="Pipes"></a><a id="pipes"></a><a id="PIPES"></a>Pipes</h3>
If <b>CreateFile</b> opens the client end of a named pipe, the 
      function uses any instance of the named pipe that is in the listening state. The opening process can duplicate 
      the handle as many times as required, but after it is opened, the named pipe instance cannot be opened by 
      another client. The access that is specified when a pipe is opened must be compatible with the access that is 
      specified in the <i>dwOpenMode</i> parameter of the 
      <a href="/windows/desktop/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a> function.

If the <a href="/windows/desktop/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a> function was not 
      successfully called on the server prior to this operation, a pipe will not exist and 
      <b>CreateFile</b> will fail with 
      <b>ERROR_FILE_NOT_FOUND</b>.

If there is at least one active pipe instance but there are no available listener pipes on the server, which 
      means all pipe instances are currently connected, 
     <b>CreateFile</b> fails with 
     <b>ERROR_PIPE_BUSY</b>.

For more information, see <a href="/windows/desktop/ipc/pipes">Pipes</a>.


#### Examples

Example file operations are shown in the following topics:

<ul>
<li>
<a href="/windows/desktop/FileIO/appending-one-file-to-another-file">Appending One File to Another File</a>
</li>
<li>
<a href="/windows/desktop/FileIO/canceling-pending-i-o-operations">Canceling Pending I/O Operations</a>
</li>
<li>
<a href="/windows/desktop/ProcThread/creating-a-child-process-with-redirected-input-and-output">Creating a Child Process with Redirected Input and Output</a>
</li>
<li>
<a href="/windows/desktop/FileIO/creating-and-using-a-temporary-file">Creating and Using a Temporary File</a>
</li>
<li>
<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_recall_file">FSCTL_RECALL_FILE</a>
</li>
<li>
<a href="/windows/desktop/api/fileapi/nf-fileapi-getfinalpathnamebyhandlea">GetFinalPathNameByHandle</a>
</li>
<li>
<a href="/windows/desktop/FileIO/locking-and-unlocking-byte-ranges-in-files">Locking and Unlocking Byte Ranges in Files</a>
</li>
<li>
<a href="/windows/desktop/Memory/obtaining-a-file-name-from-a-file-handle">Obtaining a File Name From a File Handle</a>
</li>
<li>
<a href="/windows/desktop/FileIO/obtaining-file-system-recognition-information">Obtaining File System Recognition Information</a>
</li>
<li>
<a href="/windows/desktop/FileIO/opening-a-file-for-reading-or-writing">Opening a File for Reading or Writing</a>
</li>
<li>
<a href="/windows/desktop/SysInfo/retrieving-the-last-write-time">Retrieving the Last-Write Time</a>
</li>
<li>
<a href="/windows/desktop/api/fileapi/nf-fileapi-setfileinformationbyhandle">SetFileInformationByHandle</a>
</li>
<li>
<a href="/windows/desktop/FileIO/testing-for-the-end-of-a-file">Testing for the End of a File</a>
</li>
<li>
<a href="/windows/desktop/ProcThread/using-fibers">Using Fibers</a>
</li>
<li>
<a href="/windows/desktop/FileIO/using-streams">Using Streams</a>
</li>
<li>
<a href="/windows/desktop/FileIO/walking-a-buffer-of-change-journal-records">Walking a Buffer of Change Journal Records</a>
</li>
<li>
<a href="/windows/win32/api/wow64apiset/nf-wow64apiset-wow64disablewow64fsredirection">Wow64DisableWow64FsRedirection</a>
</li>
<li>
<a href="/windows/win32/api/wow64apiset/nf-wow64apiset-wow64enablewow64fsredirection">Wow64EnableWow64FsRedirection</a>
</li>
</ul>
Physical device I/O is demonstrated in the following topics:

<ul>
<li>
<a href="/windows/desktop/DevIO/calling-deviceiocontrol">Calling DeviceIoControl</a>
</li>
<li>
<a href="/windows/desktop/DevIO/configuring-a-communications-resource">Configuring a Communications Resource</a>
</li>
<li>
<a href="/windows/desktop/DevIO/monitoring-communications-events">Monitoring Communications Events</a>
</li>
<li>
<a href="/windows/desktop/DevIO/processing-a-request-to-remove-a-device">Processing a Request to Remove a Device</a>
</li>
</ul>
An example using named pipes is located at 
      <a href="/windows/desktop/ipc/named-pipe-client">Named Pipe Client</a>.

Working with a mailslot is shown in 
      <a href="/windows/desktop/ipc/writing-to-a-mailslot">Writing to a Mailslot</a>.

A tape backup code snippet can found at 
      <a href="/windows/desktop/Backup/creating-a-backup-application">Creating a Backup Application</a>.

<div class="code"></div>




> [!NOTE]
> The fileapi.h header defines CreateFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/FileIO/about-directory-management">About Directory Management</a>



<a href="/windows/desktop/FileIO/about-volume-management">About Volume Management</a>



<a href="/windows/desktop/Backup/backup">Backup</a>



<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/DevIO/communications-resources">Communications</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createdirectorya">CreateDirectory</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createdirectoryexa">CreateDirectoryEx</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createfiletransacteda">CreateFileTransacted</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createmailslota">CreateMailSlot</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a>



<a href="/windows/desktop/FileIO/creating--deleting--and-maintaining-files">Creating, Deleting, and Maintaining Files</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-deletefilea">DeleteFile</a>



<a href="/windows/desktop/DevIO/device-input-and-output-control-ioctl-">Device Input and Output Control (IOCTL)</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="/windows/desktop/FileIO/file-compression-and-decompression">File Compression and Decompression</a>



<a href="/windows/desktop/FileIO/file-encryption">File Encryption</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>



<a href="/windows/desktop/FileIO/file-streams">File Streams</a>



<b>Functions</b>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="/windows/desktop/FileIO/i-o-completion-ports">I/O Completion Ports</a>



<a href="/windows/desktop/FileIO/i-o-concepts">I/O Concepts</a>



<a href="/windows/desktop/ipc/mailslots">Mailslots</a>



<a href="/windows/desktop/FileIO/obtaining-and-setting-file-information">Obtaining and Setting File Information</a>



<b>Overview Topics</b>



<a href="/windows/desktop/ipc/pipes">Pipes</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfileex">ReadFileEx</a>



<a href="/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-setfileattributesa">SetFileAttributes</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefileex">WriteFileEx</a>
