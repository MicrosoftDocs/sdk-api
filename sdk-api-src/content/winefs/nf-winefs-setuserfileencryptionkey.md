---
UID: NF:winefs.SetUserFileEncryptionKey
title: SetUserFileEncryptionKey function (winefs.h)
description: Sets the user's current key to the specified certificate.
helpviewer_keywords: ["SetUserFileEncryptionKey","SetUserFileEncryptionKey function [Files]","_win32_setuserfileencryptionkey","base.setuserfileencryptionkey","fs.setuserfileencryptionkey","winefs/SetUserFileEncryptionKey"]
old-location: fs\setuserfileencryptionkey.htm
tech.root: fs
ms.assetid: dd23fab7-1675-4d0d-911c-e2aac2273e7f
ms.date: 12/05/2018
ms.keywords: SetUserFileEncryptionKey, SetUserFileEncryptionKey function [Files], _win32_setuserfileencryptionkey, base.setuserfileencryptionkey, fs.setuserfileencryptionkey, winefs/SetUserFileEncryptionKey
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
 - SetUserFileEncryptionKey
 - winefs/SetUserFileEncryptionKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - SetUserFileEncryptionKey
---

# SetUserFileEncryptionKey function


## -description

Sets the user's current key to the specified certificate.

## -parameters

### -param pEncryptionCertificate [in]

A pointer to a certificate that will be the user's key. This parameter is a pointer to an 
<a href="/windows/desktop/api/winefs/ns-winefs-encryption_certificate">ENCRYPTION_CERTIFICATE</a> structure.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is a system error code. For a complete list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a> or the header file WinError.h.

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

<a href="/windows/desktop/api/winefs/ns-winefs-encryption_certificate">ENCRYPTION_CERTIFICATE</a>



<a href="/windows/desktop/FileIO/file-encryption">File Encryption</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>