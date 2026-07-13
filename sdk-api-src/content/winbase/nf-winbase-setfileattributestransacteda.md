---
UID: NF:winbase.SetFileAttributesTransactedA
title: SetFileAttributesTransactedA function (winbase.h)
description: Sets the attributes for a file or directory as a transacted operation. (ANSI)
helpviewer_keywords: ["FILE_ATTRIBUTE_ARCHIVE", "FILE_ATTRIBUTE_HIDDEN", "FILE_ATTRIBUTE_NORMAL", "FILE_ATTRIBUTE_NOT_CONTENT_INDEXED", "FILE_ATTRIBUTE_OFFLINE", "FILE_ATTRIBUTE_READONLY", "FILE_ATTRIBUTE_SYSTEM", "FILE_ATTRIBUTE_TEMPORARY", "SetFileAttributesTransactedA", "winbase/SetFileAttributesTransactedA"]
old-location: fs\setfileattributestransacted.htm
tech.root: fs
ms.assetid: e25e77b2-a6ad-4ce4-8589-d7ff6c4074f6
ms.date: 12/05/2018
ms.keywords: FILE_ATTRIBUTE_ARCHIVE, FILE_ATTRIBUTE_HIDDEN, FILE_ATTRIBUTE_NORMAL, FILE_ATTRIBUTE_NOT_CONTENT_INDEXED, FILE_ATTRIBUTE_OFFLINE, FILE_ATTRIBUTE_READONLY, FILE_ATTRIBUTE_SYSTEM, FILE_ATTRIBUTE_TEMPORARY, SetFileAttributesTransacted, SetFileAttributesTransacted function [Files], SetFileAttributesTransactedA, SetFileAttributesTransactedW, fs.setfileattributestransacted, winbase/SetFileAttributesTransacted, winbase/SetFileAttributesTransactedA, winbase/SetFileAttributesTransactedW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetFileAttributesTransactedA
 - winbase/SetFileAttributesTransactedA
dev_langs:
 - c++
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
---

# SetFileAttributesTransactedA function


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Sets the attributes for a file or directory as a transacted operation.

## -parameters

### -param lpFileName [in]

The name of the file whose attributes are to be set.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

The file must reside on the local computer; otherwise, the function fails and the last error code is set to 
      <b>ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE</b>.

### -param dwFileAttributes [in]

The file attributes to set for the file.

For a list of file attribute value and their descriptions, see 
       <a href="/windows/desktop/FileIO/file-attribute-constants">File Attribute Constants</a>. This parameter can be 
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
      <a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

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
       <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the 
       <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_set_compression">FSCTL_SET_COMPRESSION</a> operation.</td>
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
       <a href="/windows/desktop/api/fileapi/nf-fileapi-createdirectorya">CreateDirectory</a> or 
       <a href="/windows/desktop/api/winbase/nf-winbase-createdirectoryexa">CreateDirectoryEx</a> function.</td>
</tr>
<tr>
<td>
<b>FILE_ATTRIBUTE_ENCRYPTED</b>

0x4000

</td>
<td>To create an encrypted file, use the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> 
       function with the <b>FILE_ATTRIBUTE_ENCRYPTED</b> attribute. To convert an existing file 
       into an encrypted file, use the <a href="/windows/desktop/api/winbase/nf-winbase-encryptfilea">EncryptFile</a> 
       function.</td>
</tr>
<tr>
<td>
<b>FILE_ATTRIBUTE_REPARSE_POINT</b>

0x400

</td>
<td>To associate a reparse point with a file or directory, use the 
       <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the 
       <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_set_reparse_point">FSCTL_SET_REPARSE_POINT</a> operation.</td>
</tr>
<tr>
<td>
<b>FILE_ATTRIBUTE_SPARSE_FILE</b>

0x200

</td>
<td>To set a file's sparse attribute, use the 
       <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the 
       <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_set_sparse">FSCTL_SET_SPARSE</a> operation.</td>
</tr>
</table>
 

If a file is open for modification in a transaction, no other thread can successfully open the file for 
    modification until the transaction is committed. If a transacted thread opens the file first, any subsequent 
    threads that attempt to open the file for modification before the transaction is committed will receive a sharing 
    violation. If a non-transacted thread opens the file for modification before the transacted thread does, and it is 
    still open when the transacted thread attempts to open it, the transaction will receive the 
    <b>ERROR_TRANSACTIONAL_CONFLICT</b> error.

For more information on transactions, see 
    <a href="/windows/desktop/FileIO/transactional-ntfs-portal">Transactional NTFS</a>.

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





> [!NOTE]
> The winbase.h header defines SetFileAttributesTransacted as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/FileIO/file-attribute-constants">File Attribute Constants</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getfileattributestransacteda">GetFileAttributesTransacted</a>



<a href="/windows/desktop/FileIO/symbolic-links">Symbolic Links</a>



<a href="/windows/desktop/FileIO/transactional-ntfs-portal">Transactional NTFS</a>
