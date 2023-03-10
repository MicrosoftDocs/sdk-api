---
UID: NF:winefs.FreeEncryptionCertificateHashList
title: FreeEncryptionCertificateHashList function (winefs.h)
description: Frees a certificate hash list.
helpviewer_keywords: ["FreeEncryptionCertificateHashList","FreeEncryptionCertificateHashList function [Files]","_win32_freeencryptioncertificatehashlist","base.freeencryptioncertificatehashlist","fs.freeencryptioncertificatehashlist","winefs/FreeEncryptionCertificateHashList"]
old-location: fs\freeencryptioncertificatehashlist.htm
tech.root: fs
ms.assetid: 63d5811f-a135-45b0-8f23-fd8851f7bcca
ms.date: 12/05/2018
ms.keywords: FreeEncryptionCertificateHashList, FreeEncryptionCertificateHashList function [Files], _win32_freeencryptioncertificatehashlist, base.freeencryptioncertificatehashlist, fs.freeencryptioncertificatehashlist, winefs/FreeEncryptionCertificateHashList
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
 - FreeEncryptionCertificateHashList
 - winefs/FreeEncryptionCertificateHashList
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
 - FreeEncryptionCertificateHashList
req.apiset: ext-ms-win-advapi32-encryptedfile-l1-1-0 (introduced in Windows 8)
---

# FreeEncryptionCertificateHashList function


## -description

Frees a certificate hash list.

## -parameters

### -param pUsers [in]

A pointer to a certificate hash list structure, 
<a href="/windows/desktop/api/winefs/ns-winefs-encryption_certificate_hash_list">ENCRYPTION_CERTIFICATE_HASH_LIST</a>, which was returned by the 
<a href="/windows/desktop/api/winefs/nf-winefs-queryusersonencryptedfile">QueryUsersOnEncryptedFile</a> or 
<a href="/windows/desktop/api/winefs/nf-winefs-queryrecoveryagentsonencryptedfile">QueryRecoveryAgentsOnEncryptedFile</a> function.

## -remarks

<b>ReFS:  </b>This function is not supported.

## -see-also

<a href="/windows/desktop/api/winefs/ns-winefs-encryption_certificate_hash_list">ENCRYPTION_CERTIFICATE_HASH_LIST</a>



<a href="/windows/desktop/FileIO/file-encryption">File Encryption</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/winefs/nf-winefs-queryrecoveryagentsonencryptedfile">QueryRecoveryAgentsOnEncryptedFile</a>



<a href="/windows/desktop/api/winefs/nf-winefs-queryusersonencryptedfile">QueryUsersOnEncryptedFile</a>
