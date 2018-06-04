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

# _BCRYPT_DH_KEY_BLOB structure


## -description


The <b>BCRYPT_DH_KEY_BLOB</b> structure is used as a header for a Diffie-Hellman <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> or <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> in memory.


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



This structure is used as a header for a larger buffer. A Diffie-Hellman <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key BLOB</a> (BCRYPT_DH_PUBLIC_BLOB) has the following format in contiguous memory. The Modulus, Generator, and Public numbers are in big-endian format.

<pre class="syntax" xml:space="preserve"><code>
BCRYPT_DH_KEY_BLOB
Modulus[cbKey] // Big-endian.
Generator[cbKey] // Big-endian.
Public[cbKey] // Big-endian.
</code></pre>
A Diffie-Hellman <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key BLOB</a> (BCRYPT_DH_PRIVATE_BLOB) has the following format in contiguous memory. The Modulus, Generator, Public, and PrivateExponent numbers are in big-endian format.

<pre class="syntax" xml:space="preserve"><code>
BCRYPT_DH_KEY_BLOB
Modulus[cbKey] // Big-endian.
Generator[cbKey] // Big-endian.
Public[cbKey] // Big-endian.
PrivateExponent[cbKey] // Big-endian.
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/a5d73143-c1d6-43b3-a724-7e27c68a5ade">BCryptExportKey</a>



<a href="https://msdn.microsoft.com/6b9683f4-10f2-40e4-9757-a1f01991bef7">BCryptImportKey</a>
 

 

