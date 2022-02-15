---
UID: NS:bcrypt._BCRYPT_RSAKEY_BLOB
title: BCRYPT_RSAKEY_BLOB (bcrypt.h)
description: Used as a header for an RSA public key or private key BLOB in memory.
helpviewer_keywords: ["BCRYPT_RSAFULLPRIVATE_MAGIC","BCRYPT_RSAKEY_BLOB","BCRYPT_RSAKEY_BLOB structure [Security]","BCRYPT_RSAPRIVATE_MAGIC","BCRYPT_RSAPUBLIC_MAGIC","bcrypt/BCRYPT_RSAKEY_BLOB","security.bcrypt_rsakey_blob"]
old-location: security\bcrypt_rsakey_blob.htm
tech.root: security
ms.assetid: bbf3f4b9-5c69-4212-bb23-34bb2c84185c
ms.date: 12/05/2018
ms.keywords: BCRYPT_RSAFULLPRIVATE_MAGIC, BCRYPT_RSAKEY_BLOB, BCRYPT_RSAKEY_BLOB structure [Security], BCRYPT_RSAPRIVATE_MAGIC, BCRYPT_RSAPUBLIC_MAGIC, bcrypt/BCRYPT_RSAKEY_BLOB, security.bcrypt_rsakey_blob
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
req.typenames: BCRYPT_RSAKEY_BLOB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BCRYPT_RSAKEY_BLOB
 - bcrypt/_BCRYPT_RSAKEY_BLOB
 - BCRYPT_RSAKEY_BLOB
 - bcrypt/BCRYPT_RSAKEY_BLOB
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
 - BCRYPT_RSAKEY_BLOB
---

# BCRYPT_RSAKEY_BLOB structure


## -description

The <b>BCRYPT_RSAKEY_BLOB</b> structure is used as a header for an RSA <a href="/windows/desktop/SecGloss/p-gly">public key</a> or <a href="/windows/desktop/SecGloss/p-gly">private key</a> <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> in memory.

## -struct-fields

### -field Magic

Specifies the type of RSA key this BLOB represents. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_RSAPUBLIC_MAGIC"></a><a id="bcrypt_rsapublic_magic"></a><dl>
<dt><b>BCRYPT_RSAPUBLIC_MAGIC</b></dt>
</dl>
</td>
<td width="60%">
The key is an RSA public key.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_RSAPRIVATE_MAGIC"></a><a id="bcrypt_rsaprivate_magic"></a><dl>
<dt><b>BCRYPT_RSAPRIVATE_MAGIC</b></dt>
</dl>
</td>
<td width="60%">
The key is an RSA private key.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_RSAFULLPRIVATE_MAGIC"></a><a id="bcrypt_rsafullprivate_magic"></a><dl>
<dt><b>BCRYPT_RSAFULLPRIVATE_MAGIC</b></dt>
</dl>
</td>
<td width="60%">
The key is a full RSA private key.

</td>
</tr>
</table>

### -field BitLength

The size, in bits, of the key.

### -field cbPublicExp

The size, in bytes, of the exponent of the key. As of Windows 10 version 1903, public exponents larger than (2^64 - 1) are no longer supported.

### -field cbModulus

The size, in bytes, of the modulus of the key.

### -field cbPrime1

The size, in bytes, of the first prime number of the key. This is only used for private key BLOBs.

### -field cbPrime2

The size, in bytes, of the second prime number of the key. This is only used for private key BLOBs.

## -remarks

This structure is used as a header for a larger buffer. An RSA <a href="/windows/desktop/SecGloss/p-gly">public key BLOB</a> (BCRYPT_RSAPUBLIC_BLOB) has the following format in contiguous memory. All of the numbers following the structure are in big-endian format.


``` syntax

BCRYPT_RSAKEY_BLOB
PublicExponent[cbPublicExp] // Big-endian.
Modulus[cbModulus] // Big-endian.

```

An RSA <a href="/windows/desktop/SecGloss/p-gly">private key BLOB</a> (BCRYPT_RSAPRIVATE_BLOB) has the following format in contiguous memory. All of the numbers following the structure are in big-endian format.


``` syntax

BCRYPT_RSAKEY_BLOB
PublicExponent[cbPublicExp] // Big-endian.
Modulus[cbModulus] // Big-endian.
Prime1[cbPrime1] // Big-endian.
Prime2[cbPrime2] // Big-endian.

```

A full RSA private key BLOB (BCRYPT_RSAFULLPRIVATE_BLOB) has the following format in contiguous memory. All of the numbers following the structure are in big-endian format.

Note that in different versions of Windows, the value that PrivateExponent takes from a call of <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptexportkey">BCryptExportKey</a> may be different as there are several mathematically equivalent representations of the PrivateExponent in cbModulus bytes. Notably, in some versions the PrivateExponent will be exported modulo (Prime1 - 1) \* (Prime2 - 1), and in others it will be exported modulo LeastCommonMultiple(Prime1 - 1, Prime2 - 1).


``` syntax

BCRYPT_RSAKEY_BLOB
PublicExponent[cbPublicExp] // Big-endian.
Modulus[cbModulus] // Big-endian.
Prime1[cbPrime1] // Big-endian.
Prime2[cbPrime2] // Big-endian.
Exponent1[cbPrime1] // Big-endian.
Exponent2[cbPrime2] // Big-endian.
Coefficient[cbPrime1] // Big-endian.
PrivateExponent[cbModulus] // Big-endian.

```


## -see-also

<a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_key_blob">BCRYPT_KEY_BLOB</a>



<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptexportkey">BCryptExportKey</a>



<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptimportkey">BCryptImportKey</a>
