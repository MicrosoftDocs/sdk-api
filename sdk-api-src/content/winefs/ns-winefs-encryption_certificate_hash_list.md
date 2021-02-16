---
UID: NS:winefs._ENCRYPTION_CERTIFICATE_HASH_LIST
title: ENCRYPTION_CERTIFICATE_HASH_LIST (winefs.h)
description: Contains a list of certificate hashes.
helpviewer_keywords: ["*PENCRYPTION_CERTIFICATE_HASH_LIST","ENCRYPTION_CERTIFICATE_HASH_LIST","ENCRYPTION_CERTIFICATE_HASH_LIST structure [Files]","PENCRYPTION_CERTIFICATE_HASH_LIST","PENCRYPTION_CERTIFICATE_HASH_LIST structure pointer [Files]","_win32_encryption_certificate_hash_list_str","base.encryption_certificate_hash_list_str","fs.encryption_certificate_hash_list_str","winefs/ENCRYPTION_CERTIFICATE_HASH_LIST","winefs/PENCRYPTION_CERTIFICATE_HASH_LIST"]
old-location: fs\encryption_certificate_hash_list_str.htm
tech.root: fs
ms.assetid: 988159b3-3cb9-4a4d-9c68-ebfb309cff25
ms.date: 12/05/2018
ms.keywords: '*PENCRYPTION_CERTIFICATE_HASH_LIST, ENCRYPTION_CERTIFICATE_HASH_LIST, ENCRYPTION_CERTIFICATE_HASH_LIST structure [Files], PENCRYPTION_CERTIFICATE_HASH_LIST, PENCRYPTION_CERTIFICATE_HASH_LIST structure pointer [Files], _win32_encryption_certificate_hash_list_str, base.encryption_certificate_hash_list_str, fs.encryption_certificate_hash_list_str, winefs/ENCRYPTION_CERTIFICATE_HASH_LIST, winefs/PENCRYPTION_CERTIFICATE_HASH_LIST'
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
req.typenames: ENCRYPTION_CERTIFICATE_HASH_LIST, *PENCRYPTION_CERTIFICATE_HASH_LIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ENCRYPTION_CERTIFICATE_HASH_LIST
 - winefs/_ENCRYPTION_CERTIFICATE_HASH_LIST
 - PENCRYPTION_CERTIFICATE_HASH_LIST
 - winefs/PENCRYPTION_CERTIFICATE_HASH_LIST
 - ENCRYPTION_CERTIFICATE_HASH_LIST
 - winefs/ENCRYPTION_CERTIFICATE_HASH_LIST
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
 - ENCRYPTION_CERTIFICATE_HASH_LIST
---

# ENCRYPTION_CERTIFICATE_HASH_LIST structure


## -description

Contains a list of certificate hashes.

## -struct-fields

### -field nCert_Hash

The number of certificate hashes in the list.

### -field nCert_Hash.range

### -field nCert_Hash.range.0

### -field nCert_Hash.range.500

### -field pUsers

A pointer to the first 
<a href="/windows/desktop/api/winefs/ns-winefs-encryption_certificate_hash">ENCRYPTION_CERTIFICATE_HASH</a> structure in the list.

### -field pUsers.size_is

### -field pUsers.size_is.nCert_Hash

## -see-also

<a href="/windows/desktop/api/winefs/ns-winefs-encryption_certificate_hash">ENCRYPTION_CERTIFICATE_HASH</a>



<a href="/windows/desktop/FileIO/file-encryption">File Encryption</a>



<a href="/windows/desktop/api/winefs/nf-winefs-freeencryptioncertificatehashlist">FreeEncryptionCertificateHashList</a>



<a href="/windows/desktop/api/winefs/nf-winefs-queryrecoveryagentsonencryptedfile">QueryRecoveryAgentsOnEncryptedFile</a>



<a href="/windows/desktop/api/winefs/nf-winefs-queryusersonencryptedfile">QueryUsersOnEncryptedFile</a>



<a href="/windows/desktop/api/winefs/nf-winefs-removeusersfromencryptedfile">RemoveUsersFromEncryptedFile</a>