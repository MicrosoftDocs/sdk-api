---
UID: NS:bcrypt._BCRYPT_DSA_KEY_BLOB
title: BCRYPT_DSA_KEY_BLOB (bcrypt.h)
description: Used as a header for a Digital Signature Algorithm (DSA) public key or private key BLOB in memory. (BCRYPT_DSA_KEY_BLOB)
helpviewer_keywords: ["*PBCRYPT_DSA_KEY_BLOB","BCRYPT_DSA_KEY_BLOB","BCRYPT_DSA_KEY_BLOB structure [Security]","BCRYPT_DSA_PRIVATE_MAGIC","BCRYPT_DSA_PUBLIC_MAGIC","PBCRYPT_DSA_KEY_BLOB","PBCRYPT_DSA_KEY_BLOB structure pointer [Security]","bcrypt/BCRYPT_DSA_KEY_BLOB","bcrypt/PBCRYPT_DSA_KEY_BLOB","security.bcrypt_dsa_key_blob"]
old-location: security\bcrypt_dsa_key_blob.htm
tech.root: security
ms.assetid: 3db36170-106e-49c8-9866-e25759bdd7f9
ms.date: 12/05/2018
ms.keywords: '*PBCRYPT_DSA_KEY_BLOB, BCRYPT_DSA_KEY_BLOB, BCRYPT_DSA_KEY_BLOB structure [Security], BCRYPT_DSA_PRIVATE_MAGIC, BCRYPT_DSA_PUBLIC_MAGIC, PBCRYPT_DSA_KEY_BLOB, PBCRYPT_DSA_KEY_BLOB structure pointer [Security], bcrypt/BCRYPT_DSA_KEY_BLOB, bcrypt/PBCRYPT_DSA_KEY_BLOB, security.bcrypt_dsa_key_blob'
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
req.typenames: BCRYPT_DSA_KEY_BLOB, *PBCRYPT_DSA_KEY_BLOB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BCRYPT_DSA_KEY_BLOB
 - bcrypt/_BCRYPT_DSA_KEY_BLOB
 - PBCRYPT_DSA_KEY_BLOB
 - bcrypt/PBCRYPT_DSA_KEY_BLOB
 - BCRYPT_DSA_KEY_BLOB
 - bcrypt/BCRYPT_DSA_KEY_BLOB
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
 - BCRYPT_DSA_KEY_BLOB
---

# BCRYPT_DSA_KEY_BLOB structure


## -description

The <b>BCRYPT_DSA_KEY_BLOB</b> structure is used as a header for a <a href="/windows/desktop/SecGloss/d-gly">Digital Signature Algorithm</a> (DSA) <a href="/windows/desktop/SecGloss/p-gly">public key</a> or <a href="/windows/desktop/SecGloss/p-gly">private key</a> <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> in memory.

## -struct-fields

### -field dwMagic

Determines the type of key this structure represents. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_DSA_PUBLIC_MAGIC"></a><a id="bcrypt_dsa_public_magic"></a><dl>
<dt><b>BCRYPT_DSA_PUBLIC_MAGIC</b></dt>
<dt>0x42505344</dt>
</dl>
</td>
<td width="60%">
The structure represents a DSA public key.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_DSA_PRIVATE_MAGIC"></a><a id="bcrypt_dsa_private_magic"></a><dl>
<dt><b>BCRYPT_DSA_PRIVATE_MAGIC</b></dt>
<dt>0x56505344</dt>
</dl>
</td>
<td width="60%">
The structure represents a DSA private key.

</td>
</tr>
</table>

### -field cbKey

The length, in bytes, of the key.

### -field Count

The number of iterations, in big-endian format, used to generate <i>q</i>.

### -field Seed

The seed value, in big-endian format, used to generate <i>q</i>.

### -field q

The 160-bit prime factor, in big-endian format.

## -remarks

The structure applies to DSA keys that equal or exceed 512 bits in length but are less than or equal to 1024 bits.

This structure is used as a header for a larger buffer. A DSA <a href="/windows/desktop/SecGloss/p-gly">public key BLOB</a> (BCRYPT_DSA_PUBLIC_BLOB) has the following format in contiguous memory. The Modulus, Generator, and Public numbers are in big-endian format.


``` syntax

BCRYPT_DSA_KEY_BLOB
Modulus[cbKey]    // Big-endian.
Generator[cbKey]  // Big-endian.
Public[cbKey]     // Big-endian.

```

A DSA <a href="/windows/desktop/SecGloss/p-gly">private key BLOB</a> (BCRYPT_DSA_PRIVATE_BLOB) has the following format in contiguous memory. The Modulus, Generator, Public, and PrivateExponent numbers are in big-endian format.


``` syntax

BCRYPT_DSA_KEY_BLOB
Modulus[cbKey]        // Big-endian.
Generator[cbKey]      // Big-endian.
Public[cbKey]         // Big-endian.
PrivateExponent[20]   // Big-endian.

```


## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptexportkey">BCryptExportKey</a>

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptimportkeypair">BCryptImportKeyPair</a>
