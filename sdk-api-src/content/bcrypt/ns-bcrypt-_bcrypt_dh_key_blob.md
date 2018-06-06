---
UID: NS:bcrypt._BCRYPT_DH_KEY_BLOB
title: "_BCRYPT_DH_KEY_BLOB"
author: windows-sdk-content
description: Used as a header for a Diffie-Hellman public key or private key BLOB in memory.
old-location: security\bcrypt_dh_key_blob.htm
old-project: SecCNG
ms.assetid: 6004b2e5-7e06-4108-a0da-472b9b6d5fea
ms.author: windowssdkdev
ms.date: 05/01/2018
ms.keywords: "*PBCRYPT_DH_KEY_BLOB, BCRYPT_DH_KEY_BLOB, BCRYPT_DH_KEY_BLOB structure [Security], BCRYPT_DH_PRIVATE_MAGIC, BCRYPT_DH_PUBLIC_MAGIC, PBCRYPT_DH_KEY_BLOB, PBCRYPT_DH_KEY_BLOB structure pointer [Security], _BCRYPT_DH_KEY_BLOB, bcrypt/BCRYPT_DH_KEY_BLOB, bcrypt/PBCRYPT_DH_KEY_BLOB, security.bcrypt_dh_key_blob"
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
tech.root: 
req.typenames: BCRYPT_DH_KEY_BLOB, *PBCRYPT_DH_KEY_BLOB
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bcrypt.h
api_name:
 - BCRYPT_DH_KEY_BLOB
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

