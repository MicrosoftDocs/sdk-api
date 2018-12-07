---
UID: NF:fileapi.SetFileAttributesA
title: SetFileAttributesA function
author: windows-sdk-content
description: Sets the attributes for a file or directory.
old-location: fs\setfileattributes.htm
tech.root: fileio
ms.assetid: 3d5400c3-555f-44fc-9470-52a36d04d90b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FILE_ATTRIBUTE_ARCHIVE, FILE_ATTRIBUTE_COMPRESSED, FILE_ATTRIBUTE_DEVICE, FILE_ATTRIBUTE_DIRECTORY, FILE_ATTRIBUTE_ENCRYPTED, FILE_ATTRIBUTE_HIDDEN, FILE_ATTRIBUTE_NORMAL, FILE_ATTRIBUTE_NOT_CONTENT_INDEXED, FILE_ATTRIBUTE_OFFLINE, FILE_ATTRIBUTE_READONLY, FILE_ATTRIBUTE_REPARSE_POINT, FILE_ATTRIBUTE_SPARSE_FILE, FILE_ATTRIBUTE_SYSTEM, FILE_ATTRIBUTE_TEMPORARY, SetFileAttributes, SetFileAttributes function [Files], SetFileAttributesA, SetFileAttributesW, _win32_setfileattributes, base.setfileattributes, fileapi/SetFileAttributes, fileapi/SetFileAttributesA, fileapi/SetFileAttributesW, fs.setfileattributes, winbase/SetFileAttributes, winbase/SetFileAttributesA, winbase/SetFileAttributesW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - SetFileAttributes
 - SetFileAttributesA
 - SetFileAttributesW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetFileAttributesA function


## -description


Sets the attributes for a file or directory.

To perform this operation as a transacted operation, use the 
    <a href="https://msdn.microsoft.com/e25e77b2-a6ad-4ce4-8589-d7ff6c4074f6">SetFileAttributesTransacted</a> function.


## -parameters




### -param lpFileName [in]

The name of the file whose attributes are to be set.
      

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function (<b>SetFileAttributesW</b>) and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">File Names, Paths, and Namespaces</a>.

<div class="alert"><b>Tip</b>  Starting in Windows 10, version 1607, for the unicode version of this function (<b>SetFileAttributesW</b>), you can opt-in to remove the <b>MAX_PATH</b> character limitation without prepending "\\?\". See the "Maximum Path Limitation" section of  <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a> for details. </div>
<div> </div>

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
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The following table describes how to set the attributes that cannot be set using 
    <b>SetFileAttributes</b>. For a complete list of all file 
    attribute values and their descriptions, see 
    <a href="https://msdn.microsoft.com/ed9a73d2-7fb6-4fb7-97f6-4dbf89e2f156">File Attribute Constants</a>.

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
       <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the 
       <a href="https://msdn.microsoft.com/e6fb29ed-f4f4-4507-8312-d771ffb00256">FSCTL_SET_COMPRESSION</a> operation.

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
       <a href="https://msdn.microsoft.com/f8ca8b10-c8bd-4285-8a40-dbec4c24729c">CreateDirectory</a> or 
       <a href="https://msdn.microsoft.com/287996f8-e8ca-4b72-a5f6-016754785c5c">CreateDirectoryEx</a> function.

</td>
</tr>
<tr>
<td>
<b>FILE_ATTRIBUTE_ENCRYPTED</b>

0x4000

</td>
<td>
To create an encrypted file, use the 
       <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function with the 
       <b>FILE_ATTRIBUTE_ENCRYPTED</b> attribute. To convert an existing file into an encrypted 
       file, use the <a href="https://msdn.microsoft.com/7620e9fa-74d6-4b41-93db-4a562be63202">EncryptFile</a> function.

</td>
</tr>
<tr>
<td>
<b>FILE_ATTRIBUTE_REPARSE_POINT</b>

0x400

</td>
<td>
To associate a reparse point with a file or directory, use the 
       <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the 
       <a href="https://msdn.microsoft.com/0bed6d69-269b-4921-8984-69c7829fb9ea">FSCTL_SET_REPARSE_POINT</a> operation.

</td>
</tr>
<tr>
<td>
<b>FILE_ATTRIBUTE_SPARSE_FILE</b>

0x200

</td>
<td>
To set a file's sparse attribute, use the 
       <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the 
       <a href="https://msdn.microsoft.com/aa8f5880-f831-49b6-8359-fe07c78c032f">FSCTL_SET_SPARSE</a> operation.

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
     <a href="https://msdn.microsoft.com/f6eaea8a-0cc2-4fb6-bec5-7fb12b20c075">Retrieving and Changing File Attributes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/ed9a73d2-7fb6-4fb7-97f6-4dbf89e2f156">File Attribute Constants</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/9f9bcdbb-1ffd-49c2-92f4-181fdcc9c690">GetFileAttributes</a>



<a href="https://msdn.microsoft.com/e25e77b2-a6ad-4ce4-8589-d7ff6c4074f6">SetFileAttributesTransacted</a>



<a href="https://msdn.microsoft.com/d6bf5df7-bc12-4dec-b116-95d9109f5eb4">Symbolic Links</a>



<a href="https://msdn.microsoft.com/e8c3ceed-d391-4934-b3f7-12c2123c8c23">Transactional NTFS</a>
 

 

