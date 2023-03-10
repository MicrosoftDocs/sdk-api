---
UID: NS:winbase._FILE_ID_EXTD_DIR_INFO
title: FILE_ID_EXTD_DIR_INFO (winbase.h)
description: Contains identification information for a file. (FILE_ID_EXTD_DIR_INFO)
helpviewer_keywords: ["*PFILE_ID_EXTD_DIR_INFO","FILE_ATTRIBUTE_ARCHIVE","FILE_ATTRIBUTE_COMPRESSED","FILE_ATTRIBUTE_DEVICE","FILE_ATTRIBUTE_DIRECTORY","FILE_ATTRIBUTE_ENCRYPTED","FILE_ATTRIBUTE_HIDDEN","FILE_ATTRIBUTE_NORMAL","FILE_ATTRIBUTE_NOT_CONTENT_INDEXED","FILE_ATTRIBUTE_OFFLINE","FILE_ATTRIBUTE_READONLY","FILE_ATTRIBUTE_REPARSE_POINT","FILE_ATTRIBUTE_SPARSE_FILE","FILE_ATTRIBUTE_SYSTEM","FILE_ATTRIBUTE_TEMPORARY","FILE_ATTRIBUTE_VIRTUAL","FILE_ID_EXTD_DIR_INFO","FILE_ID_EXTD_DIR_INFO structure [Files]","IO_REPARSE_TAG_CSV","IO_REPARSE_TAG_DEDUP","IO_REPARSE_TAG_DFS","IO_REPARSE_TAG_DFSR","IO_REPARSE_TAG_HSM","IO_REPARSE_TAG_HSM2","IO_REPARSE_TAG_MOUNT_POINT","IO_REPARSE_TAG_NFS","IO_REPARSE_TAG_SIS","IO_REPARSE_TAG_SYMLINK","IO_REPARSE_TAG_WIM","PFILE_ID_EXTD_DIR_INFO","PFILE_ID_EXTD_DIR_INFO structure pointer [Files]","_FILE_ID_EXTD_DIR_INFO","fs.file_id_extd_dir_info","winbase/FILE_ID_EXTD_DIR_INFO","winbase/PFILE_ID_EXTD_DIR_INFO"]
old-location: fs\file_id_extd_dir_info.htm
tech.root: fs
ms.assetid: 68f222c4-beb6-4be1-a31a-c5fbebbf76f7
ms.date: 12/05/2018
ms.keywords: '*PFILE_ID_EXTD_DIR_INFO, FILE_ATTRIBUTE_ARCHIVE, FILE_ATTRIBUTE_COMPRESSED, FILE_ATTRIBUTE_DEVICE, FILE_ATTRIBUTE_DIRECTORY, FILE_ATTRIBUTE_ENCRYPTED, FILE_ATTRIBUTE_HIDDEN, FILE_ATTRIBUTE_NORMAL, FILE_ATTRIBUTE_NOT_CONTENT_INDEXED, FILE_ATTRIBUTE_OFFLINE, FILE_ATTRIBUTE_READONLY, FILE_ATTRIBUTE_REPARSE_POINT, FILE_ATTRIBUTE_SPARSE_FILE, FILE_ATTRIBUTE_SYSTEM, FILE_ATTRIBUTE_TEMPORARY, FILE_ATTRIBUTE_VIRTUAL, FILE_ID_EXTD_DIR_INFO, FILE_ID_EXTD_DIR_INFO structure [Files], IO_REPARSE_TAG_CSV, IO_REPARSE_TAG_DEDUP, IO_REPARSE_TAG_DFS, IO_REPARSE_TAG_DFSR, IO_REPARSE_TAG_HSM, IO_REPARSE_TAG_HSM2, IO_REPARSE_TAG_MOUNT_POINT, IO_REPARSE_TAG_NFS, IO_REPARSE_TAG_SIS, IO_REPARSE_TAG_SYMLINK, IO_REPARSE_TAG_WIM, PFILE_ID_EXTD_DIR_INFO, PFILE_ID_EXTD_DIR_INFO structure pointer [Files], _FILE_ID_EXTD_DIR_INFO, fs.file_id_extd_dir_info, winbase/FILE_ID_EXTD_DIR_INFO, winbase/PFILE_ID_EXTD_DIR_INFO'
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: FILE_ID_EXTD_DIR_INFO, *PFILE_ID_EXTD_DIR_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FILE_ID_EXTD_DIR_INFO
 - winbase/_FILE_ID_EXTD_DIR_INFO
 - PFILE_ID_EXTD_DIR_INFO
 - winbase/PFILE_ID_EXTD_DIR_INFO
 - FILE_ID_EXTD_DIR_INFO
 - winbase/FILE_ID_EXTD_DIR_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - FILE_ID_EXTD_DIR_INFO
---

# FILE_ID_EXTD_DIR_INFO structure


## -description

Contains identification information for a file. This structure is returned from the 
    <a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a> function when 
    <b>FileIdExtdDirectoryInfo</b> (0x13) or <b>FileIdExtdDirectoryRestartInfo</b> (0x14) 
    is passed in the <i>FileInformationClass</i> parameter.

## -struct-fields

### -field NextEntryOffset

The offset for the next <b>FILE_ID_EXTD_DIR_INFO</b> 
      structure that is returned. Contains zero (0) if no other entries follow this one.

### -field FileIndex

The byte offset of the file within the parent directory. This member is undefined for file systems, such as 
      NTFS, in which the position of a file within the parent directory is not fixed and can be changed at any time to 
      maintain sort order.

### -field CreationTime

The time that the file was created.

### -field LastAccessTime

The time that the file was last accessed.

### -field LastWriteTime

The time that the file was last written to.

### -field ChangeTime

The time that the file was last changed.

### -field EndOfFile

The absolute new end-of-file position as a byte offset from the start of the file to the end of the file. 
      Because this value is zero-based, it actually refers to the first free byte in the file. In other words, 
      <b>EndOfFile</b> is the offset to the byte that immediately follows the last valid byte in 
      the file.

### -field AllocationSize

The number of bytes that are allocated for the file. This value is usually a multiple of the sector or 
      cluster size of the underlying physical device.

### -field FileAttributes

The file attributes. This member can be any valid combination of the following attributes:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_ATTRIBUTE_ARCHIVE"></a><a id="file_attribute_archive"></a><dl>
<dt><b>FILE_ATTRIBUTE_ARCHIVE</b></dt>
<dt>32 (0x20)</dt>
</dl>
</td>
<td width="60%">
A file or directory that is an archive file or directory. Applications typically use this attribute to 
        mark files for backup or removal . 

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ATTRIBUTE_COMPRESSED"></a><a id="file_attribute_compressed"></a><dl>
<dt><b>FILE_ATTRIBUTE_COMPRESSED</b></dt>
<dt>2048 (0x800)</dt>
</dl>
</td>
<td width="60%">
A file or directory that is compressed. For a file, all of the data in the file is compressed. For a 
        directory, compression is the default for newly created files and subdirectories.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ATTRIBUTE_DEVICE"></a><a id="file_attribute_device"></a><dl>
<dt><b>FILE_ATTRIBUTE_DEVICE</b></dt>
<dt>64 (0x40)</dt>
</dl>
</td>
<td width="60%">
This value is reserved for system use.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ATTRIBUTE_DIRECTORY"></a><a id="file_attribute_directory"></a><dl>
<dt><b>FILE_ATTRIBUTE_DIRECTORY</b></dt>
<dt>16 (0x10)</dt>
</dl>
</td>
<td width="60%">
The handle that identifies a directory.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ATTRIBUTE_ENCRYPTED"></a><a id="file_attribute_encrypted"></a><dl>
<dt><b>FILE_ATTRIBUTE_ENCRYPTED</b></dt>
<dt>16384 (0x4000)</dt>
</dl>
</td>
<td width="60%">
A file or directory that is encrypted. For a file, all data streams in the file are encrypted. For a 
        directory, encryption is the default for newly created files and subdirectories.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ATTRIBUTE_HIDDEN"></a><a id="file_attribute_hidden"></a><dl>
<dt><b>FILE_ATTRIBUTE_HIDDEN</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
The file or directory is hidden. It is not included in an ordinary directory listing.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ATTRIBUTE_NORMAL"></a><a id="file_attribute_normal"></a><dl>
<dt><b>FILE_ATTRIBUTE_NORMAL</b></dt>
<dt>128 (0x80)</dt>
</dl>
</td>
<td width="60%">
A file that does not have other attributes set. This attribute is valid only when used alone.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ATTRIBUTE_NOT_CONTENT_INDEXED"></a><a id="file_attribute_not_content_indexed"></a><dl>
<dt><b>FILE_ATTRIBUTE_NOT_CONTENT_INDEXED</b></dt>
<dt>8192 (0x2000)</dt>
</dl>
</td>
<td width="60%">
The file or directory is not to be indexed by the content indexing service.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ATTRIBUTE_OFFLINE"></a><a id="file_attribute_offline"></a><dl>
<dt><b>FILE_ATTRIBUTE_OFFLINE</b></dt>
<dt>4096 (0x1000)</dt>
</dl>
</td>
<td width="60%">
The data of a file is not available immediately. This attribute indicates that the file data is 
        physically moved to offline storage. This attribute is used by Remote Storage, which is the hierarchical 
        storage management software. Applications should not arbitrarily change this attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ATTRIBUTE_READONLY"></a><a id="file_attribute_readonly"></a><dl>
<dt><b>FILE_ATTRIBUTE_READONLY</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
A file that is read-only. Applications can read the file, but cannot write to it or delete it. This 
        attribute is not honored on directories. For more information, see 
        <a href="https://support.microsoft.com/kb/326549">You cannot view or change the Read-only or the System attributes of folders in Windows Server 2003, in Windows XP, in Windows Vista or in Windows 7</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ATTRIBUTE_REPARSE_POINT"></a><a id="file_attribute_reparse_point"></a><dl>
<dt><b>FILE_ATTRIBUTE_REPARSE_POINT</b></dt>
<dt>1024 (0x400)</dt>
</dl>
</td>
<td width="60%">
A file or directory that has an associated reparse point, or a file that is a symbolic link.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ATTRIBUTE_SPARSE_FILE"></a><a id="file_attribute_sparse_file"></a><dl>
<dt><b>FILE_ATTRIBUTE_SPARSE_FILE</b></dt>
<dt>512 (0x200)</dt>
</dl>
</td>
<td width="60%">
A file that is a sparse file.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ATTRIBUTE_SYSTEM"></a><a id="file_attribute_system"></a><dl>
<dt><b>FILE_ATTRIBUTE_SYSTEM</b></dt>
<dt>4 (0x4)</dt>
</dl>
</td>
<td width="60%">
A file or directory that the operating system uses a part of, or uses exclusively.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ATTRIBUTE_TEMPORARY"></a><a id="file_attribute_temporary"></a><dl>
<dt><b>FILE_ATTRIBUTE_TEMPORARY</b></dt>
<dt>256 (0x100)</dt>
</dl>
</td>
<td width="60%">
A file that is being used for temporary storage. File systems avoid writing data back to mass storage if 
        sufficient cache memory is available, because typically, an application deletes a temporary file after the 
        handle is closed. In that scenario, the system can entirely avoid writing the data. Otherwise, the data is 
        written after the handle is closed.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ATTRIBUTE_VIRTUAL"></a><a id="file_attribute_virtual"></a><dl>
<dt><b>FILE_ATTRIBUTE_VIRTUAL</b></dt>
<dt>65536 (0x10000)</dt>
</dl>
</td>
<td width="60%">
This value is reserved for system use.

</td>
</tr>
</table>

### -field FileNameLength

The length of the file name.

### -field EaSize

The size of the extended attributes for the file.

### -field ReparsePointTag

If the <b>FileAttributes</b> member includes the 
       <b>FILE_ATTRIBUTE_REPARSE_POINT</b> attribute, this member specifies the reparse point 
       tag.

Otherwise, this value is undefined and should not be used.

For more information see <a href="/windows/desktop/FileIO/reparse-point-tags">Reparse Point Tags</a>.



#### IO_REPARSE_TAG_CSV (0x80000009)



#### IO_REPARSE_TAG_DEDUP (0x80000013)



#### IO_REPARSE_TAG_DFS (0x8000000A)



#### IO_REPARSE_TAG_DFSR (0x80000012)



#### IO_REPARSE_TAG_HSM (0xC0000004)



#### IO_REPARSE_TAG_HSM2 (0x80000006)



#### IO_REPARSE_TAG_MOUNT_POINT (0xA0000003)



#### IO_REPARSE_TAG_NFS (0x80000014)



#### IO_REPARSE_TAG_SIS (0x80000007)



#### IO_REPARSE_TAG_SYMLINK (0xA000000C)



#### IO_REPARSE_TAG_WIM (0x80000008)

### -field FileId

The file ID.

### -field FileName

The first character of the file name string. This is followed in memory by the remainder of the 
      string.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-file_id_128">FILE_ID_128</a>



<a href="/windows/desktop/api/minwinbase/ne-minwinbase-file_info_by_handle_class">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="/windows/desktop/FileIO/file-management-structures">File Management Structures</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a>
