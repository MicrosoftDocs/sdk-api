---
UID: NS:wincrypt._CERT_STRONG_SIGN_PARA
title: CERT_STRONG_SIGN_PARA (wincrypt.h)
description: Contains parameters used to check for strong signatures on certificates, certificate revocation lists (CRLs), online certificate status protocol (OCSP) responses, and PKCS
helpviewer_keywords: ["*PCERT_STRONG_SIGN_PARA","CERT_STRONG_SIGN_PARA","CERT_STRONG_SIGN_PARA structure [Security]","PCCERT_STRONG_SIGN_PARA","PCCERT_STRONG_SIGN_PARA structure pointer [Security]","PCERT_STRONG_SIGN_PARA","PCERT_STRONG_SIGN_PARA structure pointer [Security]","security.cert_strong_sign_para","szOID_CERT_STRONG_KEY_OS_1","szOID_CERT_STRONG_SIGN_OS_1","wincrypt/CERT_STRONG_SIGN_PARA","wincrypt/PCCERT_STRONG_SIGN_PARA","wincrypt/PCERT_STRONG_SIGN_PARA"]
old-location: security\cert_strong_sign_para.htm
tech.root: security
ms.assetid: 12D9F82C-F484-43B0-BD55-F07321058671
ms.date: 12/05/2018
ms.keywords: '*PCERT_STRONG_SIGN_PARA, CERT_STRONG_SIGN_PARA, CERT_STRONG_SIGN_PARA structure [Security], PCCERT_STRONG_SIGN_PARA, PCCERT_STRONG_SIGN_PARA structure pointer [Security], PCERT_STRONG_SIGN_PARA, PCERT_STRONG_SIGN_PARA structure pointer [Security], security.cert_strong_sign_para, szOID_CERT_STRONG_KEY_OS_1, szOID_CERT_STRONG_SIGN_OS_1, wincrypt/CERT_STRONG_SIGN_PARA, wincrypt/PCCERT_STRONG_SIGN_PARA, wincrypt/PCERT_STRONG_SIGN_PARA'
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
req.typenames: CERT_STRONG_SIGN_PARA, *PCERT_STRONG_SIGN_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_STRONG_SIGN_PARA
 - wincrypt/_CERT_STRONG_SIGN_PARA
 - PCERT_STRONG_SIGN_PARA
 - wincrypt/PCERT_STRONG_SIGN_PARA
 - CERT_STRONG_SIGN_PARA
 - wincrypt/CERT_STRONG_SIGN_PARA
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
 - CERT_STRONG_SIGN_PARA
---

# CERT_STRONG_SIGN_PARA structure


## -description

Contains parameters used to check for strong signatures on <a href="/windows/desktop/SecGloss/c-gly">certificates</a>, <a href="/windows/desktop/SecGloss/c-gly">certificate revocation lists</a> (CRLs), <a href="/windows/desktop/SecGloss/o-gly">online certificate status protocol</a> (OCSP) responses, and <a href="/windows/desktop/SecGloss/p-gly">PKCS #7</a> messages.

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

Pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_strong_sign_serialized_info">CERT_STRONG_SIGN_SERIALIZED_INFO</a> structure that specifies the parameters.

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
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certisstronghashtosign">CertIsStrongHashToSign</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcontrol">CryptMsgControl</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencodedex">CryptMsgVerifyCountersignatureEncodedEx</a>
</li>
</ul>
The <b>CERT_STRONG_SIGN_PARA</b> structure is also directly referenced by the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_verify_message_para">CRYPT_VERIFY_MESSAGE_PARA</a> structure and is therefore available for use by the following functions:

<ul>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodemessage">CryptDecodeMessage</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecryptandverifymessagesignature">CryptDecryptAndVerifyMessageSignature</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifydetachedmessagesignature">CryptVerifyDetachedMessageSignature</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifymessagesignature">CryptVerifyMessageSignature</a>
</li>
</ul>
Finally, the <b>CERT_STRONG_SIGN_PARA</b> structure is directly referenced by the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para">CERT_CHAIN_PARA</a> structure and is therefore available for use by the following functions:

<ul>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain">CertGetCertificateChain</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certselectcertificatechains">CertSelectCertificateChains</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_strong_sign_serialized_info">CERT_STRONG_SIGN_SERIALIZED_INFO</a>