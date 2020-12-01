---
UID: NS:bcrypt._BCRYPT_KEY_DATA_BLOB_HEADER
title: BCRYPT_KEY_DATA_BLOB_HEADER (bcrypt.h)
description: Used to contain information about a key data BLOB.
helpviewer_keywords: ["*PBCRYPT_KEY_DATA_BLOB_HEADER","BCRYPT_KEY_DATA_BLOB_HEADER","BCRYPT_KEY_DATA_BLOB_HEADER structure [Security]","BCRYPT_KEY_DATA_BLOB_MAGIC","BCRYPT_KEY_DATA_BLOB_VERSION1","PBCRYPT_KEY_DATA_BLOB_HEADER","PBCRYPT_KEY_DATA_BLOB_HEADER structure pointer [Security]","bcrypt/BCRYPT_KEY_DATA_BLOB_HEADER","bcrypt/PBCRYPT_KEY_DATA_BLOB_HEADER","security.bcrypt_key_data_blob_header"]
old-location: security\bcrypt_key_data_blob_header.htm
tech.root: security
ms.assetid: 054bba02-c73a-496d-b619-749c3f4e8ad9
ms.date: 12/05/2018
ms.keywords: '*PBCRYPT_KEY_DATA_BLOB_HEADER, BCRYPT_KEY_DATA_BLOB_HEADER, BCRYPT_KEY_DATA_BLOB_HEADER structure [Security], BCRYPT_KEY_DATA_BLOB_MAGIC, BCRYPT_KEY_DATA_BLOB_VERSION1, PBCRYPT_KEY_DATA_BLOB_HEADER, PBCRYPT_KEY_DATA_BLOB_HEADER structure pointer [Security], bcrypt/BCRYPT_KEY_DATA_BLOB_HEADER, bcrypt/PBCRYPT_KEY_DATA_BLOB_HEADER, security.bcrypt_key_data_blob_header'
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: BCRYPT_KEY_DATA_BLOB_HEADER, *PBCRYPT_KEY_DATA_BLOB_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BCRYPT_KEY_DATA_BLOB_HEADER
 - bcrypt/_BCRYPT_KEY_DATA_BLOB_HEADER
 - PBCRYPT_KEY_DATA_BLOB_HEADER
 - bcrypt/PBCRYPT_KEY_DATA_BLOB_HEADER
 - BCRYPT_KEY_DATA_BLOB_HEADER
 - bcrypt/BCRYPT_KEY_DATA_BLOB_HEADER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bcrypt.h
api_name:
 - BCRYPT_KEY_DATA_BLOB_HEADER
---

# BCRYPT_KEY_DATA_BLOB_HEADER structure


## -description

The <b>BCRYPT_KEY_DATA_BLOB_HEADER</b> structure is used to contain information about a key data BLOB. The key data BLOB must immediately follow this structure in memory.

## -struct-fields

### -field dwMagic

The magic value for the key.


This member must be the following value.





#### BCRYPT_KEY_DATA_BLOB_MAGIC (0x4d42444b)

### -field dwVersion

Contains the numeric version of the key.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_KEY_DATA_BLOB_VERSION1"></a><a id="bcrypt_key_data_blob_version1"></a><dl>
<dt><b>BCRYPT_KEY_DATA_BLOB_VERSION1</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Version 1.

</td>
</tr>
</table>

### -field cbKeyData

The size, in bytes, of the key data.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptexportkey">BCryptExportKey</a>



<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptimportkey">BCryptImportKey</a>