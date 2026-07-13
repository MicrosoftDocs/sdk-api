---
UID: NF:fileapi.SetFileAttributesW
title: SetFileAttributesW function (fileapi.h)
description: Sets the attributes for a file or directory. (Unicode)
helpviewer_keywords: ["FILE_ATTRIBUTE_ARCHIVE", "FILE_ATTRIBUTE_COMPRESSED", "FILE_ATTRIBUTE_DEVICE", "FILE_ATTRIBUTE_DIRECTORY", "FILE_ATTRIBUTE_ENCRYPTED", "FILE_ATTRIBUTE_HIDDEN", "FILE_ATTRIBUTE_NORMAL", "FILE_ATTRIBUTE_NOT_CONTENT_INDEXED", "FILE_ATTRIBUTE_OFFLINE", "FILE_ATTRIBUTE_READONLY", "FILE_ATTRIBUTE_REPARSE_POINT", "FILE_ATTRIBUTE_SPARSE_FILE", "FILE_ATTRIBUTE_SYSTEM", "FILE_ATTRIBUTE_TEMPORARY", "SetFileAttributes", "SetFileAttributes function [Files]", "SetFileAttributesW", "_win32_setfileattributes", "base.setfileattributes", "fileapi/SetFileAttributes", "fileapi/SetFileAttributesW", "fs.setfileattributes"]
old-location: fs\setfileattributes.htm
tech.root: fs
ms.assetid: 3d5400c3-555f-44fc-9470-52a36d04d90b
ms.date: 12/05/2018
ms.keywords: FILE_ATTRIBUTE_ARCHIVE, FILE_ATTRIBUTE_COMPRESSED, FILE_ATTRIBUTE_DEVICE, FILE_ATTRIBUTE_DIRECTORY, FILE_ATTRIBUTE_ENCRYPTED, FILE_ATTRIBUTE_HIDDEN, FILE_ATTRIBUTE_NORMAL, FILE_ATTRIBUTE_NOT_CONTENT_INDEXED, FILE_ATTRIBUTE_OFFLINE, FILE_ATTRIBUTE_READONLY, FILE_ATTRIBUTE_REPARSE_POINT, FILE_ATTRIBUTE_SPARSE_FILE, FILE_ATTRIBUTE_SYSTEM, FILE_ATTRIBUTE_TEMPORARY, SetFileAttributes, SetFileAttributes function [Files], SetFileAttributesA, SetFileAttributesW, _win32_setfileattributes, base.setfileattributes, fileapi/SetFileAttributes, fileapi/SetFileAttributesA, fileapi/SetFileAttributesW, fs.setfileattributes, winbase/SetFileAttributes, winbase/SetFileAttributesA, winbase/SetFileAttributesW
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetFileAttributesW (Unicode) and SetFileAttributesA (ANSI)
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
 - SetFileAttributesW
 - fileapi/SetFileAttributesW
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
 - SetFileAttributes
 - SetFileAttributesA
 - SetFileAttributesW
---

# SetFileAttributesW function


## -description

Sets the attributes for a file or directory.

To perform this operation as a transacted operation, use the 
    <a href="/windows/desktop/api/winbase/nf-winbase-setfileattributestransacteda">SetFileAttributesTransacted</a> function.

## -parameters

### -param lpFileName [in]

The name of the file whose attributes are to be set.
      
By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

### -param dwFileAttributes [in]

The file attributes to set for the file.

This parameter can be one or more values, combined using the bitwise-OR operator. However, all other values 
       override <b>FILE_ATTRIBUTE_NORMAL</b>.

Not all attributes are supported by this function. For more information, see the Remarks section.

The following is a list of supported attribute values.

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
        mark files for backup or removal.

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
        attribute is not honored on directories. For more information, see "You cannot view or change the Read-only or 
        the System attributes of folders in Windows Server 2003, in Windows XP, or in 
        Windows Vista.

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
</table>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The following table describes how to set the attributes that cannot be set using 
    <b>SetFileAttributes</b>. For a complete list of all file 
    attribute values and their descriptions, see 
    <a href="/windows/desktop/FileIO/file-attribute-constants">File Attribute Constants</a>.

<table>
<tr>
<th>Attribute</th>
<th>How to Set</th>
</tr>
<tr>
<td>
<b>FILE_ATTRIBUTE_COMPRESSED</b>

0x800

</td>
<td>
To set a file's compression state, use the 
       <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the 
       <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_set_compression">FSCTL_SET_COMPRESSION</a> operation.

</td>
</tr>
<tr>
<td>
<b>FILE_ATTRIBUTE_DEVICE</b>

0x40

</td>
<td>
Reserved; do not use.

</td>
</tr>
<tr>
<td>
<b>FILE_ATTRIBUTE_DIRECTORY</b>

0x10

</td>
<td>
Files cannot be converted into directories. To create a directory, use the 
       <a href="/windows/desktop/api/fileapi/nf-fileapi-createdirectorya">CreateDirectory</a> or 
       <a href="/windows/desktop/api/winbase/nf-winbase-createdirectoryexa">CreateDirectoryEx</a> function.

</td>
</tr>
<tr>
<td>
<b>FILE_ATTRIBUTE_ENCRYPTED</b>

0x4000

</td>
<td>
To create an encrypted file, use the 
       <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function with the 
       <b>FILE_ATTRIBUTE_ENCRYPTED</b> attribute. To convert an existing file into an encrypted 
       file, use the <a href="/windows/desktop/api/winbase/nf-winbase-encryptfilea">EncryptFile</a> function.

</td>
</tr>
<tr>
<td>
<b>FILE_ATTRIBUTE_REPARSE_POINT</b>

0x400

</td>
<td>
To associate a reparse point with a file or directory, use the 
       <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the 
       <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_set_reparse_point">FSCTL_SET_REPARSE_POINT</a> operation.

</td>
</tr>
<tr>
<td>
<b>FILE_ATTRIBUTE_SPARSE_FILE</b>

0x200

</td>
<td>
To set a file's sparse attribute, use the 
       <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the 
       <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_set_sparse">FSCTL_SET_SPARSE</a> operation.

</td>
</tr>
</table>
 

<h3><a id="Transacted_Operations"></a><a id="transacted_operations"></a><a id="TRANSACTED_OPERATIONS"></a>Transacted Operations</h3>
If a file is open for modification in a transaction, no other thread can open the file for modification until 
      the transaction is committed. So if a transacted thread opens the file first, any subsequent threads that try 
      modifying the file before the transaction is committed receives a sharing violation. If a non-transacted thread 
      modifies the file before the transacted thread does, and the file is still open when the transaction attempts to 
      open it, the transaction receives the error <b>ERROR_TRANSACTIONAL_CONFLICT</b>.

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
 


#### Examples

For an example, see 
     <a href="/windows/desktop/FileIO/retrieving-and-changing-file-attributes">Retrieving and Changing File Attributes</a>.

<div class="code"></div>




> [!NOTE]
> The fileapi.h header defines SetFileAttributes as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/FileIO/file-attribute-constants">File Attribute Constants</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa">GetFileAttributes</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setfileattributestransacteda">SetFileAttributesTransacted</a>



<a href="/windows/desktop/FileIO/symbolic-links">Symbolic Links</a>



<a href="/windows/desktop/FileIO/transactional-ntfs-portal">Transactional NTFS</a>
