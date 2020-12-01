---
UID: NS:ncrypt._NCRYPT_KEY_BLOB_HEADER
title: NCRYPT_KEY_BLOB_HEADER (ncrypt.h)
description: Contains a key BLOB.
helpviewer_keywords: ["*PNCRYPT_KEY_BLOB_HEADER","NCRYPT_KEY_BLOB_HEADER","NCRYPT_KEY_BLOB_HEADER structure [Security]","PNCRYPT_KEY_BLOB_HEADER","PNCRYPT_KEY_BLOB_HEADER structure pointer [Security]","ncrypt/NCRYPT_KEY_BLOB_HEADER","ncrypt/PNCRYPT_KEY_BLOB_HEADER","security.ncrypt_key_blob_header"]
old-location: security\ncrypt_key_blob_header.htm
tech.root: security
ms.assetid: 387F05A3-C6E2-48EE-8FD0-C0A45E752300
ms.date: 12/05/2018
ms.keywords: '*PNCRYPT_KEY_BLOB_HEADER, NCRYPT_KEY_BLOB_HEADER, NCRYPT_KEY_BLOB_HEADER structure [Security], PNCRYPT_KEY_BLOB_HEADER, PNCRYPT_KEY_BLOB_HEADER structure pointer [Security], ncrypt/NCRYPT_KEY_BLOB_HEADER, ncrypt/PNCRYPT_KEY_BLOB_HEADER, security.ncrypt_key_blob_header'
req.header: ncrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: NCRYPT_KEY_BLOB_HEADER, *PNCRYPT_KEY_BLOB_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NCRYPT_KEY_BLOB_HEADER
 - ncrypt/_NCRYPT_KEY_BLOB_HEADER
 - PNCRYPT_KEY_BLOB_HEADER
 - ncrypt/PNCRYPT_KEY_BLOB_HEADER
 - NCRYPT_KEY_BLOB_HEADER
 - ncrypt/NCRYPT_KEY_BLOB_HEADER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ncrypt.h
api_name:
 - NCRYPT_KEY_BLOB_HEADER
---

# NCRYPT_KEY_BLOB_HEADER structure


## -description

The <b>NCRYPT_KEY_BLOB_HEADER</b> structure contains a key <b>BLOB</b>. This structure is used by the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptexportkey">NCryptExportKey</a> and <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptimportkey">NCryptImportKey</a> functions.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field dwMagic

Identifies the <b>BLOB</b> type. This can be one of the following values.

<ul>
<li>NCRYPT_CIPHER_KEY_BLOB_MAGIC</li>
<li>NCRYPT_PROTECTED_KEY_BLOB_MAGIC</li>
</ul>

### -field cbAlgName

Size, in bytes, of the null-terminated algorithm name, including the terminating zero.

### -field cbKeyData

Size, in bytes, of the <b>BLOB</b>.

## -see-also

<a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptexportkey">NCryptExportKey</a>



<a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptimportkey">NCryptImportKey</a>