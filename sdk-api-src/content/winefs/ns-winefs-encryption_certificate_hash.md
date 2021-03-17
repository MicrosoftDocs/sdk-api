---
UID: NS:winefs._ENCRYPTION_CERTIFICATE_HASH
title: ENCRYPTION_CERTIFICATE_HASH (winefs.h)
description: Contains a certificate hash and display information for the certificate.
helpviewer_keywords: ["*PENCRYPTION_CERTIFICATE_HASH","ENCRYPTION_CERTIFICATE_HASH","ENCRYPTION_CERTIFICATE_HASH structure [Files]","PENCRYPTION_CERTIFICATE_HASH","PENCRYPTION_CERTIFICATE_HASH structure pointer [Files]","_win32_encryption_certificate_hash_str","base.encryption_certificate_hash_str","fs.encryption_certificate_hash_str","winefs/ENCRYPTION_CERTIFICATE_HASH","winefs/PENCRYPTION_CERTIFICATE_HASH"]
old-location: fs\encryption_certificate_hash_str.htm
tech.root: fs
ms.assetid: 6930446c-5338-4ff9-a662-791fc9e7cefe
ms.date: 12/05/2018
ms.keywords: '*PENCRYPTION_CERTIFICATE_HASH, ENCRYPTION_CERTIFICATE_HASH, ENCRYPTION_CERTIFICATE_HASH structure [Files], PENCRYPTION_CERTIFICATE_HASH, PENCRYPTION_CERTIFICATE_HASH structure pointer [Files], _win32_encryption_certificate_hash_str, base.encryption_certificate_hash_str, fs.encryption_certificate_hash_str, winefs/ENCRYPTION_CERTIFICATE_HASH, winefs/PENCRYPTION_CERTIFICATE_HASH'
req.header: winefs.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: ENCRYPTION_CERTIFICATE_HASH, *PENCRYPTION_CERTIFICATE_HASH
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ENCRYPTION_CERTIFICATE_HASH
 - winefs/_ENCRYPTION_CERTIFICATE_HASH
 - PENCRYPTION_CERTIFICATE_HASH
 - winefs/PENCRYPTION_CERTIFICATE_HASH
 - ENCRYPTION_CERTIFICATE_HASH
 - winefs/ENCRYPTION_CERTIFICATE_HASH
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinEfs.h
api_name:
 - ENCRYPTION_CERTIFICATE_HASH
---

# ENCRYPTION_CERTIFICATE_HASH structure


## -description

Contains a certificate hash and display information for the certificate.

## -struct-fields

### -field cbTotalLength

The length of this structure, in bytes.

### -field pUserSid

The <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> of the user who created the certificate. This member is optional and can be <b>NULL</b>.

### -field pHash

A pointer to an 
<a href="/windows/desktop/api/winefs/ns-winefs-efs_hash_blob">EFS_HASH_BLOB</a> structure.

### -field lpDisplayInformation

User-displayable information for the certificate.  This is usually the user's common name and universal principal name (UPN).

### -field lpDisplayInformation.string

## -see-also

<a href="/windows/desktop/api/winefs/ns-winefs-efs_hash_blob">EFS_HASH_BLOB</a>



<a href="/windows/desktop/api/winefs/ns-winefs-encryption_certificate_hash_list">ENCRYPTION_CERTIFICATE_HASH_LIST</a>



<a href="/windows/desktop/FileIO/file-encryption">File Encryption</a>