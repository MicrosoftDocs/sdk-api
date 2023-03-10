---
UID: NF:winefs.QueryUsersOnEncryptedFile
title: QueryUsersOnEncryptedFile function (winefs.h)
description: Retrieves a list of users for the specified file.
helpviewer_keywords: ["QueryUsersOnEncryptedFile","QueryUsersOnEncryptedFile function [Files]","_win32_queryusersonencryptedfile","base.queryusersonencryptedfile","fs.queryusersonencryptedfile","winefs/QueryUsersOnEncryptedFile"]
old-location: fs\queryusersonencryptedfile.htm
tech.root: fs
ms.assetid: 1bdab753-e7f2-4c08-8b37-3903c0842227
ms.date: 12/05/2018
ms.keywords: QueryUsersOnEncryptedFile, QueryUsersOnEncryptedFile function [Files], _win32_queryusersonencryptedfile, base.queryusersonencryptedfile, fs.queryusersonencryptedfile, winefs/QueryUsersOnEncryptedFile
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
 - QueryUsersOnEncryptedFile
 - winefs/QueryUsersOnEncryptedFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - Ext-MS-Win-AdvAPI32-EncryptedFile-l1-1-0.dll
 - Ext-MS-Win-AdvAPI32-EncryptedFile-L1-1-1.dll
api_name:
 - QueryUsersOnEncryptedFile
req.apiset: ext-ms-win-advapi32-encryptedfile-l1-1-0 (introduced in Windows 8)
---

# QueryUsersOnEncryptedFile function


## -description

Retrieves a list of users for the specified file.

## -parameters

### -param lpFileName [in]

The name of the file.

### -param pUsers [out]

A pointer to a 
<a href="/windows/desktop/api/winefs/ns-winefs-encryption_certificate_hash_list">ENCRYPTION_CERTIFICATE_HASH_LIST</a> structure that receives the list of users.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is a system error code. For a complete list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a> or the header file WinError.h.

## -remarks

When the list of users is no longer needed, call the 
<a href="/windows/desktop/api/winefs/nf-winefs-freeencryptioncertificatehashlist">FreeEncryptionCertificateHashList</a> function to free the list.

In Windows 8, Windows Server 2012, and later, this function is supported by the following technologies.

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



<a href="/windows/desktop/api/winefs/nf-winefs-freeencryptioncertificatehashlist">FreeEncryptionCertificateHashList</a>
