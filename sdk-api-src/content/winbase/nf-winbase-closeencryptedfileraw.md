---
UID: NF:winbase.CloseEncryptedFileRaw
title: CloseEncryptedFileRaw function (winbase.h)
description: Closes an encrypted file after a backup or restore operation, and frees associated system resources.
helpviewer_keywords: ["CloseEncryptedFileRaw","CloseEncryptedFileRaw function [Files]","base.closeencryptedfileraw","fs.closeencryptedfileraw","winbase/CloseEncryptedFileRaw"]
old-location: fs\closeencryptedfileraw.htm
tech.root: fs
ms.assetid: 54bf7114-0ebb-4d9c-bc67-2ac351dbe55d
ms.date: 12/05/2018
ms.keywords: CloseEncryptedFileRaw, CloseEncryptedFileRaw function [Files], base.closeencryptedfileraw, fs.closeencryptedfileraw, winbase/CloseEncryptedFileRaw
req.header: winbase.h
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
 - CloseEncryptedFileRaw
 - winbase/CloseEncryptedFileRaw
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
 - CloseEncryptedFileRaw
req.apiset: ext-ms-win-advapi32-encryptedfile-l1-1-0 (introduced in Windows 8)
---

# CloseEncryptedFileRaw function


## -description

Closes an encrypted file after a backup 
or restore operation, and frees associated system resources. This is one of a group of Encrypted File System (EFS) functions that is intended  to implement backup and restore functionality, while maintaining files in their encrypted state.

## -parameters

### -param pvContext [in]

A pointer to a system-defined context block. The
         <a href="/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa">OpenEncryptedFileRaw</a> function returns the context block.

## -remarks

The <b>CloseEncryptedFileRaw</b> function frees allocated system resources
      such as the system-defined context block and closes the file.

The  <a href="/windows/desktop/api/winbase/nf-winbase-backupread">BackupRead</a> and <a href="/windows/desktop/api/winbase/nf-winbase-backupwrite">BackupWrite</a> functions handle backup and restore of unencrypted files.

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
 

Note that SMB 3.0 does not support EFS on shares with continuous availability capability.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-backupread">BackupRead</a>



<a href="/windows/desktop/api/winbase/nf-winbase-backupwrite">BackupWrite</a>



<a href="/windows/desktop/FileIO/file-encryption">File Encryption</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa">OpenEncryptedFileRaw</a>



<a href="/windows/desktop/api/winbase/nf-winbase-readencryptedfileraw">ReadEncryptedFileRaw</a>



<a href="/windows/desktop/api/winbase/nf-winbase-writeencryptedfileraw">WriteEncryptedFileRaw</a>
