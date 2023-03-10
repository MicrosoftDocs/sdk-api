---
UID: NF:winefs.RemoveUsersFromEncryptedFile
title: RemoveUsersFromEncryptedFile function (winefs.h)
description: Removes specified certificate hashes from a specified file.
helpviewer_keywords: ["RemoveUsersFromEncryptedFile","RemoveUsersFromEncryptedFile function [Files]","_win32_removeusersfromencryptedfile","base.removeusersfromencryptedfile","fs.removeusersfromencryptedfile","winefs/RemoveUsersFromEncryptedFile"]
old-location: fs\removeusersfromencryptedfile.htm
tech.root: fs
ms.assetid: c6672581-24b4-464c-b32d-48a04e56eef8
ms.date: 12/05/2018
ms.keywords: RemoveUsersFromEncryptedFile, RemoveUsersFromEncryptedFile function [Files], _win32_removeusersfromencryptedfile, base.removeusersfromencryptedfile, fs.removeusersfromencryptedfile, winefs/RemoveUsersFromEncryptedFile
req.header: winefs.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RemoveUsersFromEncryptedFile
 - winefs/RemoveUsersFromEncryptedFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - Ext-MS-Win-AdvAPI32-EncryptedFile-L1-1-1.dll
api_name:
 - RemoveUsersFromEncryptedFile
req.apiset: ext-ms-win-advapi32-encryptedfile-l1-1-1 (introduced in Windows 10, version 10.0.14393)
---

# RemoveUsersFromEncryptedFile function


## -description

Removes specified certificate hashes from a specified file.

## -parameters

### -param lpFileName [in]

The name of the file.

### -param pHashes [in]

A pointer to an 
<a href="/windows/desktop/api/winefs/ns-winefs-encryption_certificate_hash_list">ENCRYPTION_CERTIFICATE_HASH_LIST</a> structure that contains a list of certificate hashes to be removed from the file.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is a system error code. For a complete list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a> or the header file WinError.h.

## -remarks

The 
<b>RemoveUsersFromEncryptedFile</b> function removes the specified certificate hashes if they exist in the specified file. If any of the certificate hashes are not found in the specified file, they are ignored and no error code is returned.

Starting with Windows 8 and Windows Server 2012, this function is supported by the following technologies.

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
 

SMB 3.0 does not support EFS on shares with continuous availability capability.

## -see-also

<a href="/windows/desktop/api/winefs/ns-winefs-encryption_certificate_hash_list">ENCRYPTION_CERTIFICATE_HASH_LIST</a>



<a href="/windows/desktop/FileIO/file-encryption">File Encryption</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>
