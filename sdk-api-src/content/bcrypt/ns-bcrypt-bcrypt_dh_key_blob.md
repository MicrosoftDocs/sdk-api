---
UID: NS:bcrypt._BCRYPT_DH_KEY_BLOB
title: BCRYPT_DH_KEY_BLOB (bcrypt.h)
description: Used as a header for a Diffie-Hellman public key or private key BLOB in memory.helpviewer_keywords: ["*PBCRYPT_DH_KEY_BLOB","BCRYPT_DH_KEY_BLOB","BCRYPT_DH_KEY_BLOB structure [Security]","BCRYPT_DH_PRIVATE_MAGIC","BCRYPT_DH_PUBLIC_MAGIC","PBCRYPT_DH_KEY_BLOB","PBCRYPT_DH_KEY_BLOB structure pointer [Security]","bcrypt/BCRYPT_DH_KEY_BLOB","bcrypt/PBCRYPT_DH_KEY_BLOB","security.bcrypt_dh_key_blob"]
old-location: security\bcrypt_dh_key_blob.htm
tech.root: SecCNG
ms.assetid: 6004b2e5-7e06-4108-a0da-472b9b6d5fea
ms.date: 12/05/2018
ms.keywords: '*PBCRYPT_DH_KEY_BLOB, BCRYPT_DH_KEY_BLOB, BCRYPT_DH_KEY_BLOB structure [Security], BCRYPT_DH_PRIVATE_MAGIC, BCRYPT_DH_PUBLIC_MAGIC, PBCRYPT_DH_KEY_BLOB, PBCRYPT_DH_KEY_BLOB structure pointer [Security], bcrypt/BCRYPT_DH_KEY_BLOB, bcrypt/PBCRYPT_DH_KEY_BLOB, security.bcrypt_dh_key_blob'
f1_keywords:
- bcrypt/BCRYPT_DH_KEY_BLOB
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Bcrypt.h
api_name:
- BCRYPT_DH_KEY_BLOB
targetos: Windows
req.typenames: BCRYPT_DH_KEY_BLOB, *PBCRYPT_DH_KEY_BLOB
req.redist: 
ms.custom: 19H1
---

# BCRYPT_DH_KEY_BLOB structure


## -description


The <b>BCRYPT_DH_KEY_BLOB</b> structure is used as a header for a Diffie-Hellman <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">public key</a> or <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">private key</a> <a href="https://docs.microsoft.com/windows/desktop/SecGloss/b-gly">BLOB</a> in memory.


## -struct-fields




### -field dwMagic

Determines the type of key this structure represents. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_DH_PUBLIC_MAGIC"></a><a id="bcrypt_dh_public_magic"></a><dl>
<dt><b>BCRYPT_DH_PUBLIC_MAGIC</b></dt>
<dt>0x42504844</dt>
</dl>
</td>
<td width="60%">
The structure represents a Diffie-Hellman public key.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_DH_PRIVATE_MAGIC"></a><a id="bcrypt_dh_private_magic"></a><dl>
<dt><b>BCRYPT_DH_PRIVATE_MAGIC</b></dt>
<dt>0x56504844</dt>
</dl>
</td>
<td width="60%">
The structure represents a Diffie-Hellman private key.

</td>
</tr>
</table>
 


### -field cbKey

The length, in bytes, of the key.


## -remarks



This structure is used as a header for a larger buffer. A Diffie-Hellman <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">public key BLOB</a> (BCRYPT_DH_PUBLIC_BLOB) has the following format in contiguous memory. The Modulus, Generator, and Public numbers are in big-endian format.

<pre class="syntax" xml:space="preserve"><code>
BCRYPT_DH_KEY_BLOB
Modulus[cbKey] // Big-endian.
Generator[cbKey] // Big-endian.
Public[cbKey] // Big-endian.
</code></pre>
A Diffie-Hellman <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">private key BLOB</a> (BCRYPT_DH_PRIVATE_BLOB) has the following format in contiguous memory. The Modulus, Generator, Public, and PrivateExponent numbers are in big-endian format.

<pre class="syntax" xml:space="preserve"><code>
BCRYPT_DH_KEY_BLOB
Modulus[cbKey] // Big-endian.
Generator[cbKey] // Big-endian.
Public[cbKey] // Big-endian.
PrivateExponent[cbKey] // Big-endian.
</code></pre>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bcrypt/nf-bcrypt-bcryptexportkey">BCryptExportKey</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bcrypt/nf-bcrypt-bcryptimportkey">BCryptImportKey</a>
 

 

