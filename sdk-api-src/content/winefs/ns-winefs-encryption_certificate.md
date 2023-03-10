---
UID: NS:winefs._ENCRYPTION_CERTIFICATE
title: ENCRYPTION_CERTIFICATE (winefs.h)
description: Contains a certificate and the SID of its owner.
helpviewer_keywords: ["*PENCRYPTION_CERTIFICATE","ENCRYPTION_CERTIFICATE","ENCRYPTION_CERTIFICATE structure [Files]","PENCRYPTION_CERTIFICATE","PENCRYPTION_CERTIFICATE structure pointer [Files]","_win32_encryption_certificate_str","base.encryption_certificate_str","fs.encryption_certificate_str","winefs/ENCRYPTION_CERTIFICATE","winefs/PENCRYPTION_CERTIFICATE"]
old-location: fs\encryption_certificate_str.htm
tech.root: fs
ms.assetid: 33b36659-48bb-4297-8142-f8702db03d20
ms.date: 12/05/2018
ms.keywords: '*PENCRYPTION_CERTIFICATE, ENCRYPTION_CERTIFICATE, ENCRYPTION_CERTIFICATE structure [Files], PENCRYPTION_CERTIFICATE, PENCRYPTION_CERTIFICATE structure pointer [Files], _win32_encryption_certificate_str, base.encryption_certificate_str, fs.encryption_certificate_str, winefs/ENCRYPTION_CERTIFICATE, winefs/PENCRYPTION_CERTIFICATE'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ENCRYPTION_CERTIFICATE, *PENCRYPTION_CERTIFICATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ENCRYPTION_CERTIFICATE
 - winefs/_ENCRYPTION_CERTIFICATE
 - PENCRYPTION_CERTIFICATE
 - winefs/PENCRYPTION_CERTIFICATE
 - ENCRYPTION_CERTIFICATE
 - winefs/ENCRYPTION_CERTIFICATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winefs.h
api_name:
 - ENCRYPTION_CERTIFICATE
---

# ENCRYPTION_CERTIFICATE structure


## -description

Contains a certificate and the SID of its owner.

## -struct-fields

### -field cbTotalLength

The length of this structure, in bytes.

### -field pUserSid

The <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> of the user who owns the certificate.

### -field pCertBlob

A pointer to an 
<a href="/windows/win32/api/winefs/ns-winefs-efs_certificate_blob">EFS_CERTIFICATE_BLOB</a> structure.

## -see-also

<a href="/windows/win32/api/winefs/ns-winefs-efs_certificate_blob">EFS_CERTIFICATE_BLOB</a>



<a href="/windows/desktop/api/winefs/ns-winefs-encryption_certificate_list">ENCRYPTION_CERTIFICATE_LIST</a>



<a href="/windows/desktop/FileIO/file-encryption">File Encryption</a>



<a href="/windows/desktop/api/winefs/nf-winefs-setuserfileencryptionkey">SetUserFileEncryptionKey</a>