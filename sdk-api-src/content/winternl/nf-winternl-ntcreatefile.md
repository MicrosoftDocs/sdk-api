---
UID: NF:winternl.NtCreateFile
title: NtCreateFile function (winternl.h)
description: Creates a new file or directory, or opens an existing file, device, directory, or volume.
helpviewer_keywords: ["DELETE","FILE_APPEND_DATA","FILE_COMPLETE_IF_OPLOCKED","FILE_CREATE","FILE_CREATE_TREE_CONNECTION","FILE_DELETE_ON_CLOSE","FILE_DIRECTORY_FILE","FILE_EXECUTE","FILE_GENERIC_EXECUTE","FILE_GENERIC_READ","FILE_GENERIC_WRITE","FILE_LIST_DIRECTORY","FILE_NON_DIRECTORY_FILE","FILE_NO_EA_KNOWLEDGE","FILE_NO_INTERMEDIATE_BUFFERING","FILE_OPEN","FILE_OPEN_BY_FILE_ID","FILE_OPEN_FOR_BACKUP_INTENT","FILE_OPEN_IF","FILE_OPEN_REPARSE_POINT","FILE_OPEN_REQUIRING_OPLOCK","FILE_OVERWRITE","FILE_OVERWRITE_IF","FILE_RANDOM_ACCESS","FILE_READ_ATTRIBUTES","FILE_READ_DATA","FILE_READ_EA","FILE_RESERVE_OPFILTER","FILE_SEQUENTIAL_ONLY","FILE_SHARE_DELETE","FILE_SHARE_READ","FILE_SHARE_WRITE","FILE_SUPERSEDE","FILE_SYNCHRONOUS_IO_ALERT","FILE_SYNCHRONOUS_IO_NONALERT","FILE_TRAVERSE","FILE_WRITE_ATTRIBUTES","FILE_WRITE_DATA","FILE_WRITE_EA","FILE_WRITE_THROUGH","HANDLE RootDirectory","NtCreateFile","NtCreateFile function [Windows API]","PSECURITY_DESCRIPTOR SecurityDescriptor","PSECURITY_QUALITY_OF_SERVICE SecurityQualityOfService","PUNICODE_STRING ObjectName","READ_CONTROL","SYNCHRONIZE","ULONG Attributes","ULONG Length","WRITE_DAC","WRITE_OWNER","winprog.ntcreatefile","winternl/NtCreateFile"]
old-location: winprog\ntcreatefile.htm
tech.root: winprog
ms.assetid: 82965665-8531-4cca-bf37-6044e154d43b
ms.date: 12/05/2018
ms.keywords: DELETE, FILE_APPEND_DATA, FILE_COMPLETE_IF_OPLOCKED, FILE_CREATE, FILE_CREATE_TREE_CONNECTION, FILE_DELETE_ON_CLOSE, FILE_DIRECTORY_FILE, FILE_EXECUTE, FILE_GENERIC_EXECUTE, FILE_GENERIC_READ, FILE_GENERIC_WRITE, FILE_LIST_DIRECTORY, FILE_NON_DIRECTORY_FILE, FILE_NO_EA_KNOWLEDGE, FILE_NO_INTERMEDIATE_BUFFERING, FILE_OPEN, FILE_OPEN_BY_FILE_ID, FILE_OPEN_FOR_BACKUP_INTENT, FILE_OPEN_IF, FILE_OPEN_REPARSE_POINT, FILE_OPEN_REQUIRING_OPLOCK, FILE_OVERWRITE, FILE_OVERWRITE_IF, FILE_RANDOM_ACCESS, FILE_READ_ATTRIBUTES, FILE_READ_DATA, FILE_READ_EA, FILE_RESERVE_OPFILTER, FILE_SEQUENTIAL_ONLY, FILE_SHARE_DELETE, FILE_SHARE_READ, FILE_SHARE_WRITE, FILE_SUPERSEDE, FILE_SYNCHRONOUS_IO_ALERT, FILE_SYNCHRONOUS_IO_NONALERT, FILE_TRAVERSE, FILE_WRITE_ATTRIBUTES, FILE_WRITE_DATA, FILE_WRITE_EA, FILE_WRITE_THROUGH, HANDLE RootDirectory, NtCreateFile, NtCreateFile function [Windows API], PSECURITY_DESCRIPTOR SecurityDescriptor, PSECURITY_QUALITY_OF_SERVICE SecurityQualityOfService, PUNICODE_STRING ObjectName, READ_CONTROL, SYNCHRONIZE, ULONG Attributes, ULONG Length, WRITE_DAC, WRITE_OWNER, winprog.ntcreatefile, winternl/NtCreateFile
req.header: winternl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ntdll.lib
req.dll: ntdll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NtCreateFile
 - winternl/NtCreateFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NtDll.dll
api_name:
 - NtCreateFile
---

# NtCreateFile function

## -description

Creates a new file or directory, or opens an existing file, device, directory, or volume.

This function is the user-mode equivalent to the <b>ZwCreateFile</b> function documented in the Windows Driver Kit (WDK).

## -parameters

### -param FileHandle [out]

A pointer to a variable that receives the file handle if the call is successful.

### -param DesiredAccess [in]

The <b>ACCESS_MASK</b> value that expresses the type of access that the caller requires to the file or directory. The set of system-defined <i>DesiredAccess</i> flags determines the following specific access rights for file objects.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DELETE"></a><a id="delete"></a><dl>
<dt><b>DELETE</b></dt>
</dl>
</td>
<td width="60%">
The file can be deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_READ_DATA"></a><a id="file_read_data"></a><dl>
<dt><b>FILE_READ_DATA</b></dt>
</dl>
</td>
<td width="60%">
Data can be read from the file.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_READ_ATTRIBUTES"></a><a id="file_read_attributes"></a><dl>
<dt><b>FILE_READ_ATTRIBUTES</b></dt>
</dl>
</td>
<td width="60%">
<i>FileAttributes</i> flags, described later, can be read.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_READ_EA"></a><a id="file_read_ea"></a><dl>
<dt><b>FILE_READ_EA</b></dt>
</dl>
</td>
<td width="60%">
Extended attributes associated with the file can be read. This flag is irrelevant to device and 
        intermediate drivers.

</td>
</tr>
<tr>
<td width="40%"><a id="READ_CONTROL"></a><a id="read_control"></a><dl>
<dt><b>READ_CONTROL</b></dt>
</dl>
</td>
<td width="60%">
The access control list (ACL) and ownership information associated with the file can be read.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_WRITE_DATA"></a><a id="file_write_data"></a><dl>
<dt><b>FILE_WRITE_DATA</b></dt>
</dl>
</td>
<td width="60%">
Data can be written to the file.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_WRITE_ATTRIBUTES"></a><a id="file_write_attributes"></a><dl>
<dt><b>FILE_WRITE_ATTRIBUTES</b></dt>
</dl>
</td>
<td width="60%">
<i>FileAttributes</i> flags can be written.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_WRITE_EA"></a><a id="file_write_ea"></a><dl>
<dt><b>FILE_WRITE_EA</b></dt>
</dl>
</td>
<td width="60%">
Extended attributes (EAs) associated with the file can be written. This flag is irrelevant to device and 
        intermediate drivers.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_APPEND_DATA"></a><a id="file_append_data"></a><dl>
<dt><b>FILE_APPEND_DATA</b></dt>
</dl>
</td>
<td width="60%">
Data can be appended to the file.

</td>
</tr>
<tr>
<td width="40%"><a id="WRITE_DAC"></a><a id="write_dac"></a><dl>
<dt><b>WRITE_DAC</b></dt>
</dl>
</td>
<td width="60%">
The discretionary access control list (DACL) associated with the file can be written.

</td>
</tr>
<tr>
<td width="40%"><a id="WRITE_OWNER"></a><a id="write_owner"></a><dl>
<dt><b>WRITE_OWNER</b></dt>
</dl>
</td>
<td width="60%">
Ownership information associated with the file can be written.

</td>
</tr>
<tr>
<td width="40%"><a id="SYNCHRONIZE"></a><a id="synchronize"></a><dl>
<dt><b>SYNCHRONIZE</b></dt>
</dl>
</td>
<td width="60%">
The returned <i>FileHandle</i> can be waited on to synchronize with the completion of 
        an I/O operation. If <i>FileHandle</i> was not opened for synchronous I/O, this value is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_EXECUTE"></a><a id="file_execute"></a><dl>
<dt><b>FILE_EXECUTE</b></dt>
</dl>
</td>
<td width="60%">
Data can be read into memory from the file using system paging I/O. This flag is irrelevant for device and 
        intermediate drivers.

</td>
</tr>
</table>
 
Do not specify <b>FILE_READ_DATA</b>, <b>FILE_WRITE_DATA</b>, <b>FILE_APPEND_DATA</b>, or <b>FILE_EXECUTE</b> when you create or open a directory.

Callers of <b>NtCreateFile</b> can specify one or a combination of the following, possibly using a bitwise-OR with additional compatible flags from the preceding <i>DesiredAccess</i> flags list, for any file object that does not represent a directory file.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_GENERIC_READ"></a><a id="file_generic_read"></a><dl>
<dt><b>FILE_GENERIC_READ</b></dt>
</dl>
</td>
<td width="60%">
<code>STANDARD_RIGHTS_READ | FILE_READ_DATA | 
        FILE_READ_ATTRIBUTES | FILE_READ_EA | SYNCHRONIZE</code>

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_GENERIC_WRITE"></a><a id="file_generic_write"></a><dl>
<dt><b>FILE_GENERIC_WRITE</b></dt>
</dl>
</td>
<td width="60%">
<code>STANDARD_RIGHTS_WRITE | FILE_WRITE_DATA | 
        FILE_WRITE_ATTRIBUTES | FILE_WRITE_EA |
        FILE_APPEND_DATA | SYNCHRONIZE</code>

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_GENERIC_EXECUTE"></a><a id="file_generic_execute"></a><dl>
<dt><b>FILE_GENERIC_EXECUTE</b></dt>
</dl>
</td>
<td width="60%">
<code>STANDARD_RIGHTS_EXECUTE | FILE_READ_ATTRIBUTES | FILE_EXECUTE | SYNCHRONIZE</code>

</td>
</tr>
</table>

The <b>FILE_GENERIC_EXECUTE</b>  value is irrelevant for device and intermediate drivers.

The <b>STANDARD_RIGHTS_</b><i>XXX</i> are predefined system values used to enforce security on system objects.

To open or create a directory file, as also indicated with the <i>CreateOptions</i> parameter, callers of <b>NtCreateFile</b> can specify one or a combination of the following, possibly using a bitwise-OR with one or more compatible flags from the preceding <i>DesiredAccess</i> flags list.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_LIST_DIRECTORY"></a><a id="file_list_directory"></a><dl>
<dt><b>FILE_LIST_DIRECTORY</b></dt>
</dl>
</td>
<td width="60%">
Files in the directory can be listed.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_TRAVERSE"></a><a id="file_traverse"></a><dl>
<dt><b>FILE_TRAVERSE</b></dt>
</dl>
</td>
<td width="60%">
The directory can be traversed: that is, it can be part of the pathname of a file.

</td>
</tr>
</table>

### -param ObjectAttributes [in]

A pointer to a structure already initialized with <b>InitializeObjectAttributes</b>. Members of this structure for a file object include the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ULONG_Length"></a><a id="ulong_length"></a><a id="ULONG_LENGTH"></a><dl>
<dt><b>ULONG Length</b></dt>
</dl>
</td>
<td width="60%">
Specifies the number of bytes of <i>ObjectAttributes</i> data supplied. This value must be at least sizeof(OBJECT_ATTRIBUTES).

</td>
</tr>
<tr>
<td width="40%"><a id="HANDLE_RootDirectory"></a><a id="handle_rootdirectory"></a><a id="HANDLE_ROOTDIRECTORY"></a><dl>
<dt><b>HANDLE RootDirectory</b></dt>
</dl>
</td>
<td width="60%">
Optionally specifies a handle to a directory obtained by a preceding call to <b>NtCreateFile</b>. If this value is <b>NULL</b>, the <b>ObjectName</b> member must be a fully qualified file specification that includes the full path to the target file. If this value is non-<b>NULL</b>, the <b>ObjectName</b> member specifies a file name relative to this directory.

</td>
</tr>
<tr>
<td width="40%"><a id="PUNICODE_STRING_ObjectName"></a><a id="punicode_string_objectname"></a><a id="PUNICODE_STRING_OBJECTNAME"></a><dl>
<dt><b>PUNICODE_STRING ObjectName</b></dt>
</dl>
</td>
<td width="60%">
Points to a buffered Unicode string that names the file to be created or opened. This value must be a fully qualified file specification or the name of a device object, unless it is the name of a file relative to the directory specified by <b>RootDirectory</b>. For example, \Device\Floppy1\myfile.dat or \??\B:\myfile.dat could be the fully qualified file specification, provided that the floppy driver and overlying file system are already loaded. For more information, see <a href="/windows/desktop/FileIO/naming-a-file">File Names, Paths, and Namespaces</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="ULONG_Attributes"></a><a id="ulong_attributes"></a><a id="ULONG_ATTRIBUTES"></a><dl>
<dt><b>ULONG Attributes</b></dt>
</dl>
</td>
<td width="60%">
Is a set of flags that controls the file object attributes. This value can be zero or <b>OBJ_CASE_INSENSITIVE</b>, which indicates that name-lookup code should ignore the case of the <b>ObjectName</b> member rather than performing an exact-match search. The value <b>OBJ_INHERIT</b> is irrelevant to device and intermediate drivers.

</td>
</tr>
<tr>
<td width="40%"><a id="PSECURITY_DESCRIPTOR_SecurityDescriptor"></a><a id="psecurity_descriptor_securitydescriptor"></a><a id="PSECURITY_DESCRIPTOR_SECURITYDESCRIPTOR"></a><dl>
<dt><b>PSECURITY_DESCRIPTOR SecurityDescriptor</b></dt>
</dl>
</td>
<td width="60%">
Optionally specifies a security descriptor to be applied to a file. ACLs specified by such a security descriptor are applied to the file only when it is created. If the value is <b>NULL</b> when a file is created, the ACL placed on the file is file-system-dependent; most file systems propagate some part of such an ACL from the parent directory file combined with the caller's default ACL. Device and intermediate drivers can set this member to <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="PSECURITY_QUALITY_OF_SERVICE_SecurityQualityOfService"></a><a id="psecurity_quality_of_service_securityqualityofservice"></a><a id="PSECURITY_QUALITY_OF_SERVICE_SECURITYQUALITYOFSERVICE"></a><dl>
<dt><b>PSECURITY_QUALITY_OF_SERVICE SecurityQualityOfService</b></dt>
</dl>
</td>
<td width="60%">
Specifies the access rights a server should be given to the client's security context. This value is non-<b>NULL</b> only when a connection to a protected server is established, allowing the caller to control which parts of the caller's security context are made available to the server and whether the server is allowed to impersonate the caller.

</td>
</tr>
</table>

### -param IoStatusBlock [out]

A pointer to a variable that receives the final completion status and information about the requested operation. On return from <b>NtCreateFile</b>, the <b>Information</b> member contains one of the following values:

<ul>
<li><b>FILE_CREATED</b></li>
<li><b>FILE_OPENED</b></li>
<li><b>FILE_OVERWRITTEN</b></li>
<li><b>FILE_SUPERSEDED</b></li>
<li><b>FILE_EXISTS</b></li>
<li><b>FILE_DOES_NOT_EXIST</b></li>
</ul>

### -param AllocationSize [in, optional]

The initial allocation size in bytes for the file. A nonzero value has no effect unless the file is being created, overwritten, or superseded.

### -param FileAttributes [in]

The file attributes. Explicitly specified attributes are applied only when the file is created, superseded, or, in some cases, overwritten. By default, this value is a <b>FILE_ATTRIBUTE_NORMAL</b>, which can be overridden by an ORed combination of one or more <b>FILE_ATTRIBUTE_</b><i>xxxx</i> flags, which are defined in Wdm.h and NtDdk.h. For a list of flags that can be used with <b>NtCreateFile</b>, see <b>CreateFile</b>.

### -param ShareAccess [in]

The type of share access that the caller would like to use in  the file, as zero, or as one or a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_SHARE_READ"></a><a id="file_share_read"></a><dl>
<dt><b>FILE_SHARE_READ</b></dt>
</dl>
</td>
<td width="60%">
The file can be opened for read access by other threads' calls to <b>NtCreateFile</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SHARE_WRITE"></a><a id="file_share_write"></a><dl>
<dt><b>FILE_SHARE_WRITE</b></dt>
</dl>
</td>
<td width="60%">
The file can be opened for write access by other threads' calls to <b>NtCreateFile</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SHARE_DELETE"></a><a id="file_share_delete"></a><dl>
<dt><b>FILE_SHARE_DELETE</b></dt>
</dl>
</td>
<td width="60%">
The file can be opened for delete access by other threads' calls to <b>NtCreateFile</b>.

</td>
</tr>
</table>

For more information, see the Windows SDK.

### -param CreateDisposition [in]

Specifies what to do, depending on whether the file already exists, as one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_SUPERSEDE"></a><a id="file_supersede"></a><dl>
<dt><b>FILE_SUPERSEDE</b></dt>
</dl>
</td>
<td width="60%">
If the file already exists, replace it with the given file. If it does not, create the given file.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_CREATE"></a><a id="file_create"></a><dl>
<dt><b>FILE_CREATE</b></dt>
</dl>
</td>
<td width="60%">
If the file already exists, fail the request and do not create or open the given file. If it does not, create the given file.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_OPEN"></a><a id="file_open"></a><dl>
<dt><b>FILE_OPEN</b></dt>
</dl>
</td>
<td width="60%">
If the file already exists, open it instead of creating a new file. If it does not, fail the request and do not create a new file.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_OPEN_IF"></a><a id="file_open_if"></a><dl>
<dt><b>FILE_OPEN_IF</b></dt>
</dl>
</td>
<td width="60%">
If the file already exists, open it. If it does not, create the given file.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_OVERWRITE"></a><a id="file_overwrite"></a><dl>
<dt><b>FILE_OVERWRITE</b></dt>
</dl>
</td>
<td width="60%">
If the file already exists, open it and overwrite it. If it does not, fail the request.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_OVERWRITE_IF"></a><a id="file_overwrite_if"></a><dl>
<dt><b>FILE_OVERWRITE_IF</b></dt>
</dl>
</td>
<td width="60%">
If the file already exists, open it and overwrite it. If it does not, create the given file.

</td>
</tr>
</table>

### -param CreateOptions [in]

The options to be applied when creating or opening the file, as a compatible combination of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_DIRECTORY_FILE"></a><a id="file_directory_file"></a><dl>
<dt><b>FILE_DIRECTORY_FILE</b></dt>
</dl>
</td>
<td width="60%">
The file being created or opened is a directory file. With this flag, the <i>CreateDisposition</i> parameter must be set to <b>FILE_CREATE</b>, <b>FILE_OPEN</b>, or <b>FILE_OPEN_IF</b>. With this flag, other compatible <i>CreateOptions</i> flags include only the following: <b>FILE_SYNCHRONOUS_IO_ALERT</b>, <b>FILE_SYNCHRONOUS_IO _NONALERT</b>, <b>FILE_WRITE_THROUGH</b>, <b>FILE_OPEN_FOR_BACKUP_INTENT</b>, and <b>FILE_OPEN_BY_FILE_ID</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_NON_DIRECTORY_FILE"></a><a id="file_non_directory_file"></a><dl>
<dt><b>FILE_NON_DIRECTORY_FILE</b></dt>
</dl>
</td>
<td width="60%">
The file being opened must not be a directory file or this call fails. The file object being opened can represent a data file, a logical, virtual, or physical device, or a volume.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_WRITE_THROUGH"></a><a id="file_write_through"></a><dl>
<dt><b>FILE_WRITE_THROUGH</b></dt>
</dl>
</td>
<td width="60%">
Applications that write data to the file must actually transfer the data into the file before any requested write operation is considered complete. This flag is automatically set if the <i>CreateOptions</i> flag <b>FILE_NO_INTERMEDIATE _BUFFERING</b> is set.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SEQUENTIAL_ONLY"></a><a id="file_sequential_only"></a><dl>
<dt><b>FILE_SEQUENTIAL_ONLY</b></dt>
</dl>
</td>
<td width="60%">
All accesses to the file are sequential.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_RANDOM_ACCESS"></a><a id="file_random_access"></a><dl>
<dt><b>FILE_RANDOM_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
Accesses to the file can be random, so no sequential read-ahead operations should be performed on the file by FSDs or the system.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_NO_INTERMEDIATE_BUFFERING"></a><a id="file_no_intermediate_buffering"></a><dl>
<dt><b>FILE_NO_INTERMEDIATE_BUFFERING</b></dt>
</dl>
</td>
<td width="60%">
The file cannot be cached or buffered in a driver's internal buffers. This flag is incompatible with the <i>DesiredAccess</i> <b>FILE_APPEND_DATA</b> 
        flag.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SYNCHRONOUS_IO_ALERT"></a><a id="file_synchronous_io_alert"></a><dl>
<dt><b>FILE_SYNCHRONOUS_IO_ALERT</b></dt>
</dl>
</td>
<td width="60%">
All operations on the file are performed synchronously. Any wait on behalf of the caller is subject to premature termination from alerts. This flag also causes the I/O system to maintain the file position context. If this flag is set, the <i>DesiredAccess</i> <b>SYNCHRONIZE</b> flag also must be set.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SYNCHRONOUS_IO_NONALERT"></a><a id="file_synchronous_io_nonalert"></a><dl>
<dt><b>FILE_SYNCHRONOUS_IO_NONALERT</b></dt>
</dl>
</td>
<td width="60%">
All operations on the file are performed synchronously. Waits in the system to synchronize I/O queuing and completion are not subject to alerts. This flag also causes the I/O system to maintain the file position context. If this flag is set, the <i>DesiredAccess</i> <b>SYNCHRONIZE</b> flag also must be set.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_CREATE_TREE_CONNECTION"></a><a id="file_create_tree_connection"></a><dl>
<dt><b>FILE_CREATE_TREE_CONNECTION</b></dt>
</dl>
</td>
<td width="60%">
Create a tree connection for this file in order to open it over the network. This flag is not used by device and intermediate drivers.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_NO_EA_KNOWLEDGE"></a><a id="file_no_ea_knowledge"></a><dl>
<dt><b>FILE_NO_EA_KNOWLEDGE</b></dt>
</dl>
</td>
<td width="60%">
If the extended attributes on an existing file being opened indicate that the caller must understand EAs to properly interpret the file, fail this request because the caller does not understand how to deal with EAs. This flag is irrelevant for device and intermediate drivers.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_OPEN_REPARSE_POINT"></a><a id="file_open_reparse_point"></a><dl>
<dt><b>FILE_OPEN_REPARSE_POINT</b></dt>
</dl>
</td>
<td width="60%">
Open a file with a reparse point and bypass normal reparse point processing for the file. For more information, see the Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_DELETE_ON_CLOSE"></a><a id="file_delete_on_close"></a><dl>
<dt><b>FILE_DELETE_ON_CLOSE</b></dt>
</dl>
</td>
<td width="60%">
Delete the file when the last handle to it is passed to <b>NtClose</b>. If this flag is set, the DELETE flag must be set in the <i>DesiredAccess</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_OPEN_BY_FILE_ID"></a><a id="file_open_by_file_id"></a><dl>
<dt><b>FILE_OPEN_BY_FILE_ID</b></dt>
</dl>
</td>
<td width="60%">
The file name that is specified by the <i>ObjectAttributes</i> parameter includes the 8-byte file reference number for the file. This number is assigned by and specific to the particular file system. If the file is a reparse point, the file name will also include the name of a device. Note that the FAT file system does not support this flag. This flag is not used by device and intermediate drivers.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_OPEN_FOR_BACKUP_INTENT"></a><a id="file_open_for_backup_intent"></a><dl>
<dt><b>FILE_OPEN_FOR_BACKUP_INTENT</b></dt>
</dl>
</td>
<td width="60%">
The file is being opened for backup intent. Therefore, the system should check for certain access rights and grant the caller the appropriate access to the file before checking the <i>DesiredAccess</i> parameter against the file's security descriptor. This flag not used by device and intermediate drivers.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_RESERVE_OPFILTER_"></a><a id="file_reserve_opfilter_"></a><dl>
<dt><b>FILE_RESERVE_OPFILTER </b></dt>
</dl>
</td>
<td width="60%">
This flag allows an application to request a filter <a href="/windows/win32/fileio/opportunistic-locks">opportunistic lock</a> to prevent other applications from getting share violations. If there are already open handles, the create request will fail with <b>STATUS_OPLOCK_NOT_GRANTED</b>. For more information, see the Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_OPEN_REQUIRING_OPLOCK"></a><a id="file_open_requiring_oplock"></a><dl>
<dt><b>FILE_OPEN_REQUIRING_OPLOCK</b></dt>
</dl>
</td>
<td width="60%">
The file is being opened and an <a href="/windows/win32/fileio/opportunistic-locks">opportunistic lock</a> on the file is being requested as a single atomic operation. The file system checks for oplocks before it performs the create operation and will fail the create with a return code of <b>STATUS_CANNOT_BREAK_OPLOCK</b> if the result would be to break an existing oplock.  For more information, see the Remarks section.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This flag is not supported.

This flag is supported on the following file systems: NTFS, FAT, and exFAT.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_COMPLETE_IF_OPLOCKED"></a><a id="file_complete_if_oplocked"></a><dl>
<dt><b>FILE_COMPLETE_IF_OPLOCKED</b></dt>
</dl>
</td>
<td width="60%">
Complete this operation immediately with an alternate success code of <b>STATUS_OPLOCK_BREAK_IN_PROGRESS</b> if the target file is oplocked, rather than blocking the caller's thread. If the file is <a href="/windows/win32/fileio/opportunistic-locks">oplocked</a>, another caller already has access to the file. This flag is not used by device and intermediate drivers.

</td>
</tr>
</table>

### -param EaBuffer [in]

Pointer to an EA buffer used to pass extended attributes.
      

<div class="alert"><b>Note</b>  Some file systems may not support EA buffers.</div>
<div> </div>

### -param EaLength [in]

Length of the EA buffer.

## -returns

<b>NtCreateFile</b> returns either <b>STATUS_SUCCESS</b> or an appropriate error status. If it returns an error status, the caller can find more information about the cause of the failure by checking the <i>IoStatusBlock</i>. To simplify this check, an application can use the <b>NT_SUCCESS</b>, <b>NT_ERROR</b>, and <b>NT_WARNING</b> macros.

## -remarks

The handle, given by <b>NtCreateFile</b>, can be used by subsequent calls to manipulate data within the file or the file object's state or attributes.

There are two alternate ways to specify the name of the file to be created or opened with <b>NtCreateFile</b>:

<ul>
<li>As a fully qualified pathname, supplied in the <b>ObjectName</b> member of the input <i>ObjectAttributes</i></li>
<li>As a pathname relative to the directory file represented by the handle in the <b>RootDirectory</b> member of the input <i>ObjectAttributes</i></li>
</ul>

Certain <i>DesiredAccess</i> flags and combinations of flags have the following effects:

<ul>
<li>For a caller to synchronize an I/O completion by waiting on the returned <i>FileHandle</i>, the <b>SYNCHRONIZE</b> flag must be set.</li>
<li>Passing a zero to <i>DesiredAccess</i> is not valid.</li>
<li>If only the <b>FILE_APPEND_DATA</b> and <b>SYNCHRONIZE</b> flags are set, the caller can write only to the end of the file, and any offset information on writes to the file is ignored. However, the file is automatically  extended as necessary for this type of write operation.</li>
<li>Setting the <b>FILE_WRITE_DATA</b> flag for a file also allows writes beyond the end of the file to occur. The file is automatically extended for this type of write, as well.</li>
<li>If only the <b>FILE_EXECUTE</b> and <b>SYNCHRONIZE</b> flags are set, the caller cannot directly read or write any data in the file using the returned <i>FileHandle</i>, that is, all operations on the file occur through the system pager in response to instruction and data accesses. </li>
</ul>

The <i>ShareAccess</i> parameter determines whether separate threads can access the same file, possibly simultaneously. Provided that both file openers have the privilege to access a file in the specified manner, the file can be successfully opened and shared. If the original caller of <b>NtCreateFile</b> does not specify <b>FILE_SHARE_READ</b>, <b>FILE_SHARE_WRITE</b>, or <b>FILE_SHARE_DELETE</b>, no other open operations can be performed on the file; that is, the original caller is given exclusive access to the file.

For a shared file to be successfully opened, the requested <i>DesiredAccess</i> parameter to the file must be compatible with both the <i>DesiredAccess</i> and <i>ShareAccess</i> specifications of all preceding opens that have not yet been released with <b>NtClose</b>. That is, the <i>DesiredAccess</i> parameter specified to <b>NtCreateFile</b> for a given file must not conflict with the accesses that other openers of the file have disallowed.

The <i>CreateDisposition</i> value <b>FILE_SUPERSEDE</b> requires that the caller have <b>DELETE</b> access to an existing file object. If so, a successful call to <b>NtCreateFile</b> with <b>FILE_SUPERSEDE</b> on an existing file effectively deletes that file, and then re-creates it. This implies that, if the file has already been opened by another thread, it opened the file by specifying a <i>ShareAccess</i> parameter with the <b>FILE_SHARE_DELETE</b> flag set. 

Note that this type of disposition is consistent with the POSIX style of overwriting files. The <i>CreateDisposition</i> values <b>FILE_OVERWRITE_IF</b> and <b>FILE_SUPERSEDE</b> are similar. If <b>ZwCreateFile</b> is called with an existing file and either of these <i>CreateDisposition</i> values, the file is replaced.

Overwriting a file is semantically equivalent to a supersede operation, except for the following:

<ul>
<li>The caller must have write access to the file, rather than delete access. This implies that, if the file has already been opened by another thread, it opened the file with the <b>FILE_SHARE_WRITE</b> flag set in the input <i>ShareAccess</i> parameter.</li>
<li>The specified file attributes are logically ORed with those already on the file. This implies that, if the file has already been opened by another thread, a subsequent caller of <b>NtCreateFile</b> cannot disable existing <i>FileAttributes</i> flags but can enable additional flags for the same file. Note that this style of overwriting files is consistent with MS-DOS, Windows 3.1, and  OS/2 operating systems.</li>
</ul>

The <i>CreateOptions</i> <b>FILE_DIRECTORY_FILE</b> value specifies that the file to be created or opened is a 
     directory file. When a directory file is created, the file system creates an appropriate structure on the disk to 
     represent an empty directory for that particular file system's on-disk structure. If this option was specified 
     and the given file to be opened is not a directory file, or if the caller specified an inconsistent 
     <i>CreateOptions</i> or <i>CreateDisposition</i> value, the call to 
     <b>NtCreateFile</b> fails.

The <i>CreateOptions</i> <b>FILE_NO_INTERMEDIATE_BUFFERING</b> flag prevents the file system from performing any 
     intermediate buffering on behalf of the caller. Specifying this value places certain restrictions on the caller's 
     parameters to other <b>Nt<i>XXX</i>File</b> routines, including the 
     following:

<ul>
<li>Any optional <i>ByteOffset</i> passed to  the 
      <b>NtReadFile</b> or <b>NtWriteFile</b> function must be an 
      integral of the sector size.</li>
<li>The <i>Length</i> passed to <b>NtReadFile</b> or 
      <b>NtWriteFile</b>, must be an integral of the sector size. Note that specifying a 
      read operation to a buffer whose length is exactly the sector size might result in a lesser number of 
      significant bytes being transferred to that buffer if the end of the file was reached during the transfer.</li>
<li>Buffers must be adjusted in accordance with the alignment requirement of the underlying device. This 
      information can be obtained by calling <b>NtCreateFile</b> 
      to get a handle for the file object that represents the physical device, and then calling 
      <b>NtQueryInformationFile</b> with that handle. For a list of the system 
       <b>FILE_</b><i>XXX</i><b>_ALIGNMENT</b> values, see 
       the Windows SDK documentation.</li>
<li>Calls to <b>NtSetInformationFile</b> with the 
      <i>FileInformationClass</i> parameter set to 
      <b>FilePositionInformation</b> must specify an offset that is an integral of the 
      sector size.</li>
</ul>
The <i>CreateOptions</i> <b>FILE_SYNCHRONOUS_IO_ALERT</b> and <b>FILE_SYNCHRONOUS_IO_NONALERT</b> flags, 
     which are mutually exclusive as their names suggest, specify that all I/O operations on the file are to be 
     synchronous as long as they occur through the file object referred to by the returned 
     <i>FileHandle</i>. All I/O on such a file is serialized across all threads using the returned 
     handle. With either of these <i>CreateOptions</i>, the <i>DesiredAccess</i> <b>SYNCHRONIZE</b> flag must be set so that the I/O Manager  uses the 
     file object as a synchronization object. With either of these <i>CreateOptions</i> set, the 
     I/O Manager maintains the "file position context" for the file object, an internal, current file position offset. 
     This offset can be used in calls to <b>NtReadFile</b> and 
     <b>NtWriteFile</b>. Its position also can be queried or set with 
     <b>NtQueryInformationFile</b> and 
     <b>NtSetInformationFile</b>.

If the <i>CreateOptions</i> parameter specifies the <b>FILE_OPEN_REPARSE_POINT</b> flag and <b>NtCreateFile</b> opens a file with a reparse point, normal reparse processing does not occur and <b>NtCreateFile</b> attempts to directly open the reparse point file. If the <b>FILE_OPEN_REPARSE_POINT</b> flag is not specified, normal reparse point processing occurs for the file. In either case, if the open operation was successful, <b>NtCreateFile</b> returns <b>STATUS_SUCCESS</b>; otherwise, an error code. The <b>NtCreateFile</b> function never returns <b>STATUS_REPARSE</b>.

The <i>CreateOptions</i> parameter's <b>FILE_OPEN_REQUIRING_OPLOCK</b> flag eliminates the time between when you open the file and request an oplock that could potentially allow a third party to open the file, which would cause a sharing violation. An application can use the <b>FILE_OPEN_REQUIRING_OPLOCK</b> flag with <b>NtCreateFile</b> and then request any oplock. This ensures that an oplock owner will be notified of any subsequent open request that causes a sharing violation. 

In Windows 7, if other handles exist on the file when an application uses this flag, the create operation will fail with <b>STATUS_OPLOCK_NOT_GRANTED</b>. This restriction no longer exists starting with Windows 8.

If this create operation would break an oplock that already exists on the file, then setting the <b>FILE_OPEN_REQUIRING_OPLOCK</b> flag will cause the create operation to fail with <b>STATUS_CANNOT_BREAK_OPLOCK</b>. The existing oplock will not be broken by this create operation.

An application that uses the FILE_OPEN_REQUIRING_OPLOCK flag must request an oplock on the file after this call succeeds, or all subsequent attempts to open the file will be blocked without the benefit of normal oplock processing. Similarly, if this call succeeds but the subsequent oplock request fails, an application that uses this flag must close its handle after it detects that the oplock request has failed. The application must not perform any other file system operation on the file before requsting the oplock (besides closing the file handle), otherwise a deadlock may occur.

<div class="alert"><b>Note</b>  The <b>FILE_OPEN_REQUIRING_OPLOCK</b> flag is available in Windows 7, Windows Server 2008 R2 and later operating systems for the following file systems: NTFS, FAT, and exFAT.
</div>
<div> </div>



The <i>CreateOptions</i> parameter's <b>FILE_RESERVE_OPFILTER</b> flag allows an application to request a Level 1, Batch, or Filter oplock to prevent other applications from getting share violations. However, in practical terms, the <b>FILE_RESERVE_OPFILTER</b> is useful only for filter oplocks. To use it, you must complete the following steps:



<ol>
<li>Issue a create request with <i>CreateOptions</i> of <b>FILE_RESERVE_OPFILTER</b>, <i>DesiredAccess</i> of exactly <b>FILE_READ_ATTRIBUTES</b>, and <i>ShareAccess</i> of exactly <code>(FILE_SHARE_READ | FILE_SHARE_WRITE | FILE_SHARE_DELETE)</code>. Possible failures are as follows:<ul>
<li>If there are already open handles, the create request fails with <b>STATUS_OPLOCK_NOT_GRANTED</b>, and the next requested oplock also fails. </li>
<li>If you open with more access than <b>FILE_READ_ATTRIBUTES</b>  or less sharing than <code>(FILE_SHARE_READ | FILE_SHARE_WRITE | FILE_SHARE_DELETE)</code>, the request  fails with <b>STATUS_OPLOCK_NOT_GRANTED</b>.</li>
</ul>
</li>
<li>If the create request succeeds, request an oplock.</li>
<li>Open another handle to the file to do I/O.</li>
</ol>Step three makes this practical only for filter oplocks. The handle opened in step three can have a <i>DesiredAccess</i> that contains a maximum of <code>(FILE_READ_ATTRIBUTES | FILE_WRITE_ATTRIBUTES | FILE_READ_DATA | FILE_READ_EA | FILE_EXECUTE | SYNCHRONIZE | READ_CONTROL)</code> and still not break a filter oplock. However, any <i>DesiredAccess</i> greater than <code>(FILE_READ_ATTRIBUTES | FILE_WRITE_ATTRIBUTES | SYNCHRONIZE)</code> will break a Level 1 or Batch oplock and make the <b>FILE_RESERVE_OPFILTER</b> flag useless for those oplock types.



NTFS is the only Microsoft file system that implements <b>FILE_RESERVE_OPFILTER</b>.

For more information on oplocks, see [Opportunistic Locks](/windows/win32/fileio/opportunistic-locks).

Note that the WDK header file NtDef.h is necessary for many constant definitions. You can also use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to NtDll.dll.
