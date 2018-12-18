---
UID: NS:bcrypt._BCRYPT_DSA_KEY_BLOB_V2
title: BCRYPT_DSA_KEY_BLOB_V2
author: windows-sdk-content
description: Used as a header for a Digital Signature Algorithm (DSA) public key or private key BLOB in memory.
old-location: security\bcrypt_dsa_key_blob_v2.htm
tech.root: seccng
ms.assetid: E8240DE1-B65F-4DAC-92C9-45725435A0F7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PBCRYPT_DSA_KEY_BLOB_V2, BCRYPT_DSA_KEY_BLOB_V2, BCRYPT_DSA_KEY_BLOB_V2 structure [Security], BCRYPT_DSA_PRIVATE_MAGIC, BCRYPT_DSA_PUBLIC_MAGIC, PBCRYPT_DSA_KEY_BLOB_V2, PBCRYPT_DSA_KEY_BLOB_V2 structure pointer [Security], bcrypt/BCRYPT_DSA_KEY_BLOB_V2, bcrypt/PBCRYPT_DSA_KEY_BLOB_V2, security.bcrypt_dsa_key_blob_v2"
ms.topic: struct
req.header: bcrypt.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bcrypt.h
api_name:
 - BCRYPT_DSA_KEY_BLOB_V2
product: Windows
targetos: Windows
req.typenames: BCRYPT_DSA_KEY_BLOB_V2, *PBCRYPT_DSA_KEY_BLOB_V2
req.redist: 
---

# BCRYPT_DSA_KEY_BLOB_V2 structure


## -description


The <b>BCRYPT_DSA_KEY_BLOB_V2</b> structure is used as a header for a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Digital Signature Algorithm</a> (DSA) <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> or <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> in memory.


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


### -field hashAlgorithm

A <a href="https://msdn.microsoft.com/en-us/library/JJ670565(v=VS.85).aspx">HASHALGORITHM_ENUM</a> enumeration value that specifies the hashing algorithm to use.


### -field standardVersion

A <a href="https://msdn.microsoft.com/en-us/library/JJ670564(v=VS.85).aspx">DSAFIPSVERSION_ENUM</a> enumeration value that specifies the Federal Information Processing Standard(FIPS) to apply.


### -field cbSeedLength

Length of the seed used to generate the prime number q.


### -field cbGroupSize

Size of the prime number q . Currently, if the key is less than 128 bits, q is 20 bytes long. If the key exceeds 256 bits, q is 32 bytes long.


### -field Count

The number of iterations performed to generate the prime number q from the seed. For more information, see NIST standard FIPS186-3.


## -remarks



The structure applies to DSA keys that exceed 1024 bits in length but are less  than or equal to 3072 bits.

This structure is used as a header for a larger buffer. A DSA <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key BLOB</a> (BCRYPT_DSA_PUBLIC_BLOB) has the following format in contiguous memory. The Modulus, Generator, and Public numbers are in big-endian format.

<pre class="syntax" xml:space="preserve"><code>
BCRYPT_DSA_KEY_BLOB_V2
Modulus[cbKey]     // Big-endian.
Generator[cbKey]   // Big-endian.
Public[cbKey]      // Big-endian.
</code></pre>
A DSA <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key BLOB</a> (BCRYPT_DSA_PRIVATE_BLOB) has the following format in contiguous memory. The Modulus, Generator, Public, and PrivateExponent numbers are in big-endian format.

<pre class="syntax" xml:space="preserve"><code>
BCRYPT_DSA_KEY_BLOB_V2
Modulus[cbKey]         // Big-endian.
Generator[cbKey]       // Big-endian.
Public[cbKey]          // Big-endian.
PrivateExponent[20]    // Big-endian.
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/a5d73143-c1d6-43b3-a724-7e27c68a5ade">BCryptExportKey</a>



<a href="https://msdn.microsoft.com/6b9683f4-10f2-40e4-9757-a1f01991bef7">BCryptImportKey</a>
 

 

