---
UID: NS:wincrypt._CRYPT_KEY_SIGN_MESSAGE_PARA
title: CRYPT_KEY_SIGN_MESSAGE_PARA (wincrypt.h)
description: Contains information about the cryptographic service provider (CSP) and algorithms used to sign a message.
helpviewer_keywords: ["*PCRYPT_KEY_SIGN_MESSAGE_PARA","AT_KEYEXCHANGE","AT_SIGNATURE","CRYPT_KEY_SIGN_MESSAGE_PARA","CRYPT_KEY_SIGN_MESSAGE_PARA structure [Security]","PCRYPT_KEY_SIGN_MESSAGE_PARA","PCRYPT_KEY_SIGN_MESSAGE_PARA structure pointer [Security]","PKCS_7_ASN_ENCODING","X509_ASN_ENCODING","security.crypt_key_sign_message_para","wincrypt/CRYPT_KEY_SIGN_MESSAGE_PARA","wincrypt/PCRYPT_KEY_SIGN_MESSAGE_PARA"]
old-location: security\crypt_key_sign_message_para.htm
tech.root: security
ms.assetid: d5426ad6-2181-42ce-99f2-cc6cc83e20a8
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_KEY_SIGN_MESSAGE_PARA, AT_KEYEXCHANGE, AT_SIGNATURE, CRYPT_KEY_SIGN_MESSAGE_PARA, CRYPT_KEY_SIGN_MESSAGE_PARA structure [Security], PCRYPT_KEY_SIGN_MESSAGE_PARA, PCRYPT_KEY_SIGN_MESSAGE_PARA structure pointer [Security], PKCS_7_ASN_ENCODING, X509_ASN_ENCODING, security.crypt_key_sign_message_para, wincrypt/CRYPT_KEY_SIGN_MESSAGE_PARA, wincrypt/PCRYPT_KEY_SIGN_MESSAGE_PARA'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: CRYPT_KEY_SIGN_MESSAGE_PARA, *PCRYPT_KEY_SIGN_MESSAGE_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_KEY_SIGN_MESSAGE_PARA
 - wincrypt/_CRYPT_KEY_SIGN_MESSAGE_PARA
 - PCRYPT_KEY_SIGN_MESSAGE_PARA
 - wincrypt/PCRYPT_KEY_SIGN_MESSAGE_PARA
 - CRYPT_KEY_SIGN_MESSAGE_PARA
 - wincrypt/CRYPT_KEY_SIGN_MESSAGE_PARA
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
 - CRYPT_KEY_SIGN_MESSAGE_PARA
---

# CRYPT_KEY_SIGN_MESSAGE_PARA structure


## -description

The <b>CRYPT_KEY_SIGN_MESSAGE_PARA</b> structure contains information about the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) and algorithms used to sign a message.

## -struct-fields

### -field cbSize

The size, in bytes, of this data structure.

### -field dwMsgAndCertEncodingType

Specifies the type of message and certificate encoding used. This can be a combination of one or more of the following values.
					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="X509_ASN_ENCODING"></a><a id="x509_asn_encoding"></a><dl>
<dt><b>X509_ASN_ENCODING</b></dt>
</dl>
</td>
<td width="60%">
Specifies <a href="/windows/desktop/SecGloss/x-gly">X.509</a> certificate encoding.

</td>
</tr>
<tr>
<td width="40%"><a id="PKCS_7_ASN_ENCODING"></a><a id="pkcs_7_asn_encoding"></a><dl>
<dt><b>PKCS_7_ASN_ENCODING</b></dt>
</dl>
</td>
<td width="60%">
Specifies PKCS 7 message encoding.

</td>
</tr>
</table>

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.hCryptProv

The handle of the CSP to use to sign the message. The <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a> function is called to obtain this handle.

### -field DUMMYUNIONNAME.hNCryptKey

The handle of the Cryptography API: Next Generation (CNG) CSP to use to sign the message. CNG signature algorithms are only supported in CNG functions.

### -field dwKeySpec

Identifies the type of <a href="/windows/desktop/SecGloss/p-gly">private key</a> to use to sign the message. This must be one of the following values. This member is ignored if a CNG key is passed in the <i>hNCryptKey</i> member.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AT_KEYEXCHANGE"></a><a id="at_keyexchange"></a><dl>
<dt><b>AT_KEYEXCHANGE</b></dt>
</dl>
</td>
<td width="60%">
Use the key exchange key.

</td>
</tr>
<tr>
<td width="40%"><a id="AT_SIGNATURE"></a><a id="at_signature"></a><dl>
<dt><b>AT_SIGNATURE</b></dt>
</dl>
</td>
<td width="60%">
Use the digital signature key.

</td>
</tr>
</table>

### -field HashAlgorithm

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that specifies the algorithm to use to generate the hash of the message. This must be a hash algorithm.

### -field pvHashAuxInfo

This member is not used and must be set to <b>NULL</b>.

### -field PubKeyAlgorithm

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that specifies the algorithm to use to sign the message. This must be either a public key or a signature algorithm.