---
UID: NF:fileapi.CreateFile2
title: CreateFile2 function (fileapi.h)
description: Creates or opens a file or I/O device.
helpviewer_keywords: ["0","CREATE_ALWAYS","CREATE_NEW","CreateFile2","CreateFile2 function [Files]","FILE_SHARE_DELETE","FILE_SHARE_READ","FILE_SHARE_WRITE","OPEN_ALWAYS","OPEN_EXISTING","TRUNCATE_EXISTING","fileapi/CreateFile2","fs.createfile2"]
old-location: fs\createfile2.htm
tech.root: fs
ms.assetid: cd7a81f3-60ee-443a-99f3-a4c8afd365e7
ms.date: 12/05/2018
ms.keywords: 0, CREATE_ALWAYS, CREATE_NEW, CreateFile2, CreateFile2 function [Files], FILE_SHARE_DELETE, FILE_SHARE_READ, FILE_SHARE_WRITE, OPEN_ALWAYS, OPEN_EXISTING, TRUNCATE_EXISTING, fileapi/CreateFile2, fs.createfile2
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateFile2
 - fileapi/CreateFile2
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
 - API-MS-Win-Core-File-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - MinKernelBase.dll
api_name:
 - CreateFile2
---

# CreateFile2 function


## -description

Creates or opens a file or I/O device. The most commonly used I/O devices are as follows: file, file stream, 
    directory, physical disk, volume, console buffer, tape drive, communications resource, mailslot, and pipe. The 
    function returns a handle that can be used to access the file or device for various types of I/O depending on the 
    file or device and the flags and attributes specified.

When called from a Windows Store app, <b>CreateFile2</b> 
    is simplified. You can open only files or directories inside the 
    <a href="/uwp/api/windows.storage.applicationdata.localfolder">ApplicationData.LocalFolder</a> or 
    <a href="/uwp/api/windows.applicationmodel.package.installedlocation">Package.InstalledLocation</a> 
    directories. You can't open named pipes or mailslots or create encrypted files 
    (<b>FILE_ATTRIBUTE_ENCRYPTED</b>).
<div class="alert"><b>Note</b>  We refer here to the app's local folder and the package's installed location, not additional packages in the package graph, like resource packages. <b>CreateFile2</b> doesn't support opening files in additional packages in the package graph. For example, suppose an app has a dependency on <a href="/previous-versions/windows/br212652(v=win.10)">WinJS</a>. The app can call <b>CreateFile2</b> to open a file in its package but not in the <b>WinJS</b> package.</div><div> </div>To perform this operation as a transacted operation, which results in a handle that can be used for transacted 
    I/O, use the <a href="/windows/desktop/api/winbase/nf-winbase-createfiletransacteda">CreateFileTransacted</a> function.

## -parameters

### -param lpFileName [in]

The name of the file or device to be created or opened.

For information on special device names, see 
       <a href="/windows/desktop/FileIO/defining-an-ms-dos-device-name">Defining an MS-DOS Device Name</a>.

To create a file stream, specify the name of the file, a colon, and then the name of the stream. For more 
       information, see <a href="/windows/desktop/FileIO/file-streams">File Streams</a>.

<div class="alert"><b>Tip</b>  Starting with Windows 10, version 1607, you can opt-in to remove the <b>MAX_PATH</b> limitation without prepending "\\?\". See the "Maximum Path Length Limitation" section of <a href="/windows/desktop/FileIO/naming-a-file">Naming Files, Paths, and Namespaces</a> for details.</div>
<div> </div>

### -param dwDesiredAccess [in]

The requested access to the file or device, which can be summarized as read, write, both or neither zero).

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

If this parameter is zero and <b>CreateFile2</b> succeeds, the 
       file or device cannot be shared and cannot be opened again until the handle to the file or device is closed. 
       For more information, see the Remarks section.

You cannot request a sharing mode that conflicts with the access mode that is specified in an existing 
       request that has an open handle. <b>CreateFile2</b> would fail 
       and the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function would return 
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
         Exclusive access to a file or directory is only granted if the application has write access to the file.

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

If a file or directory is being opened and this flag is not specified, and the caller does not have write 
         access to the file or directory, the function fails.

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

### -param pCreateExParams [in, optional]

Pointer to an optional 
      <a href="/windows/desktop/api/fileapi/ns-fileapi-createfile2_extended_parameters">CREATEFILE2_EXTENDED_PARAMETERS</a> 
      structure.

## -returns

If the function succeeds, the return value is an open handle to the specified file, device, named pipe, or 
       mail slot.

If the function fails, the return value is <b>INVALID_HANDLE_VALUE</b>. To get extended 
       error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To compile an application that uses the <b>CreateFile2</b> 
    function, define the <b>_WIN32_WINNT</b> macro as 0x0602 or later. For more information, see 
    <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

<b>CreateFile2</b> supports file interaction and most other 
    types of I/O devices and mechanisms available to Windows developers. This section attempts to cover the varied 
    issues developers may experience when using <b>CreateFile2</b> in 
    different contexts and with different I/O types. The text attempts to use the word <i>file</i> 
    only when referring specifically to data stored in an actual file on a file system. However, some uses of 
    <i>file</i> may be referring more generally to an I/O object that supports file-like mechanisms. 
    This liberal use of the term <i>file</i> is particularly prevalent in constant names and 
    parameter names because of the previously mentioned historical reasons.

When an application is finished using the object handle returned by 
    <b>CreateFile2</b>, use the 
    <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to close the handle. This not only 
    frees up system resources, but can have wider influence on things like sharing the file or device and committing 
    data to disk. Specifics are noted within this topic as appropriate.

Some file systems, such as the NTFS file system, support compression or encryption for individual files and 
     directories. On volumes that have a mounted file system with this support, a new file inherits the compression 
     and encryption attributes of its directory.

You cannot use <b>CreateFile2</b> to control compression, 
     decompression, or decryption on a file or directory. For more information, see 
     <a href="/windows/desktop/FileIO/creating-and-opening-files">Creating and Opening Files</a>, 
     <a href="/windows/desktop/FileIO/file-compression-and-decompression">File Compression and Decompression</a>, 
     and <a href="/windows/desktop/FileIO/file-encryption">File Encryption</a>.

If the <b>lpSecurityAttributes</b> member of the 
     <a href="/windows/desktop/api/fileapi/ns-fileapi-createfile2_extended_parameters">CREATEFILE2_EXTENDED_PARAMETERS</a> structure 
     passed in the <i>pCreateExParams</i> parameter is <b>NULL</b>, the handle 
     returned by <b>CreateFile2</b> cannot be inherited by any child 
     processes your application may create. The following information regarding this member also applies:

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
 

<h3><a id="Symbolic_Link_Behavior"></a><a id="symbolic_link_behavior"></a><a id="SYMBOLIC_LINK_BEHAVIOR"></a>Symbolic Link Behavior</h3>
If the call to this function creates a file, there is no change in behavior. Also, consider the following 
      information regarding <b>FILE_FLAG_OPEN_REPARSE_POINT</b> flag for the 
      <b>dwFileFlags</b> member of the 
      <a href="/windows/desktop/api/fileapi/ns-fileapi-createfile2_extended_parameters">CREATEFILE2_EXTENDED_PARAMETERS</a> 
      structure passed in the <i>pCreateExParams</i> parameter:

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
<h3><a id="Files"></a><a id="files"></a><a id="FILES"></a>Files</h3>
If you rename or delete a file and then restore it shortly afterward, the system searches the cache for file 
      information to restore. Cached information includes its short/long name pair and creation time.

If you call <b>CreateFile2</b> on a file that is pending deletion 
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

When an application creates a file across a network, it is better to use 
      <code>GENERIC_READ | GENERIC_WRITE</code> for 
      <i>dwDesiredAccess</i> than to use <b>GENERIC_WRITE</b> alone. The 
      resulting code is faster, because the redirector can use the cache manager and send fewer SMBs with more data. 
      This combination also avoids an issue where writing to a file across a network can occasionally return 
      <b>ERROR_ACCESS_DENIED</b>.

For more information, see 
      <a href="/windows/desktop/FileIO/creating-and-opening-files">Creating and Opening Files</a>.

<h3><a id="File_Streams"></a><a id="file_streams"></a><a id="FILE_STREAMS"></a>File Streams</h3>
On NTFS file systems, you can use <b>CreateFile2</b> to create 
      separate streams within a file. For more information, see 
      <a href="/windows/desktop/FileIO/file-streams">File Streams</a>.

<h3><a id="Directories"></a><a id="directories"></a><a id="DIRECTORIES"></a>Directories</h3>
An application cannot create a directory by using 
      <b>CreateFile2</b>, therefore only the 
      <b>OPEN_EXISTING</b> value is valid for 
      <i>dwCreationDisposition</i> for this use case. To create a directory, the application must 
      call <a href="/windows/desktop/api/fileapi/nf-fileapi-createdirectorya">CreateDirectory</a> or 
      <a href="/windows/desktop/api/winbase/nf-winbase-createdirectoryexa">CreateDirectoryEx</a>.

To open a directory using <b>CreateFile2</b>, specify the 
      <b>FILE_FLAG_BACKUP_SEMANTICS</b> flag as part of <b>dwFileFlags</b> 
      member of the 
      <a href="/windows/desktop/api/fileapi/ns-fileapi-createfile2_extended_parameters">CREATEFILE2_EXTENDED_PARAMETERS</a> 
      structure passed in the <i>pCreateExParams</i> parameter. Appropriate security checks still 
      apply when this flag is used without <b>SE_BACKUP_NAME</b> and 
      <b>SE_RESTORE_NAME</b> privileges.

When using <b>CreateFile2</b> to open a directory during 
      defragmentation of a FAT or FAT32 file system volume, do not specify the 
      <b>MAXIMUM_ALLOWED</b> access right. Access to the directory is denied if this is done. 
      Specify the <b>GENERIC_READ</b> access right instead.

For more information, see 
      <a href="/windows/desktop/FileIO/about-directory-management">About Directory Management</a>.

<h3><a id="Physical_Disks_and_Volumes"></a><a id="physical_disks_and_volumes"></a><a id="PHYSICAL_DISKS_AND_VOLUMES"></a>Physical Disks and Volumes</h3>
Direct access to the disk or to a volume is restricted.

You can use the <b>CreateFile2</b> function to open a physical 
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
      <b>CreateFile2</b>. You should assume that all Microsoft file 
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
      "\\\\.\\Changer0".

<h3><a id="Tape_Drives"></a><a id="tape_drives"></a><a id="TAPE_DRIVES"></a>Tape Drives</h3>
You can open tape drives by using a file name of the following form: 
      "\\.\TAPE<i>x</i>" where 
      <i>x</i> is a number that indicates which drive to open, starting with tape drive zero. To 
      open tape drive zero in an application that is written in C or C++, use the following file name: 
      "\\\\.\\TAPE0".

For more information, see <a href="/windows/desktop/Backup/backup">Backup</a>.

<h3><a id="Communications_Resources"></a><a id="communications_resources"></a><a id="COMMUNICATIONS_RESOURCES"></a>Communications Resources</h3>
The <b>CreateFile2</b> function can create a handle to a 
      communications resource, such as the serial port COM1. For communications resources, 
      the <i>dwCreationDisposition</i> parameter must be 
      <b>OPEN_EXISTING</b>, the <i>dwShareMode</i> parameter must be zero 
      (exclusive access), and the <i>hTemplateFile</i> parameter must be 
      <b>NULL</b>. Read, write, or read/write access can be specified, and the handle can be opened 
      for overlapped I/O.

To specify a COM port number greater than 9, use the following syntax: 
      "\\.\COM10". This syntax works for all port numbers and hardware that 
      allows COM port numbers to be specified.

For more information about communications, see 
      <a href="/windows/desktop/DevIO/communications-resources">Communications</a>.

<h3><a id="Consoles"></a><a id="consoles"></a><a id="CONSOLES"></a>Consoles</h3>
The <b>CreateFile2</b> function can create a handle to console 
      input (CONIN$). If the process has an open handle to it as a result of inheritance or 
      duplication, it can also create a handle to the active screen buffer (CONOUT$). The 
      calling process must be attached to an inherited console or one allocated by the 
      <a href="/windows/console/allocconsole">AllocConsole</a> function. For console handles, set the 
      <b>CreateFile2</b> parameters as follows.

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
<i>dwCreationDisposition</i>

</td>
<td>
You should specify <b>OPEN_EXISTING</b> when using 
         <b>CreateFile2</b> to open the console.

</td>
</tr>
</table>
 

Set the members of the 
      <a href="/windows/desktop/api/fileapi/ns-fileapi-createfile2_extended_parameters">CREATEFILE2_EXTENDED_PARAMETERS</a> 
      structure passed in the <i>pCreateExParams</i> parameter as follows.

<table>
<tr>
<th>Members</th>
<th>Value</th>
</tr>
<tr>
<td>
<b>lpSecurityAttributes</b>

</td>
<td>
If you want the console to be inherited, the <b>bInheritHandle</b> member of the 
         <a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure 
         must be <b>TRUE</b>.

</td>
</tr>
<tr>
<td>
<b>dwFileAttributes</b>

<b>dwFileFlags</b>

<b>dwSecurityQosFlags</b>

<b>hTemplateFile</b>

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
<td>Causes <b>CreateFile2</b> to fail; 
        <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns 
        <b>ERROR_FILE_NOT_FOUND</b>.</td>
</tr>
</table>
 

<h3><a id="Mailslots"></a><a id="mailslots"></a><a id="MAILSLOTS"></a>Mailslots</h3>
If <b>CreateFile2</b> opens the client end of a mailslot, the 
      function returns <b>INVALID_HANDLE_VALUE</b> if the mailslot client attempts to open a local 
      mailslot before the mailslot server has created it with the 
      <a href="/windows/desktop/api/winbase/nf-winbase-createmailslota">CreateMailSlot</a> function.

For more information, see <a href="/windows/desktop/ipc/mailslots">Mailslots</a>.

<h3><a id="Pipes"></a><a id="pipes"></a><a id="PIPES"></a>Pipes</h3>
If <b>CreateFile2</b> opens the client end of a named pipe, the 
      function uses any instance of the named pipe that is in the listening state. The opening process can duplicate 
      the handle as many times as required, but after it is opened, the named pipe instance cannot be opened by 
      another client. The access that is specified when a pipe is opened must be compatible with the access that is 
      specified in the <i>dwOpenMode</i> parameter of the 
      <a href="/windows/desktop/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a> function.

If the <a href="/windows/desktop/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a> function was not 
      successfully called on the server prior to this operation, a pipe will not exist and 
      <b>CreateFile2</b> will fail with 
      <b>ERROR_FILE_NOT_FOUND</b>.

If there is at least one active pipe instance but there are no available listener pipes on the server, which 
      means all pipe instances are currently connected, 
     <b>CreateFile2</b> fails with 
     <b>ERROR_PIPE_BUSY</b>.

For more information, see <a href="/windows/desktop/ipc/pipes">Pipes</a>.

## -see-also

<a href="/windows/desktop/FileIO/about-directory-management">About Directory Management</a>



<a href="/windows/desktop/FileIO/about-volume-management">About Volume Management</a>



<a href="/windows/desktop/Backup/backup">Backup</a>



<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/DevIO/communications-resources">Communications</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createdirectorya">CreateDirectory</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createdirectoryexa">CreateDirectoryEx</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



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