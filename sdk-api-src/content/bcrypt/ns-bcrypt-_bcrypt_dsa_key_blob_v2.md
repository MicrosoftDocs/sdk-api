---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _BCRYPT_DSA_KEY_BLOB_V2 structure


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

A <a href="https://msdn.microsoft.com/482DA4B6-EC1C-4E88-95C0-62ED1356DC3B">HASHALGORITHM_ENUM</a> enumeration value that specifies the hashing algorithm to use.


### -field standardVersion

A <a href="https://msdn.microsoft.com/6797D7C0-3451-464E-9261-61217ADAB9C1">DSAFIPSVERSION_ENUM</a> enumeration value that specifies the Federal Information Processing Standard(FIPS) to apply.


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
 

 

