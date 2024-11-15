---
UID: NF:fileapifromapp.CreateFileFromAppW
tech.root: fs
title: CreateFileFromAppW
ms.date: 03/23/2021
targetos: Windows
description: Creates or opens a file or I/O device. The behavior of this function is identical to CreateFile, except that this function adheres to the Universal Windows Platform app security model.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: fileapifromapp.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 1803
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_location:
- Kernel32.dll
api_name:
- CreateFileFromAppW
- CreateFileFromApp
api_type:
- DLLExport
product:
f1_keywords:
 - CreateFileFromAppW
 - fileapifromapp/CreateFileFromAppW
dev_langs:
 - c++
---

## -description

Creates or opens a file or I/O device. The behavior of this function is identical to [**CreateFile**](../fileapi/nf-fileapi-createfilew.md), except that this function adheres to the Universal Windows Platform app security model.


## -parameters

### -param lpFileName

The name of the file or device to be created or opened. You may use either forward slashes (/) or backslashes (\\) in this name.
    
In the ANSI version of this function, the name is limited to **MAX\_PATH** characters. To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

For information on special device names, see [Defining an MS-DOS Device Name](/windows/win32/fileio/defining-an-ms-dos-device-name).

To create a file stream, specify the name of the file, a colon, and then the name of the stream. For more information, see [File Streams](/windows/win32/fileio/file-streams).

For the unicode version of this function (**CreateFileFromAppW**), you can opt-in to remove the **MAX\_PATH** limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.


### -param dwDesiredAccess

The requested access to the file or device, which can be summarized as read, write, both or neither zero).

The most commonly used values are **GENERIC\_READ**, **GENERIC\_WRITE**, or both (`GENERIC_READ | GENERIC_WRITE`). For more information, see [Generic Access Rights](/windows/win32/secauthz/generic-access-rights), [File Security and Access Rights](/windows/win32/fileio/file-security-and-access-rights), [**File Access Rights Constants**](/windows/win32/fileio/file-access-rights-constants), and [**ACCESS\_MASK**](/windows/win32/secauthz/access-mask).

If this parameter is zero, the application can query certain metadata such as file, directory, or device attributes without accessing that file or device, even if **GENERIC\_READ** access would have been denied.

You cannot request an access mode that conflicts with the sharing mode that is specified by the *dwShareMode* parameter in an open request that already has an open handle.


### -param dwShareMode

 The requested sharing mode of the file or device, which can be read, write, both, delete, all of these, or none (refer to the following table). Access requests to attributes or extended attributes are not affected by this flag.
    
<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Meaning</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="0"></span>
<strong>0</strong>
0x00000000</td>
<td><p>Prevents other processes from opening a file or device if they request delete, read, or write access.</p></td>
</tr>
<tr class="even">
<td><span id="FILE_SHARE_DELETE"></span><span id="file_share_delete"></span>
<strong>FILE_SHARE_DELETE</strong>
0x00000004</td>
<td><p>Enables subsequent open operations on a file or device to request delete access.</p>
<p>Otherwise, other processes cannot open the file or device if they request delete access.</p>
<p>If this flag is not specified, but the file or device has been opened for delete access, the function fails.</p>
<strong>Note</strong>  Delete access allows both delete and rename operations.
<div>
 
</div></td>
</tr>
<tr class="odd">
<td><span id="FILE_SHARE_READ"></span><span id="file_share_read"></span>
<strong>FILE_SHARE_READ</strong>
0x00000001</td>
<td><p>Enables subsequent open operations on a file or device to request read access.</p>
<p>Otherwise, other processes cannot open the file or device if they request read access.</p>
<p>If this flag is not specified, but the file or device has been opened for read access, the function fails.</p></td>
</tr>
<tr class="even">
<td><span id="FILE_SHARE_WRITE"></span><span id="file_share_write"></span>
<strong>FILE_SHARE_WRITE</strong>
0x00000002</td>
<td><p>Enables subsequent open operations on a file or device to request write access.</p>
<p>Otherwise, other processes cannot open the file or device if they request write access.</p>
<p>If this flag is not specified, but the file or device has been opened for write access or has a file mapping with write access, the function fails.</p></td>
</tr>
</tbody>
</table>

### -param lpSecurityAttributes

A pointer to a [**SECURITY\_ATTRIBUTES**](https://docs.microsoft.com/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes) structure that contains two separate but related data members: an optional security descriptor, and a Boolean value that determines whether the returned handle can be inherited by child processes.
    
This parameter can be **NULL**.

If this parameter is **NULL**, the handle returned cannot be inherited by any child processes the application may create and the file or device associated with the returned handle gets a default security descriptor.

The **lpSecurityDescriptor** member of the structure specifies a [**SECURITY\_DESCRIPTOR**](../winnt/ns-winnt-security_descriptor.md) for a file or device. If this member is **NULL**, the file or device associated with the returned handle is assigned a default security descriptor.

This function ignores the **lpSecurityDescriptor** member when opening an existing file or device, but continues to use the **bInheritHandle** member.

The **bInheritHandle** member of the structure specifies whether the returned handle can be inherited.


### -param dwCreationDisposition

 An action to take on a file or device that exists or does not exist.
    
For devices other than files, this parameter is usually set to **OPEN\_EXISTING**.

For more information, see the Remarks section.

This parameter must be one of the following values, which cannot be combined:

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Meaning</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="CREATE_ALWAYS"></span><span id="create_always"></span>
<strong>CREATE_ALWAYS</strong>
2</td>
<td><p>Creates a new file, always.</p>
<p>If the specified file exists and is writable, the function truncates the file, the function succeeds, and last-error code is set to <strong>ERROR_ALREADY_EXISTS</strong> (183).</p>
<p>If the specified file does not exist and is a valid path, a new file is created, the function succeeds, and the last-error code is set to zero.</p>
<p>For more information, see the Remarks section of this topic.</p></td>
</tr>
<tr class="even">
<td><span id="CREATE_NEW"></span><span id="create_new"></span>
<strong>CREATE_NEW</strong>
1</td>
<td><p>Creates a new file, only if it does not already exist.</p>
<p>If the specified file exists, the function fails and the last-error code is set to <strong>ERROR_FILE_EXISTS</strong> (80).</p>
<p>If the specified file does not exist and is a valid path to a writable location, a new file is created.</p></td>
</tr>
<tr class="odd">
<td><span id="OPEN_ALWAYS"></span><span id="open_always"></span>
<strong>OPEN_ALWAYS</strong>
4</td>
<td><p>Opens a file, always.</p>
<p>If the specified file exists, the function succeeds and the last-error code is set to <strong>ERROR_ALREADY_EXISTS</strong> (183).</p>
<p>If the specified file does not exist and is a valid path to a writable location, the function creates a file and the last-error code is set to zero.</p></td>
</tr>
<tr class="even">
<td><span id="OPEN_EXISTING"></span><span id="open_existing"></span>
<strong>OPEN_EXISTING</strong>
3</td>
<td><p>Opens a file or device, only if it exists.</p>
<p>If the specified file or device does not exist, the function fails and the last-error code is set to <strong>ERROR_FILE_NOT_FOUND</strong> (2).</p>
<p>For more information about devices, see the Remarks section.</p></td>
</tr>
<tr class="odd">
<td><span id="TRUNCATE_EXISTING"></span><span id="truncate_existing"></span>
<strong>TRUNCATE_EXISTING</strong>
5</td>
<td><p>Opens a file and truncates it so that its size is zero bytes, only if it exists.</p>
<p>If the specified file does not exist, the function fails and the last-error code is set to <strong>ERROR_FILE_NOT_FOUND</strong> (2).</p>
<p>The calling process must open the file with the <strong>GENERIC_WRITE</strong> bit set as part of the <em>dwDesiredAccess</em> parameter.</p></td>
</tr>
</tbody>
</table>

### -param dwFlagsAndAttributes

The file or device attributes and flags, **FILE\_ATTRIBUTE\_NORMAL** being the most common default value for files.
    
This parameter can include any combination of the available file attributes (**FILE\_ATTRIBUTE\_\***). All other file attributes override **FILE\_ATTRIBUTE\_NORMAL**.

This parameter can also contain combinations of flags (**FILE\_FLAG\_\***) for control of file or device caching behavior, access modes, and other special-purpose flags. These combine with any **FILE\_ATTRIBUTE\_\*** values.

This parameter can also contain Security Quality of Service (SQOS) information by specifying the **SECURITY\_SQOS\_PRESENT** flag. Additional SQOS-related flags information is presented in the table following the attributes and flags tables.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th>Attribute</th>
<th>Meaning</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="FILE_ATTRIBUTE_ARCHIVE"></span><span id="file_attribute_archive"></span>
<strong>FILE_ATTRIBUTE_ARCHIVE</strong>
32 (0x20)</td>
<td><p>The file should be archived. Applications use this attribute to mark files for backup or removal.</p></td>
</tr>
<tr class="even">
<td><span id="FILE_ATTRIBUTE_ENCRYPTED"></span><span id="file_attribute_encrypted"></span>
<strong>FILE_ATTRIBUTE_ENCRYPTED</strong>
16384 (0x4000)</td>
<td><p>The file or directory is encrypted. For a file, this means that all data in the file is encrypted. For a directory, this means that encryption is the default for newly created files and subdirectories. For more information, see <a href="/windows/win32/fileio/file-encryption"><strong>File Encryption</strong></a>.</p>
<p>This flag has no effect if <strong>FILE_ATTRIBUTE_SYSTEM</strong> is also specified.</p>
<p>This flag is not supported on Home, Home Premium, Starter, or ARM editions of Windows.</p></td>
</tr>
<tr class="odd">
<td><span id="FILE_ATTRIBUTE_HIDDEN"></span><span id="file_attribute_hidden"></span>
<strong>FILE_ATTRIBUTE_HIDDEN</strong>
2 (0x2)</td>
<td><p>The file is hidden. Do not include it in an ordinary directory listing.</p></td>
</tr>
<tr class="even">
<td><span id="FILE_ATTRIBUTE_NORMAL"></span><span id="file_attribute_normal"></span>
<strong>FILE_ATTRIBUTE_NORMAL</strong>
128 (0x80)</td>
<td><p>The file does not have other attributes set. This attribute is valid only if used alone.</p></td>
</tr>
<tr class="odd">
<td><span id="FILE_ATTRIBUTE_OFFLINE"></span><span id="file_attribute_offline"></span>
<strong>FILE_ATTRIBUTE_OFFLINE</strong>
4096 (0x1000)</td>
<td><p>The data of a file is not immediately available. This attribute indicates that file data is physically moved to offline storage. This attribute is used by Remote Storage, the hierarchical storage management software. Applications should not arbitrarily change this attribute.</p></td>
</tr>
<tr class="even">
<td><span id="FILE_ATTRIBUTE_READONLY"></span><span id="file_attribute_readonly"></span>
<strong>FILE_ATTRIBUTE_READONLY</strong>
1 (0x1)</td>
<td><p>The file is read only. Applications can read the file, but cannot write to or delete it.</p></td>
</tr>
<tr class="odd">
<td><span id="FILE_ATTRIBUTE_SYSTEM"></span><span id="file_attribute_system"></span>
<strong>FILE_ATTRIBUTE_SYSTEM</strong>
4 (0x4)</td>
<td><p>The file is part of or used exclusively by an operating system.</p></td>
</tr>
<tr class="even">
<td><span id="FILE_ATTRIBUTE_TEMPORARY"></span><span id="file_attribute_temporary"></span>
<strong>FILE_ATTRIBUTE_TEMPORARY</strong>
256 (0x100)</td>
<td><p>The file is being used for temporary storage.</p>
<p>For more information, see the Caching Behavior section of this topic.</p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th>Flag</th>
<th>Meaning</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="FILE_FLAG_BACKUP_SEMANTICS"></span><span id="file_flag_backup_semantics"></span>
<strong>FILE_FLAG_BACKUP_SEMANTICS</strong>
0x02000000</td>
<td><p>The file is being opened or created for a backup or restore operation. The system ensures that the calling process overrides file security checks when the process has <strong>SE_BACKUP_NAME</strong> and <strong>SE_RESTORE_NAME</strong> privileges. For more information, see <a href="/windows/win32/secbp/changing-privileges-in-a-token">Changing Privileges in a Token</a>.</p>
<p>You must set this flag to obtain a handle to a directory. A directory handle can be passed to some functions instead of a file handle. For more information, see the Remarks section.</p></td>
</tr>
<tr class="even">
<td><span id="FILE_FLAG_DELETE_ON_CLOSE"></span><span id="file_flag_delete_on_close"></span>
<strong>FILE_FLAG_DELETE_ON_CLOSE</strong>
0x04000000</td>
<td><p>The file is to be deleted immediately after all of its handles are closed, which includes the specified handle and any other open or duplicated handles.</p>
<p>If there are existing open handles to a file, the call fails unless they were all opened with the <strong>FILE_SHARE_DELETE</strong> share mode.</p>
<p>Subsequent open requests for the file fail, unless the <strong>FILE_SHARE_DELETE</strong> share mode is specified.</p></td>
</tr>
<tr class="odd">
<td><span id="FILE_FLAG_NO_BUFFERING"></span><span id="file_flag_no_buffering"></span>
<strong>FILE_FLAG_NO_BUFFERING</strong>
0x20000000</td>
<td><p>The file or device is being opened with no system caching for data reads and writes. This flag does not affect hard disk caching or memory mapped files.</p>
<p>There are strict requirements for successfully working with files opened with this function using the <strong>FILE_FLAG_NO_BUFFERING</strong> flag, for details see <a href="/windows/win32/fileio/file-buffering">File Buffering</a>.</p></td>
</tr>
<tr class="even">
<td><span id="FILE_FLAG_OPEN_NO_RECALL"></span><span id="file_flag_open_no_recall"></span>
<strong>FILE_FLAG_OPEN_NO_RECALL</strong>
0x00100000</td>
<td><p>The file data is requested, but it should continue to be located in remote storage. It should not be transported back to local storage. This flag is for use by remote storage systems.</p></td>
</tr>
<tr class="odd">
<td><span id="FILE_FLAG_OPEN_REPARSE_POINT"></span><span id="file_flag_open_reparse_point"></span>
<strong>FILE_FLAG_OPEN_REPARSE_POINT</strong>
0x00200000</td>
<td><p>Normal <a href="/windows/win32/fileio/reparse-points">reparse point</a> processing will not occur; this function will attempt to open the reparse point. When a file is opened, a file handle is returned, whether or not the filter that controls the reparse point is operational.</p>
<p>This flag cannot be used with the <strong>CREATE_ALWAYS</strong> flag.</p>
<p>If the file is not a reparse point, then this flag is ignored.</p>
<p>For more information, see the Remarks section.</p></td>
</tr>
<tr class="even">
<td><span id="FILE_FLAG_OVERLAPPED"></span><span id="file_flag_overlapped"></span>
<strong>FILE_FLAG_OVERLAPPED</strong>
0x40000000</td>
<td><p>The file or device is being opened or created for asynchronous I/O.</p>
<p>When subsequent I/O operations are completed on this handle, the event specified in the <a href="/windows/win32/api/minwinbase/ns-minwinbase-overlapped"><strong>OVERLAPPED</strong></a> structure will be set to the signaled state.</p>
<p>If this flag is specified, the file can be used for simultaneous read and write operations.</p>
<p>If this flag is not specified, then I/O operations are serialized, even if the calls to the read and write functions specify an <a href="/windows/win32/api/minwinbase/ns-minwinbase-overlapped"><strong>OVERLAPPED</strong></a> structure.</p>
<p>For information about considerations when using a file handle created with this flag, see the Synchronous and Asynchronous I/O Handles section of this topic.</p></td>
</tr>
<tr class="odd">
<td><span id="FILE_FLAG_POSIX_SEMANTICS"></span><span id="file_flag_posix_semantics"></span>
<strong>FILE_FLAG_POSIX_SEMANTICS</strong>
0x0100000</td>
<td><p>Access will occur according to POSIX rules. This includes allowing multiple files with names, differing only in case, for file systems that support that naming. Use care when using this option, because files created with this flag may not be accessible by applications that are written for MS-DOS or 16-bit Windows.</p></td>
</tr>
<tr class="even">
<td><span id="FILE_FLAG_RANDOM_ACCESS"></span><span id="file_flag_random_access"></span>
<strong>FILE_FLAG_RANDOM_ACCESS</strong>
0x10000000</td>
<td><p>Access is intended to be random. The system can use this as a hint to optimize file caching.</p>
<p>This flag has no effect if the file system does not support cached I/O and <strong>FILE_FLAG_NO_BUFFERING</strong>.</p>
<p>For more information, see the Caching Behavior section of this topic.</p></td>
</tr>
<tr class="odd">
<td><span id="FILE_FLAG_SESSION_AWARE"></span><span id="file_flag_session_aware"></span>
<strong>FILE_FLAG_SESSION_AWARE</strong>
0x00800000</td>
<td><p>The file or device is being opened with session awareness. If this flag is not specified, then per-session devices (such as a device using RemoteFX USB Redirection) cannot be opened by processes running in session 0. This flag has no effect for callers not in session 0. This flag is supported only on server editions of Windows.</p></td>
</tr>
<tr class="even">
<td><span id="FILE_FLAG_SEQUENTIAL_SCAN"></span><span id="file_flag_sequential_scan"></span>
<strong>FILE_FLAG_SEQUENTIAL_SCAN</strong>
0x08000000</td>
<td><p>Access is intended to be sequential from beginning to end. The system can use this as a hint to optimize file caching.</p>
<p>This flag should not be used if read-behind (that is, reverse scans) will be used.</p>
<p>This flag has no effect if the file system does not support cached I/O and <strong>FILE_FLAG_NO_BUFFERING</strong>.</p>
<p>For more information, see the Caching Behavior section of this topic.</p></td>
</tr>
<tr class="odd">
<td><span id="FILE_FLAG_WRITE_THROUGH"></span><span id="file_flag_write_through"></span>
<strong>FILE_FLAG_WRITE_THROUGH</strong>
0x80000000</td>
<td><p>Write operations will not go through any intermediate cache, they will go directly to disk.</p>
<p>For additional information, see the Caching Behavior section of this topic.</p></td>
</tr>
</tbody>
</table>

 

The *dwFlagsAndAttributes*parameter can also specify SQOS information. For more information, see [Impersonation Levels](/windows/win32/secauthz/impersonation-levels). When the calling application specifies the **SECURITY\_SQOS\_PRESENT** flag as part of *dwFlagsAndAttributes*, it can also contain one or more of the following values.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th>Security flag</th>
<th>Meaning</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="SECURITY_ANONYMOUS"></span><span id="security_anonymous"></span>
<strong>SECURITY_ANONYMOUS</strong></td>
<td><p>Impersonates a client at the Anonymous impersonation level.</p></td>
</tr>
<tr class="even">
<td><span id="SECURITY_CONTEXT_TRACKING"></span><span id="security_context_tracking"></span>
<strong>SECURITY_CONTEXT_TRACKING</strong></td>
<td><p>The security tracking mode is dynamic. If this flag is not specified, the security tracking mode is static.</p></td>
</tr>
<tr class="odd">
<td><span id="SECURITY_DELEGATION"></span><span id="security_delegation"></span>
<strong>SECURITY_DELEGATION</strong></td>
<td><p>Impersonates a client at the Delegation impersonation level.</p></td>
</tr>
<tr class="even">
<td><span id="SECURITY_EFFECTIVE_ONLY"></span><span id="security_effective_only"></span>
<strong>SECURITY_EFFECTIVE_ONLY</strong></td>
<td><p>Only the enabled aspects of the client's security context are available to the server. If you do not specify this flag, all aspects of the client's security context are available.</p>
<p>This allows the client to limit the groups and privileges that a server can use while impersonating the client.</p></td>
</tr>
<tr class="odd">
<td><span id="SECURITY_IDENTIFICATION"></span><span id="security_identification"></span>
<strong>SECURITY_IDENTIFICATION</strong></td>
<td><p>Impersonates a client at the Identification impersonation level.</p></td>
</tr>
<tr class="even">
<td><span id="SECURITY_IMPERSONATION"></span><span id="security_impersonation"></span>
<strong>SECURITY_IMPERSONATION</strong></td>
<td><p>Impersonate a client at the impersonation level. This is the default behavior if no other flags are specified along with the <strong>SECURITY_SQOS_PRESENT</strong> flag.</p></td>
</tr>
</tbody>
</table>

### -param hTemplateFile

 A valid handle to a template file with the **GENERIC\_READ** access right. The template file supplies file attributes and extended attributes for the file that is being created.
    
This parameter can be **NULL**.

When opening an existing file, this parameter is ignored.

When opening a new encrypted file, the file inherits the discretionary access control list from its parent directory. For more information, see [File Encryption](/windows/win32/fileio/file-encryption).


## -returns

If the function succeeds, the return value is an open handle to the specified file, device, named pipe, or mail slot.

If the function fails, the return value is **INVALID\_HANDLE\_VALUE**. To get extended error information, call [**GetLastError**](../errhandlingapi/nf-errhandlingapi-getlasterror.md).


## -remarks

## -see-also

