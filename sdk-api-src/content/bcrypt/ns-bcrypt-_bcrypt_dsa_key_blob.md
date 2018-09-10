---
UID: NS:bcrypt._BCRYPT_DSA_KEY_BLOB
title: "_BCRYPT_DSA_KEY_BLOB"
author: windows-sdk-content
description: Used as a header for a Digital Signature Algorithm (DSA) public key or private key BLOB in memory.
old-location: security\bcrypt_dsa_key_blob.htm
tech.root: SecCNG
ms.assetid: 3db36170-106e-49c8-9866-e25759bdd7f9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PBCRYPT_DSA_KEY_BLOB, BCRYPT_DSA_KEY_BLOB, BCRYPT_DSA_KEY_BLOB structure [Security], BCRYPT_DSA_PRIVATE_MAGIC, BCRYPT_DSA_PUBLIC_MAGIC, PBCRYPT_DSA_KEY_BLOB, PBCRYPT_DSA_KEY_BLOB structure pointer [Security], _BCRYPT_DSA_KEY_BLOB, bcrypt/BCRYPT_DSA_KEY_BLOB, bcrypt/PBCRYPT_DSA_KEY_BLOB, security.bcrypt_dsa_key_blob"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - BCRYPT_DSA_KEY_BLOB
product: Windows
targetos: Windows
req.typenames: BCRYPT_DSA_KEY_BLOB, *PBCRYPT_DSA_KEY_BLOB
req.redist: 
---

# _BCRYPT_DSA_KEY_BLOB structure


## -description


The <b>BCRYPT_DSA_KEY_BLOB</b> structure is used as a header for a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Digital Signature Algorithm</a> (DSA) <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> or <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> in memory.


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



The structure applies to DSA keys that equal or exceed 512 bits in length but are less  than or equal to 1024 bits.

This structure is used as a header for a larger buffer. A DSA <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key BLOB</a> (BCRYPT_DSA_PUBLIC_BLOB) has the following format in contiguous memory. The Modulus, Generator, and Public numbers are in big-endian format.

<pre class="syntax" xml:space="preserve"><code>
BCRYPT_DSA_KEY_BLOB
Modulus[cbKey]    // Big-endian.
Generator[cbKey]  // Big-endian.
Public[cbKey]     // Big-endian.
</code></pre>
A DSA <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key BLOB</a> (BCRYPT_DSA_PRIVATE_BLOB) has the following format in contiguous memory. The Modulus, Generator, Public, and PrivateExponent numbers are in big-endian format.

<pre class="syntax" xml:space="preserve"><code>
BCRYPT_DSA_KEY_BLOB
Modulus[cbKey]        // Big-endian.
Generator[cbKey]      // Big-endian.
Public[cbKey]         // Big-endian.
PrivateExponent[20]   // Big-endian.
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/a5d73143-c1d6-43b3-a724-7e27c68a5ade">BCryptExportKey</a>



<a href="https://msdn.microsoft.com/6b9683f4-10f2-40e4-9757-a1f01991bef7">BCryptImportKey</a>
 

 

