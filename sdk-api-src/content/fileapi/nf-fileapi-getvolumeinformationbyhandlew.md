---
UID: NF:fileapi.GetVolumeInformationByHandleW
title: GetVolumeInformationByHandleW function (fileapi.h)
description: Retrieves information about the file system and volume associated with the specified file.helpviewer_keywords: ["FILE_CASE_PRESERVED_NAMES","FILE_CASE_SENSITIVE_SEARCH","FILE_FILE_COMPRESSION","FILE_NAMED_STREAMS","FILE_PERSISTENT_ACLS","FILE_READ_ONLY_VOLUME","FILE_SEQUENTIAL_WRITE_ONCE","FILE_SUPPORTS_ENCRYPTION","FILE_SUPPORTS_EXTENDED_ATTRIBUTES","FILE_SUPPORTS_HARD_LINKS","FILE_SUPPORTS_OBJECT_IDS","FILE_SUPPORTS_OPEN_BY_FILE_ID","FILE_SUPPORTS_REPARSE_POINTS","FILE_SUPPORTS_SPARSE_FILES","FILE_SUPPORTS_TRANSACTIONS","FILE_SUPPORTS_USN_JOURNAL","FILE_UNICODE_ON_DISK","FILE_VOLUME_IS_COMPRESSED","FILE_VOLUME_QUOTAS","GetVolumeInformationByHandleW","GetVolumeInformationByHandleW function [Files]","fileapi/GetVolumeInformationByHandleW","fs.getvolumeinformationbyhandlew","winbase/GetVolumeInformationByHandleW"]
old-location: fs\getvolumeinformationbyhandlew.htm
tech.root: FileIO
ms.assetid: 09fab0a4-23fd-4bd9-b9f6-f0d1597ab609
ms.date: 12/05/2018
ms.keywords: FILE_CASE_PRESERVED_NAMES, FILE_CASE_SENSITIVE_SEARCH, FILE_FILE_COMPRESSION, FILE_NAMED_STREAMS, FILE_PERSISTENT_ACLS, FILE_READ_ONLY_VOLUME, FILE_SEQUENTIAL_WRITE_ONCE, FILE_SUPPORTS_ENCRYPTION, FILE_SUPPORTS_EXTENDED_ATTRIBUTES, FILE_SUPPORTS_HARD_LINKS, FILE_SUPPORTS_OBJECT_IDS, FILE_SUPPORTS_OPEN_BY_FILE_ID, FILE_SUPPORTS_REPARSE_POINTS, FILE_SUPPORTS_SPARSE_FILES, FILE_SUPPORTS_TRANSACTIONS, FILE_SUPPORTS_USN_JOURNAL, FILE_UNICODE_ON_DISK, FILE_VOLUME_IS_COMPRESSED, FILE_VOLUME_QUOTAS, GetVolumeInformationByHandleW, GetVolumeInformationByHandleW function [Files], fileapi/GetVolumeInformationByHandleW, fs.getvolumeinformationbyhandlew, winbase/GetVolumeInformationByHandleW
f1_keywords:
- fileapi/GetVolumeInformationByHandleW
dev_langs:
- c++
req.header: fileapi.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-File-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-File-l1-2-0.dll
- API-MS-Win-Core-File-l1-2-1.dll
- API-MS-Win-Core-File-l1-2-2.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
api_name:
- GetVolumeInformationByHandleW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetVolumeInformationByHandleW function


## -description


Retrieves information about the file system and volume associated with the specified 
    file.

To retrieve the current compression state of a file or directory, use 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_compression">FSCTL_GET_COMPRESSION</a>.


## -parameters




### -param hFile [in]

A handle to the file.


### -param lpVolumeNameBuffer [out, optional]

A pointer to a buffer that receives the name of a specified volume. The maximum buffer size is 
      <code>MAX_PATH+1</code>.


### -param nVolumeNameSize [in]

The length of a volume name buffer, in <b>WCHAR</b>s. The maximum buffer size is 
       <code>MAX_PATH+1</code>.

This parameter is ignored if the volume name buffer is not supplied.


### -param lpVolumeSerialNumber [out, optional]

A pointer to a variable that receives the volume serial number.

This parameter can be <b>NULL</b> if the serial number is not required.

This function returns the volume serial number that the operating system assigns when a hard disk is 
       formatted. To programmatically obtain the hard disk's serial number that the manufacturer assigns, use the 
       Windows Management Instrumentation (WMI) 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/cimwin32a/win32-physicalmedia">Win32_PhysicalMedia</a> property 
       <b>SerialNumber</b>.


### -param lpMaximumComponentLength [out, optional]

A pointer to a variable that receives the maximum length, in <b>WCHAR</b>s, of a file 
       name component  that a specified file system supports.

A file name component is the portion of a file name between backslashes.

The value that is stored in the variable  that  *<i>lpMaximumComponentLength</i> points to 
       is used to indicate that a specified file system supports long names. For example, for a FAT file system that 
       supports long names, the function stores the value 255, rather than the previous 8.3 indicator. Long names can 
       also be supported on systems that use the NTFS file system.


### -param lpFileSystemFlags [out, optional]

A pointer to a variable that receives flags associated with the specified file system.

This parameter can be one or more of the following flags. However, 
       <b>FILE_FILE_COMPRESSION</b> and <b>FILE_VOL_IS_COMPRESSED</b> are mutually 
       exclusive.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_CASE_PRESERVED_NAMES"></a><a id="file_case_preserved_names"></a><dl>
<dt><b>FILE_CASE_PRESERVED_NAMES</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The specified volume supports preserved case of file names when it places a name on disk.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_CASE_SENSITIVE_SEARCH"></a><a id="file_case_sensitive_search"></a><dl>
<dt><b>FILE_CASE_SENSITIVE_SEARCH</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The specified volume supports case-sensitive file names.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_FILE_COMPRESSION"></a><a id="file_file_compression"></a><dl>
<dt><b>FILE_FILE_COMPRESSION</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The specified volume supports file-based compression.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_NAMED_STREAMS"></a><a id="file_named_streams"></a><dl>
<dt><b>FILE_NAMED_STREAMS</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
The specified volume supports named streams.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_PERSISTENT_ACLS"></a><a id="file_persistent_acls"></a><dl>
<dt><b>FILE_PERSISTENT_ACLS</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The specified volume preserves and enforces access control lists (ACL). For example, the NTFS file system 
        preserves and enforces ACLs, and the FAT file system does not.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_READ_ONLY_VOLUME"></a><a id="file_read_only_volume"></a><dl>
<dt><b>FILE_READ_ONLY_VOLUME</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
The specified volume is read-only.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SEQUENTIAL_WRITE_ONCE"></a><a id="file_sequential_write_once"></a><dl>
<dt><b>FILE_SEQUENTIAL_WRITE_ONCE</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
The specified volume supports a single sequential write.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SUPPORTS_ENCRYPTION"></a><a id="file_supports_encryption"></a><dl>
<dt><b>FILE_SUPPORTS_ENCRYPTION</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
The specified volume supports the Encrypted File System (EFS). For more information, see 
        <a href="https://docs.microsoft.com/windows/desktop/FileIO/file-encryption">File Encryption</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SUPPORTS_EXTENDED_ATTRIBUTES"></a><a id="file_supports_extended_attributes"></a><dl>
<dt><b>FILE_SUPPORTS_EXTENDED_ATTRIBUTES</b></dt>
<dt>0x00800000</dt>
</dl>
</td>
<td width="60%">
The specified volume supports extended attributes. An extended attribute is a piece of 
        application-specific metadata that an application can associate with a file and is not part of the file's data.

<b>Windows Vista and Windows Server 2008:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SUPPORTS_HARD_LINKS"></a><a id="file_supports_hard_links"></a><dl>
<dt><b>FILE_SUPPORTS_HARD_LINKS</b></dt>
<dt>0x00400000</dt>
</dl>
</td>
<td width="60%">
The specified volume supports hard links. For more information, see 
        <a href="https://docs.microsoft.com/windows/desktop/FileIO/hard-links-and-junctions">Hard Links and Junctions</a>.

<b>Windows Vista and Windows Server 2008:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SUPPORTS_OBJECT_IDS"></a><a id="file_supports_object_ids"></a><dl>
<dt><b>FILE_SUPPORTS_OBJECT_IDS</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
The specified volume supports object identifiers.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SUPPORTS_OPEN_BY_FILE_ID"></a><a id="file_supports_open_by_file_id"></a><dl>
<dt><b>FILE_SUPPORTS_OPEN_BY_FILE_ID</b></dt>
<dt>0x01000000</dt>
</dl>
</td>
<td width="60%">
The file system supports open by FileID. For more information, see 
        <a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-file_id_both_dir_info">FILE_ID_BOTH_DIR_INFO</a>.

<b>Windows Vista and Windows Server 2008:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SUPPORTS_REPARSE_POINTS"></a><a id="file_supports_reparse_points"></a><dl>
<dt><b>FILE_SUPPORTS_REPARSE_POINTS</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
The specified volume supports re-parse points.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SUPPORTS_SPARSE_FILES"></a><a id="file_supports_sparse_files"></a><dl>
<dt><b>FILE_SUPPORTS_SPARSE_FILES</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
The specified volume supports sparse files.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SUPPORTS_TRANSACTIONS"></a><a id="file_supports_transactions"></a><dl>
<dt><b>FILE_SUPPORTS_TRANSACTIONS</b></dt>
<dt>0x00200000</dt>
</dl>
</td>
<td width="60%">
The specified volume supports transactions. For more information, see 
        <a href="https://docs.microsoft.com/windows/desktop/Ktm/about-ktm">About KTM</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SUPPORTS_USN_JOURNAL"></a><a id="file_supports_usn_journal"></a><dl>
<dt><b>FILE_SUPPORTS_USN_JOURNAL</b></dt>
<dt>0x02000000</dt>
</dl>
</td>
<td width="60%">
The specified volume supports update sequence number (USN) journals. For more information, see 
        <a href="https://docs.microsoft.com/windows/desktop/FileIO/change-journal-records">Change Journal Records</a>.

<b>Windows Vista and Windows Server 2008:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_UNICODE_ON_DISK"></a><a id="file_unicode_on_disk"></a><dl>
<dt><b>FILE_UNICODE_ON_DISK</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The specified volume supports Unicode in file names as they appear on disk.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_VOLUME_IS_COMPRESSED"></a><a id="file_volume_is_compressed"></a><dl>
<dt><b>FILE_VOLUME_IS_COMPRESSED</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
The specified volume is a compressed volume.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_VOLUME_QUOTAS"></a><a id="file_volume_quotas"></a><dl>
<dt><b>FILE_VOLUME_QUOTAS</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
The specified volume supports disk quotas.

</td>
</tr>
</table>
 


### -param lpFileSystemNameBuffer [out, optional]

A pointer to a buffer that receives the name of the file system, for example, the FAT file system or the 
      NTFS file system. The buffer size is specified by the <i>nFileSystemNameSize</i> 
      parameter.


### -param nFileSystemNameSize [in]

The length of the file system name buffer, in <b>WCHAR</b>s. The maximum buffer size 
       is <code>MAX_PATH+1</code>.

This parameter is ignored if the file system name buffer is not supplied.


## -returns



If all the requested information is retrieved, the return value is nonzero.

If not all the requested information is retrieved, the return value is zero. To get extended error 
       information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



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
 

SMB does not support volume management functions.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Ktm/about-ktm">About KTM</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/file-encryption">File Encryption</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea">GetCompressedFileSize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa">GetFileAttributes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa">GetVolumeInformation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode">SetErrorMode</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-setvolumelabela">SetVolumeLabel</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/volume-management-functions">Volume Management Functions</a>
 

 

