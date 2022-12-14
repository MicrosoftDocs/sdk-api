---
UID: NS:fileapi._CREATEFILE2_EXTENDED_PARAMETERS
title: CREATEFILE2_EXTENDED_PARAMETERS (fileapi.h)
description: Contains optional extended parameters for CreateFile2.
helpviewer_keywords: ["*LPCREATEFILE2_EXTENDED_PARAMETERS","*PCREATEFILE2_EXTENDED_PARAMETERS","CREATEFILE2_EXTENDED_PARAMETERS","CREATEFILE2_EXTENDED_PARAMETERS structure [Files]","FILE_ATTRIBUTE_ARCHIVE","FILE_ATTRIBUTE_ENCRYPTED","FILE_ATTRIBUTE_HIDDEN","FILE_ATTRIBUTE_INTEGRITY_STREAM","FILE_ATTRIBUTE_NORMAL","FILE_ATTRIBUTE_OFFLINE","FILE_ATTRIBUTE_READONLY","FILE_ATTRIBUTE_SYSTEM","FILE_ATTRIBUTE_TEMPORARY","FILE_FLAG_BACKUP_SEMANTICS","FILE_FLAG_DELETE_ON_CLOSE","FILE_FLAG_NO_BUFFERING","FILE_FLAG_OPEN_NO_RECALL","FILE_FLAG_OPEN_REPARSE_POINT","FILE_FLAG_OPEN_REQUIRING_OPLOCK","FILE_FLAG_OVERLAPPED","FILE_FLAG_POSIX_SEMANTICS","FILE_FLAG_RANDOM_ACCESS","FILE_FLAG_SEQUENTIAL_SCAN","FILE_FLAG_SESSION_AWARE","FILE_FLAG_WRITE_THROUGH","LPCREATEFILE2_EXTENDED_PARAMETERS","LPCREATEFILE2_EXTENDED_PARAMETERS structure pointer [Files]","PCREATEFILE2_EXTENDED_PARAMETERS","PCREATEFILE2_EXTENDED_PARAMETERS structure pointer [Files]","SECURITY_ANONYMOUS","SECURITY_CONTEXT_TRACKING","SECURITY_DELEGATION","SECURITY_EFFECTIVE_ONLY","SECURITY_IDENTIFICATION","SECURITY_IMPERSONATION","fileapi/CREATEFILE2_EXTENDED_PARAMETERS","fileapi/LPCREATEFILE2_EXTENDED_PARAMETERS","fileapi/PCREATEFILE2_EXTENDED_PARAMETERS","fs.createfile2_extended_parameters"]
old-location: fs\createfile2_extended_parameters.htm
tech.root: fs
ms.assetid: efe68dfc-f13d-47de-9443-30404977e26f
ms.date: 12/05/2018
ms.keywords: '*LPCREATEFILE2_EXTENDED_PARAMETERS, *PCREATEFILE2_EXTENDED_PARAMETERS, CREATEFILE2_EXTENDED_PARAMETERS, CREATEFILE2_EXTENDED_PARAMETERS structure [Files], FILE_ATTRIBUTE_ARCHIVE, FILE_ATTRIBUTE_ENCRYPTED, FILE_ATTRIBUTE_HIDDEN, FILE_ATTRIBUTE_INTEGRITY_STREAM, FILE_ATTRIBUTE_NORMAL, FILE_ATTRIBUTE_OFFLINE, FILE_ATTRIBUTE_READONLY, FILE_ATTRIBUTE_SYSTEM, FILE_ATTRIBUTE_TEMPORARY, FILE_FLAG_BACKUP_SEMANTICS, FILE_FLAG_DELETE_ON_CLOSE, FILE_FLAG_NO_BUFFERING, FILE_FLAG_OPEN_NO_RECALL, FILE_FLAG_OPEN_REPARSE_POINT, FILE_FLAG_OPEN_REQUIRING_OPLOCK, FILE_FLAG_OVERLAPPED, FILE_FLAG_POSIX_SEMANTICS, FILE_FLAG_RANDOM_ACCESS, FILE_FLAG_SEQUENTIAL_SCAN, FILE_FLAG_SESSION_AWARE, FILE_FLAG_WRITE_THROUGH, LPCREATEFILE2_EXTENDED_PARAMETERS, LPCREATEFILE2_EXTENDED_PARAMETERS structure pointer [Files], PCREATEFILE2_EXTENDED_PARAMETERS, PCREATEFILE2_EXTENDED_PARAMETERS structure pointer [Files], SECURITY_ANONYMOUS, SECURITY_CONTEXT_TRACKING, SECURITY_DELEGATION, SECURITY_EFFECTIVE_ONLY, SECURITY_IDENTIFICATION, SECURITY_IMPERSONATION, fileapi/CREATEFILE2_EXTENDED_PARAMETERS, fileapi/LPCREATEFILE2_EXTENDED_PARAMETERS, fileapi/PCREATEFILE2_EXTENDED_PARAMETERS, fs.createfile2_extended_parameters'
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CREATEFILE2_EXTENDED_PARAMETERS, *PCREATEFILE2_EXTENDED_PARAMETERS, *LPCREATEFILE2_EXTENDED_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CREATEFILE2_EXTENDED_PARAMETERS
 - fileapi/_CREATEFILE2_EXTENDED_PARAMETERS
 - PCREATEFILE2_EXTENDED_PARAMETERS
 - fileapi/PCREATEFILE2_EXTENDED_PARAMETERS
 - CREATEFILE2_EXTENDED_PARAMETERS
 - fileapi/CREATEFILE2_EXTENDED_PARAMETERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FileAPI.h
api_name:
 - CREATEFILE2_EXTENDED_PARAMETERS
---

# CREATEFILE2_EXTENDED_PARAMETERS structure


## -description

Contains optional extended parameters for 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-createfile2">CreateFile2</a>.

## -struct-fields

### -field dwSize

Contains the size of this structure, 
      <code>sizeof(CREATEFILE2_EXTENDED_PARAMETERS)</code>.

### -field dwFileAttributes

The file or device attributes and flags, <b>FILE_ATTRIBUTE_NORMAL</b> being the most 
       common default value for files.

This parameter can include any combination of the available file attributes 
       (<b>FILE_ATTRIBUTE_*</b>). All other file attributes override 
       <b>FILE_ATTRIBUTE_NORMAL</b>.

<div class="alert"><b>Note</b>  When <a href="/windows/desktop/api/fileapi/nf-fileapi-createfile2">CreateFile2</a> opens an existing file, it generally 
       combines the file flags with the file attributes of the existing file, and ignores any file attributes supplied 
       as part of <i>dwFlagsAndAttributes</i>. Special cases are detailed in 
       <a href="/windows/desktop/FileIO/creating-and-opening-files">Creating and Opening Files</a>.</div>
<div> </div>
Some of the following file attributes and flags may only apply to files and not necessarily all other types 
       of devices that <a href="/windows/desktop/api/fileapi/nf-fileapi-createfile2">CreateFile2</a> can open. For additional 
       information, see the Remarks section of the 
       <a href="/windows/desktop/api/fileapi/nf-fileapi-createfile2">CreateFile2</a> reference page and 
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

This flag is not supported when called from a Windows Store app.

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
<td width="40%"><a id="FILE_ATTRIBUTE_INTEGRITY_STREAM"></a><a id="file_attribute_integrity_stream"></a><dl>
<dt><b>FILE_ATTRIBUTE_INTEGRITY_STREAM</b></dt>
<dt>32768 (0x8000)</dt>
</dl>
</td>
<td width="60%">
A file or directory that is configured with integrity. For a file, all data streams in the file have 
         integrity. For a directory, integrity is the default for newly created files and subdirectories, unless the 
         caller specifies otherwise.

This flag is only supported on the ReFS file system.

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

For more information, see the **Caching Behavior** section of this 
         topic.

</td>
</tr>
</table>

### -field dwFileFlags

This parameter can contain combinations of flags (<b>FILE_FLAG_*</b>) for control of file 
       or device caching behavior, access modes, and other special-purpose flags.

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
         <a href="/windows/desktop/api/fileapi/nf-fileapi-createfile2">CreateFile2</a> using the 
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
         occur; <a href="/windows/desktop/api/fileapi/nf-fileapi-createfile2">CreateFile2</a> will attempt to open the reparse 
         point. When a file is opened, a file handle is returned, whether or not the filter that controls the reparse 
         point is operational.

This flag cannot be used with the <b>CREATE_ALWAYS</b> flag.

If the file is not a reparse point, then this flag is ignored.

For more information, see the Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_FLAG_OPEN_REQUIRING_OPLOCK"></a><a id="file_flag_open_requiring_oplock"></a><dl>
<dt><b>FILE_FLAG_OPEN_REQUIRING_OPLOCK</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
The file is being opened and an opportunistic lock (oplock) on the file is being requested as a single 
         atomic operation. The file system checks for oplocks before it performs the create operation, and will fail 
         the create with a last error code of <b>ERROR_CANNOT_BREAK_OPLOCK</b> if the result would 
         be to break an existing oplock.

If you use this flag  and your call to the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfile2">CreateFile2</a> function successfully returns, the first operation you should perform on the file handle is to request an oplock by calling the <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIOControl</a> function and then pass in <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_request_oplock">FSCTL_REQUEST_OPLOCK</a> or one of the other <a href="/windows/desktop/FileIO/opportunistic-lock-operations">Opportunistic Lock Operations</a>.  If you perform other file system operations with the file handle before requesting an oplock, a deadlock might occur.<div class="alert"><b>Note</b>  You can safely call the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function on the file handle without first requesting an oplock.</div>
<div> </div>


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
         **Synchronous and Asynchronous I/O Handles**
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

For more information, see the **Caching Behavior** section of this 
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

This flag should not be used if read-behind (that is, backwards scans) will be used.

This flag has no effect if the file system does not support cached I/O and 
         <b>FILE_FLAG_NO_BUFFERING</b>.

For more information, see the **Caching Behavior** section of this 
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

For additional information, see the **Caching Behavior** section of this 
         topic.

</td>
</tr>
</table>

### -field dwSecurityQosFlags

The <i>dwSecurityQosFlags</i> parameter specifies SQOS information. For more 
       information, see 
       <a href="/windows/desktop/SecAuthZ/impersonation-levels">Impersonation Levels</a>.

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
         specified.

</td>
</tr>
</table>

### -field lpSecurityAttributes

A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)">SECURITY_ATTRIBUTES</a> 
       structure that contains two separate but related data members: an optional security descriptor, and a Boolean 
       value that determines whether the returned handle can be inherited by child processes.

This parameter can be <b>NULL</b>.

If this parameter is <b>NULL</b>, the handle returned by 
       <a href="/windows/desktop/api/fileapi/nf-fileapi-createfile2">CreateFile2</a> cannot be inherited by any child processes the 
       application may create and the file or device associated with the returned handle gets a default security 
       descriptor.

The <b>lpSecurityDescriptor</b> member of the structure specifies a 
       <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> for a file or device. If 
       this member is <b>NULL</b>, the file or device associated with the returned handle is 
       assigned a default security descriptor.


<a href="/windows/desktop/api/fileapi/nf-fileapi-createfile2">CreateFile2</a> ignores the 
       <b>lpSecurityDescriptor</b> member when opening an existing file or device, but continues 
       to use the <b>bInheritHandle</b> member.

The <b>bInheritHandle</b> member of the structure specifies whether the returned handle 
       can be inherited.

For more information, see the Remarks section of the 
       <a href="/windows/desktop/api/fileapi/nf-fileapi-createfile2">CreateFile2</a> topic.

### -field hTemplateFile

A valid handle to a template file with the <b>GENERIC_READ</b> access right. The template 
       file supplies file attributes and extended attributes for the file that is being created.

This parameter can be <b>NULL</b>.

When opening an existing file, <a href="/windows/desktop/api/fileapi/nf-fileapi-createfile2">CreateFile2</a> ignores this 
       parameter.

When opening a new encrypted file, the file inherits the discretionary access control list from its parent 
       directory. For additional information, see 
       <a href="/windows/desktop/FileIO/file-encryption">File Encryption</a>.

## -remarks

To compile an application that uses the 
    <b>CREATEFILE2_EXTENDED_PARAMETERS</b> structure, 
    define the <b>_WIN32_WINNT</b> macro as 0x0602 or later. For more information, see 
    <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

<h3><a id="caching_behavior"></a><a id="CACHING_BEHAVIOR"></a>Caching Behavior</h3>
Several of the possible values for the <b>dwFileFlags</b> member are used to control or 
      affect how the data associated with the handle is cached by the system. They are:

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

<h3><a id="synchronous_and_asynchronous_i_o_handles"></a><a id="SYNCHRONOUS_AND_ASYNCHRONOUS_I_O_HANDLES"></a>Synchronous and Asynchronous I/O Handles</h3>

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfile2">CreateFile2</a> provides for creating a file or device handle 
      that is either synchronous or asynchronous. A synchronous handle behaves such that I/O function calls using that 
      handle are blocked until they complete, while an asynchronous file handle makes it possible for the system to 
      return immediately from I/O function calls, whether they completed the I/O operation or not. As stated 
      previously, this synchronous versus asynchronous behavior is determined by specifying 
      <b>FILE_FLAG_OVERLAPPED</b> within the <b>dwFileFlags</b> member of the 
      <b>CREATEFILE2_EXTENDED_PARAMETERS</b> 
      structure passed in the <i>pCreateExParams</i> parameter. There are several complexities and 
      potential pitfalls when using asynchronous I/O; for more information, see 
      <a href="/windows/desktop/FileIO/synchronous-and-asynchronous-i-o">Synchronous and Asynchronous I/O</a>.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfile2">CreateFile2</a>



<a href="/windows/desktop/FileIO/file-management-structures">File Management Structures</a>