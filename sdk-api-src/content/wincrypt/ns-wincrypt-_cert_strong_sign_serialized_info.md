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

# _CERT_STRONG_SIGN_SERIALIZED_INFO structure


## -description


Contains the <i>signature algorithm</i>/<i>hash algorithm</i> and <i>public key algorithm</i>/<i>bit length</i> pairs that can be used for strong signing. This structure is used by the <a href="https://msdn.microsoft.com/12D9F82C-F484-43B0-BD55-F07321058671">CERT_STRONG_SIGN_PARA</a> structure.


## -struct-fields




### -field dwFlags

By default, certificate strong signing parameters do not apply to certificate revocation lists (CRLs) or online certificate status protocol (OCSP) responses. You can set one or both of the following values to enable strong signing on CRLs and OCSP responses.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_STRONG_SIGN_ENABLE_CRL_CHECK"></a><a id="cert_strong_sign_enable_crl_check"></a><dl>
<dt><b>CERT_STRONG_SIGN_ENABLE_CRL_CHECK</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Enable strong signing of CRLs.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STRONG_SIGN_ENABLE_OCSP_CHECK"></a><a id="cert_strong_sign_enable_ocsp_check"></a><dl>
<dt><b>CERT_STRONG_SIGN_ENABLE_OCSP_CHECK</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
Enable strong signing of OCSP responses.

</td>
</tr>
</table>
 


### -field pwszCNGSignHashAlgids

Pointer to a null-terminated Unicode string that contains a set of <i>signature algorithm</i>/<i>hash algorithm</i> pairs. A Unicode semicolon (L";") separates the pairs. This is shown by the following example.

<code>L"RSA/SHA256;RSA/SHA384;ECDSA/SHA256;ECDSA/SHA384"</code>

The following signature algorithms are supported:<ul>
<li>L"RSA" (BCRYPT_RSA_ALGORITHM)</li>
<li>L"DSA" (BCRYPT_DSA_ALGORITHM)</li>
<li>L"ECDSA" (SSL_ECDSA_ALGORITHM)</li>
</ul>


The following signature algorithms are not supported:<ul>
<li>L"ECDSA_P256" (BCRYPT_ECDSA_P256_ALGORITHM)</li>
<li>L"ECDSA_P384" (BCRYPT_ECDSA_P384_ALGORITHM)</li>
<li>L"ECDSA_P521" (BCRYPT_ECDSA_P521_ALGORITHM)</li>
</ul>


The following hash algorithms are supported:<ul>
<li>L"MD5" (BCRYPT_MD5_ALGORITHM)</li>
<li>L"SHA1" (BCRYPT_SHA1_ALGORITHM)</li>
<li>L"SHA256" (BCRYPT_SHA256_ALGORITHM)</li>
<li>L"SHA256" (BCRYPT_SHA256_ALGORITHM)</li>
<li>L"SHA512" (BCRYPT_SHA512_ALGORITHM)</li>
</ul>



### -field pwszCNGPubKeyMinBitLengths

Pointer to a null-terminated Unicode string that contains a set of <i>public key algorithm</i>/<i>bit length</i> pairs. A Unicode semicolon (L";") separates the pairs. This is shown by the following example.

<code>L”RSA/2048;ECDSA/256”</code>

The following public key algorithms are supported:<ul>
<li>L"RSA" (BCRYPT_RSA_ALGORITHM)</li>
<li>L"DSA" (BCRYPT_DSA_ALGORITHM)</li>
<li>L"ECDSA" (SSL_ECDSA_ALGORITHM)</li>
</ul>



## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/12D9F82C-F484-43B0-BD55-F07321058671">CERT_STRONG_SIGN_PARA</a> structure which is directly referenced by the following functions:

<ul>
<li>
<a href="https://msdn.microsoft.com/B498C1F0-1EFF-49AF-9CD4-A447F79256F1">CertIsStrongHashToSign</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a990d44d-2993-429f-b817-2a834105ecef">CryptMsgControl</a>
</li>
<li>
<a href="https://msdn.microsoft.com/da756cd5-1dec-4d88-9c90-76dd263035eb">CryptMsgVerifyCountersignatureEncodedEx</a>
</li>
</ul>
Also, <a href="https://msdn.microsoft.com/12D9F82C-F484-43B0-BD55-F07321058671">CERT_STRONG_SIGN_PARA</a> is indirectly referenced by the following:

<ul>
<li>
<a href="https://msdn.microsoft.com/25ffd058-8f75-4ba5-b075-e3efc09f5d9d">CryptDecodeMessage</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0864a187-617f-4a21-9809-d2dbbc54ab9c">CryptDecryptAndVerifyMessageSignature</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8c93036c-0b93-40d4-b0e3-ba1f2fc72db1">CertGetCertificateChain</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b740772b-d25b-4b3d-9acb-03f7018750d6">CertSelectCertificateChains</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d437f6bf-eb56-4d29-bb91-eb8487e50219">CryptVerifyDetachedMessageSignature</a>
</li>
<li>
<a href="https://msdn.microsoft.com/03411e7a-b097-4059-a198-3d412ae40e38">CryptVerifyMessageSignature</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/12D9F82C-F484-43B0-BD55-F07321058671">CERT_STRONG_SIGN_PARA</a>
 

 

