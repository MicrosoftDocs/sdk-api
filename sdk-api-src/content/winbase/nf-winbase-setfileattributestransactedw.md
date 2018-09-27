---
UID: NF:winbase.SetFileAttributesTransactedW
title: SetFileAttributesTransactedW function
author: windows-sdk-content
description: Sets the attributes for a file or directory as a transacted operation.
old-location: fs\setfileattributestransacted.htm
tech.root: fileio
ms.assetid: e25e77b2-a6ad-4ce4-8589-d7ff6c4074f6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FILE_ATTRIBUTE_ARCHIVE, FILE_ATTRIBUTE_HIDDEN, FILE_ATTRIBUTE_NORMAL, FILE_ATTRIBUTE_NOT_CONTENT_INDEXED, FILE_ATTRIBUTE_OFFLINE, FILE_ATTRIBUTE_READONLY, FILE_ATTRIBUTE_SYSTEM, FILE_ATTRIBUTE_TEMPORARY, SetFileAttributesTransacted, SetFileAttributesTransacted function [Files], SetFileAttributesTransactedA, SetFileAttributesTransactedW, fs.setfileattributestransacted, winbase/SetFileAttributesTransacted, winbase/SetFileAttributesTransactedA, winbase/SetFileAttributesTransactedW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetFileAttributesTransactedW (Unicode) and SetFileAttributesTransactedA (ANSI)
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
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - Kernel32Legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - SetFileAttributesTransacted
 - SetFileAttributesTransactedA
 - SetFileAttributesTransactedW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetFileAttributesTransactedW function


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://msdn.microsoft.com/9ee26e7e-990e-4cd3-8180-f0fcaac2b752">Alternatives to using Transactional NTFS</a>.]

Sets the attributes for a file or directory as a transacted operation.


## -parameters




### -param lpFileName [in]

The name of the file whose attributes are to be set.
      

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">File Names, Paths, and Namespaces</a>.

The file must reside on the local computer; otherwise, the function fails and the last error code is set to 
      <b>ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE</b>.


### -param dwFileAttributes [in]

The file attributes to set for the file.

For a list of file attribute value and their descriptions, see 
       <a href="https://msdn.microsoft.com/ed9a73d2-7fb6-4fb7-97f6-4dbf89e2f156">File Attribute Constants</a>. This parameter can be 
       one or more values, combined using the bitwise-OR operator. However, all other values override 
       <b>FILE_ATTRIBUTE_NORMAL</b>.

Not all attributes are supported by this function. For more information, see the Remarks section.

The following is a list of supported attribute values.



#### FILE_ATTRIBUTE_ARCHIVE (32 (0x20))



#### FILE_ATTRIBUTE_HIDDEN (2 (0x2))



#### FILE_ATTRIBUTE_NORMAL (128 (0x80))



#### FILE_ATTRIBUTE_NOT_CONTENT_INDEXED (8192 (0x2000))



#### FILE_ATTRIBUTE_OFFLINE (4096 (0x1000))



#### FILE_ATTRIBUTE_READONLY (1 (0x1))



#### FILE_ATTRIBUTE_SYSTEM (4 (0x4))



#### FILE_ATTRIBUTE_TEMPORARY (256 (0x100))


### -param hTransaction [in]

A handle to the transaction. This handle is returned by the 
      <a href="https://msdn.microsoft.com/578bda35-bd35-4f6d-8366-a4bfb4dbfe42">CreateTransaction</a> function.


##### - dwFileAttributes.FILE_ATTRIBUTE_ARCHIVE (32 (0x20))


##### - dwFileAttributes.FILE_ATTRIBUTE_HIDDEN (2 (0x2))


##### - dwFileAttributes.FILE_ATTRIBUTE_NORMAL (128 (0x80))


##### - dwFileAttributes.FILE_ATTRIBUTE_NOT_CONTENT_INDEXED (8192 (0x2000))


##### - dwFileAttributes.FILE_ATTRIBUTE_OFFLINE (4096 (0x1000))


##### - dwFileAttributes.FILE_ATTRIBUTE_READONLY (1 (0x1))


##### - dwFileAttributes.FILE_ATTRIBUTE_SYSTEM (4 (0x4))


##### - dwFileAttributes.FILE_ATTRIBUTE_TEMPORARY (256 (0x100))


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The following table describes how to set the attributes that cannot be set using 
    <b>SetFileAttributesTransacted</b>. Note that these 
    are not transacted operations.

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
<td>To set a file's compression state, use the 
       <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the 
       <a href="https://msdn.microsoft.com/e6fb29ed-f4f4-4507-8312-d771ffb00256">FSCTL_SET_COMPRESSION</a> operation.</td>
</tr>
<tr>
<td>
<b>FILE_ATTRIBUTE_DEVICE</b>

0x40

</td>
<td>Reserved; do not use.</td>
</tr>
<tr>
<td>
<b>FILE_ATTRIBUTE_DIRECTORY</b>

0x10

</td>
<td>Files cannot be converted into directories. To create a directory, use the 
       <a href="https://msdn.microsoft.com/f8ca8b10-c8bd-4285-8a40-dbec4c24729c">CreateDirectory</a> or 
       <a href="https://msdn.microsoft.com/287996f8-e8ca-4b72-a5f6-016754785c5c">CreateDirectoryEx</a> function.</td>
</tr>
<tr>
<td>
<b>FILE_ATTRIBUTE_ENCRYPTED</b>

0x4000

</td>
<td>To create an encrypted file, use the <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> 
       function with the <b>FILE_ATTRIBUTE_ENCRYPTED</b> attribute. To convert an existing file 
       into an encrypted file, use the <a href="https://msdn.microsoft.com/7620e9fa-74d6-4b41-93db-4a562be63202">EncryptFile</a> 
       function.</td>
</tr>
<tr>
<td>
<b>FILE_ATTRIBUTE_REPARSE_POINT</b>

0x400

</td>
<td>To associate a reparse point with a file or directory, use the 
       <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the 
       <a href="https://msdn.microsoft.com/0bed6d69-269b-4921-8984-69c7829fb9ea">FSCTL_SET_REPARSE_POINT</a> operation.</td>
</tr>
<tr>
<td>
<b>FILE_ATTRIBUTE_SPARSE_FILE</b>

0x200

</td>
<td>To set a file's sparse attribute, use the 
       <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the 
       <a href="https://msdn.microsoft.com/aa8f5880-f831-49b6-8359-fe07c78c032f">FSCTL_SET_SPARSE</a> operation.</td>
</tr>
</table>
 

If a file is open for modification in a transaction, no other thread can successfully open the file for 
    modification until the transaction is committed. If a transacted thread opens the file first, any subsequent 
    threads that attempt to open the file for modification before the transaction is committed will receive a sharing 
    violation. If a non-transacted thread opens the file for modification before the transacted thread does, and it is 
    still open when the transacted thread attempts to open it, the transaction will receive the 
    <b>ERROR_TRANSACTIONAL_CONFLICT</b> error.

For more information on transactions, see 
    <a href="https://msdn.microsoft.com/e8c3ceed-d391-4934-b3f7-12c2123c8c23">Transactional NTFS</a>.

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
 

SMB 3.0 does not support TxF.

<h3><a id="Transacted_Operations"></a><a id="transacted_operations"></a><a id="TRANSACTED_OPERATIONS"></a>Transacted Operations</h3>
If a file is open for modification in a transaction, no other thread can open the file for modification until 
      the transaction is committed. So if a transacted thread opens the file first, any subsequent threads that try 
      modifying the file before the transaction is committed receives a sharing violation. If a non-transacted thread 
      modifies the file before the transacted thread does, and the file is still open when the transaction attempts to 
      open it, the transaction receives the error <b>ERROR_TRANSACTIONAL_CONFLICT</b>.




## -see-also




<a href="https://msdn.microsoft.com/ed9a73d2-7fb6-4fb7-97f6-4dbf89e2f156">File Attribute Constants</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/dd1435da-93e5-440a-913a-9e40e39b4a01">GetFileAttributesTransacted</a>



<a href="https://msdn.microsoft.com/d6bf5df7-bc12-4dec-b116-95d9109f5eb4">Symbolic Links</a>



<a href="https://msdn.microsoft.com/e8c3ceed-d391-4934-b3f7-12c2123c8c23">Transactional NTFS</a>
 

 

