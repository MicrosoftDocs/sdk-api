---
UID: NS:winefs._ENCRYPTION_CERTIFICATE_LIST
title: ENCRYPTION_CERTIFICATE_LIST (winefs.h)
description: Contains a list of certificates.
helpviewer_keywords: ["*PENCRYPTION_CERTIFICATE_LIST","ENCRYPTION_CERTIFICATE_LIST","ENCRYPTION_CERTIFICATE_LIST structure [Files]","PENCRYPTION_CERTIFICATE_LIST","PENCRYPTION_CERTIFICATE_LIST structure pointer [Files]","_win32_encryption_certificate_list_str","base.encryption_certificate_list_str","fs.encryption_certificate_list_str","winefs/ENCRYPTION_CERTIFICATE_LIST","winefs/PENCRYPTION_CERTIFICATE_LIST"]
old-location: fs\encryption_certificate_list_str.htm
tech.root: fs
ms.assetid: e1914b96-2fba-49ed-9dd2-464659323eda
ms.date: 12/05/2018
ms.keywords: '*PENCRYPTION_CERTIFICATE_LIST, ENCRYPTION_CERTIFICATE_LIST, ENCRYPTION_CERTIFICATE_LIST structure [Files], PENCRYPTION_CERTIFICATE_LIST, PENCRYPTION_CERTIFICATE_LIST structure pointer [Files], _win32_encryption_certificate_list_str, base.encryption_certificate_list_str, fs.encryption_certificate_list_str, winefs/ENCRYPTION_CERTIFICATE_LIST, winefs/PENCRYPTION_CERTIFICATE_LIST'
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
req.typenames: ENCRYPTION_CERTIFICATE_LIST, *PENCRYPTION_CERTIFICATE_LIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ENCRYPTION_CERTIFICATE_LIST
 - winefs/_ENCRYPTION_CERTIFICATE_LIST
 - PENCRYPTION_CERTIFICATE_LIST
 - winefs/PENCRYPTION_CERTIFICATE_LIST
 - ENCRYPTION_CERTIFICATE_LIST
 - winefs/ENCRYPTION_CERTIFICATE_LIST
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
 - ENCRYPTION_CERTIFICATE_LIST
---

# ENCRYPTION_CERTIFICATE_LIST structure


## -description

Contains a list of certificates.

## -struct-fields

### -field nUsers

The number of certificates in the list.

### -field nUsers.range

### -field nUsers.range.0

### -field nUsers.range.500

### -field pUsers

A pointer to the first 
						<a href="/windows/desktop/api/winefs/ns-winefs-encryption_certificate">ENCRYPTION_CERTIFICATE</a> structure in the list.

### -field pUsers.size_is

### -field pUsers.size_is.nUsers

## -see-also

<a href="/windows/desktop/api/winefs/nf-winefs-adduserstoencryptedfile">AddUsersToEncryptedFile</a>



<a href="/windows/desktop/api/winefs/ns-winefs-encryption_certificate">ENCRYPTION_CERTIFICATE</a>



<a href="/windows/desktop/FileIO/file-encryption">File Encryption</a>