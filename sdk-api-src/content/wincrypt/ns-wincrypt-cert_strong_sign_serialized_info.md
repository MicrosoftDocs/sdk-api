---
UID: NS:wincrypt._CERT_STRONG_SIGN_SERIALIZED_INFO
title: CERT_STRONG_SIGN_SERIALIZED_INFO (wincrypt.h)
description: Contains the signature algorithm/hash algorithm and public key algorithm/bit length pairs that can be used for strong signing.
helpviewer_keywords: ["*PCERT_STRONG_SIGN_SERIALIZED_INFO","CERT_STRONG_SIGN_ENABLE_CRL_CHECK","CERT_STRONG_SIGN_ENABLE_OCSP_CHECK","CERT_STRONG_SIGN_SERIALIZED_INFO","CERT_STRONG_SIGN_SERIALIZED_INFO structure [Security]","PCERT_STRONG_SIGN_SERIALIZED_INFO","PCERT_STRONG_SIGN_SERIALIZED_INFO structure pointer [Security]","security.cert_strong_sign_serialized_info","wincrypt/CERT_STRONG_SIGN_SERIALIZED_INFO","wincrypt/PCERT_STRONG_SIGN_SERIALIZED_INFO"]
old-location: security\cert_strong_sign_serialized_info.htm
tech.root: security
ms.assetid: B89CDF67-4620-47B2-8363-717D284368FD
ms.date: 12/05/2018
ms.keywords: '*PCERT_STRONG_SIGN_SERIALIZED_INFO, CERT_STRONG_SIGN_ENABLE_CRL_CHECK, CERT_STRONG_SIGN_ENABLE_OCSP_CHECK, CERT_STRONG_SIGN_SERIALIZED_INFO, CERT_STRONG_SIGN_SERIALIZED_INFO structure [Security], PCERT_STRONG_SIGN_SERIALIZED_INFO, PCERT_STRONG_SIGN_SERIALIZED_INFO structure pointer [Security], security.cert_strong_sign_serialized_info, wincrypt/CERT_STRONG_SIGN_SERIALIZED_INFO, wincrypt/PCERT_STRONG_SIGN_SERIALIZED_INFO'
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
targetos: Windows
req.typenames: CERT_STRONG_SIGN_SERIALIZED_INFO, *PCERT_STRONG_SIGN_SERIALIZED_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_STRONG_SIGN_SERIALIZED_INFO
 - wincrypt/_CERT_STRONG_SIGN_SERIALIZED_INFO
 - PCERT_STRONG_SIGN_SERIALIZED_INFO
 - wincrypt/PCERT_STRONG_SIGN_SERIALIZED_INFO
 - CERT_STRONG_SIGN_SERIALIZED_INFO
 - wincrypt/CERT_STRONG_SIGN_SERIALIZED_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_STRONG_SIGN_SERIALIZED_INFO
---

# CERT_STRONG_SIGN_SERIALIZED_INFO structure


## -description

Contains the <i>signature algorithm</i>/<i>hash algorithm</i> and <i>public key algorithm</i>/<i>bit length</i> pairs that can be used for strong signing. This structure is used by the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_strong_sign_para">CERT_STRONG_SIGN_PARA</a> structure.

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

This structure is used by the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_strong_sign_para">CERT_STRONG_SIGN_PARA</a> structure which is directly referenced by the following functions:

<ul>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certisstronghashtosign">CertIsStrongHashToSign</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcontrol">CryptMsgControl</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencodedex">CryptMsgVerifyCountersignatureEncodedEx</a>
</li>
</ul>
Also, <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_strong_sign_para">CERT_STRONG_SIGN_PARA</a> is indirectly referenced by the following:

<ul>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodemessage">CryptDecodeMessage</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecryptandverifymessagesignature">CryptDecryptAndVerifyMessageSignature</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain">CertGetCertificateChain</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certselectcertificatechains">CertSelectCertificateChains</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifydetachedmessagesignature">CryptVerifyDetachedMessageSignature</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifymessagesignature">CryptVerifyMessageSignature</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_strong_sign_para">CERT_STRONG_SIGN_PARA</a>