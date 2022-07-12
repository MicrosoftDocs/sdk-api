---
UID: NF:winefs.AddUsersToEncryptedFile
title: AddUsersToEncryptedFile function (winefs.h)
description: Adds user keys to the specified encrypted file.
helpviewer_keywords: ["AddUsersToEncryptedFile","AddUsersToEncryptedFile function [Files]","_win32_adduserstoencryptedfile","base.adduserstoencryptedfile","fs.adduserstoencryptedfile","winefs/AddUsersToEncryptedFile"]
old-location: fs\adduserstoencryptedfile.htm
tech.root: fs
ms.assetid: a92d6a52-20d1-4d5c-a222-ab9afaf85c4b
ms.date: 12/05/2018
ms.keywords: AddUsersToEncryptedFile, AddUsersToEncryptedFile function [Files], _win32_adduserstoencryptedfile, base.adduserstoencryptedfile, fs.adduserstoencryptedfile, winefs/AddUsersToEncryptedFile
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
 - AddUsersToEncryptedFile
 - winefs/AddUsersToEncryptedFile
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
 - AddUsersToEncryptedFile
req.apiset: ext-ms-win-advapi32-encryptedfile-l1-1-1 (introduced in Windows 10, version 10.0.14393)
---

# AddUsersToEncryptedFile function


## -description

Adds user keys to the specified encrypted file.

## -parameters

### -param lpFileName [in]

The name of the encrypted file.

### -param pEncryptionCertificates [in]

A pointer to an 
<a href="/windows/desktop/api/winefs/ns-winefs-encryption_certificate_list">ENCRYPTION_CERTIFICATE_LIST</a> structure that contains the list of new user keys to be added to the file.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is a system error code. For a complete list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a> or the header file WinError.h.

## -remarks

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
 

SMB 3.0 does not support EFS on shares with continuous availability capability.


#### Examples

For example code that uses this function, see <a href="/windows/desktop/FileIO/adding-users-to-an-encrypted-file">Adding Users to an Encrypted File</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winefs/ns-winefs-encryption_certificate_list">ENCRYPTION_CERTIFICATE_LIST</a>



<a href="/windows/desktop/FileIO/file-encryption">File Encryption</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>
