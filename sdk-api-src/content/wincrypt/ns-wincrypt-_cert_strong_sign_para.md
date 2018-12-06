---
UID: NS:wincrypt._CERT_STRONG_SIGN_PARA
title: "_CERT_STRONG_SIGN_PARA"
author: windows-sdk-content
description: Contains parameters used to check for strong signatures on certificates, certificate revocation lists (CRLs), online certificate status protocol (OCSP) responses, and PKCS #7 messages.
old-location: security\cert_strong_sign_para.htm
tech.root: seccrypto
ms.assetid: 12D9F82C-F484-43B0-BD55-F07321058671
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCERT_STRONG_SIGN_PARA, CERT_STRONG_SIGN_PARA, CERT_STRONG_SIGN_PARA structure [Security], PCCERT_STRONG_SIGN_PARA, PCCERT_STRONG_SIGN_PARA structure pointer [Security], PCERT_STRONG_SIGN_PARA, PCERT_STRONG_SIGN_PARA structure pointer [Security], _CERT_STRONG_SIGN_PARA, security.cert_strong_sign_para, szOID_CERT_STRONG_KEY_OS_1, szOID_CERT_STRONG_SIGN_OS_1, wincrypt/CERT_STRONG_SIGN_PARA, wincrypt/PCCERT_STRONG_SIGN_PARA, wincrypt/PCERT_STRONG_SIGN_PARA"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wincrypt.h
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
 - Wincrypt.h
api_name:
 - CERT_STRONG_SIGN_PARA
product: Windows
targetos: Windows
req.typenames: CERT_STRONG_SIGN_PARA, *PCERT_STRONG_SIGN_PARA
req.redist: 
---

# _CERT_STRONG_SIGN_PARA structure


## -description


Contains parameters used to check for strong signatures on <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificates</a>, <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation lists</a> (CRLs), <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">online certificate status protocol</a> (OCSP) responses, and <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">PKCS #7</a> messages.


## -struct-fields




### -field cbSize

Size, in bytes, of this structure.


### -field dwInfoChoice

Indicates which nested union member points to the strong signature information. This can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>CERT_STRONG_SIGN_SERIALIZED_INFO_CHOICE</b></td>
<td>
Specifies the <b>pSerializedInfo</b> member.

</td>
</tr>
<tr>
<td><b>CERT_STRONG_SIGN_OID_INFO_CHOICE</b></td>
<td>
Specifies the <b>pszOID</b> member.

</td>
</tr>
</table>
 


### -field DUMMYUNIONNAME

Union that contains the parameters that can be used for checking whether a signature is strong. The parameters consist of <i>signature algorithm</i> / <i>hash algorithm</i> pairs and <i>public key algorithm</i> / <i>bit length</i> pairs.


### -field DUMMYUNIONNAME.pvInfo

Reserved.


### -field DUMMYUNIONNAME.pSerializedInfo

Pointer to a <a href="https://msdn.microsoft.com/B89CDF67-4620-47B2-8363-717D284368FD">CERT_STRONG_SIGN_SERIALIZED_INFO</a> structure that specifies the parameters.


### -field DUMMYUNIONNAME.pszOID

Pointer to a string that contains an object identifier (OID) that represents predefined parameters that can be used for strong signature checking. This can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="szOID_CERT_STRONG_SIGN_OS_1"></a><a id="szoid_cert_strong_sign_os_1"></a><a id="SZOID_CERT_STRONG_SIGN_OS_1"></a><dl>
<dt><b>szOID_CERT_STRONG_SIGN_OS_1</b></dt>
<dt>"1.3.6.1.4.1.311.72.1.1"</dt>
</dl>
</td>
<td width="60%">
The SHA2 hash algorithm is supported. MD2, MD4, MD5, and SSHA1 are not supported.

The signing and public key algorithms can be RSA or ECDSA. The DSA algorithm is not supported. The key size for the RSA algorithm must equal or be greater than 2047 bits. The key size for the ECDSA algorithm must equal or be greater than 256 bits. 

Strong signing of CRLs and OCSP responses are enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_CERT_STRONG_KEY_OS_1"></a><a id="szoid_cert_strong_key_os_1"></a><a id="SZOID_CERT_STRONG_KEY_OS_1"></a><dl>
<dt><b>szOID_CERT_STRONG_KEY_OS_1</b></dt>
<dt>"1.3.6.1.4.1.311.72.2.1"</dt>
</dl>
</td>
<td width="60%">
SHA1 and SHA2 hashes are supported. MD2, MD4, and MD5 are not.

The signing and public key algorithms can be RSA or ECDSA. The DSA algorithm is not supported. The key size for the RSA algorithm must equal or be greater than 2047 bits. The key size for the ECDSA algorithm must equal or be greater than 256 bits. 

Strong signing of CRLs and OCSP responses are enabled.

</td>
</tr>
</table>
 


## -remarks



The parameters needed to check for a strong signature include the following:

<ul>
<li>Name of the public (asymmetric) algorithm</li>
<li>Size, in bits, of the public key</li>
<li>Name of the signature algorithm</li>
<li>Name of the hashing algorithm</li>
</ul>
The value you specify for the <b>dwInfoChoice</b> member   of this structure chooses whether the parameters are transmitted as serialized strings or are predefined by using an object identifier.

The <b>CERT_STRONG_SIGN_PARA</b> structure is directly referenced by the following functions:

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
The <b>CERT_STRONG_SIGN_PARA</b> structure is also directly referenced by the <a href="https://msdn.microsoft.com/bbd56b5e-2bbe-420f-8842-1be50dca779f">CRYPT_VERIFY_MESSAGE_PARA</a> structure and is therefore available for use by the following functions:

<ul>
<li>
<a href="https://msdn.microsoft.com/25ffd058-8f75-4ba5-b075-e3efc09f5d9d">CryptDecodeMessage</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0864a187-617f-4a21-9809-d2dbbc54ab9c">CryptDecryptAndVerifyMessageSignature</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d437f6bf-eb56-4d29-bb91-eb8487e50219">CryptVerifyDetachedMessageSignature</a>
</li>
<li>
<a href="https://msdn.microsoft.com/03411e7a-b097-4059-a198-3d412ae40e38">CryptVerifyMessageSignature</a>
</li>
</ul>
Finally, the <b>CERT_STRONG_SIGN_PARA</b> structure is directly referenced by the <a href="https://msdn.microsoft.com/86094e1c-be59-4a15-a05b-21769f80e653">CERT_CHAIN_PARA</a> structure and is therefore available for use by the following functions:

<ul>
<li>
<a href="https://msdn.microsoft.com/8c93036c-0b93-40d4-b0e3-ba1f2fc72db1">CertGetCertificateChain</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b740772b-d25b-4b3d-9acb-03f7018750d6">CertSelectCertificateChains</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/B89CDF67-4620-47B2-8363-717D284368FD">CERT_STRONG_SIGN_SERIALIZED_INFO</a>
 

 

