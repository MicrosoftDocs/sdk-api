---
UID: NS:wincrypt._CMSG_SIGNER_ENCODE_INFO
title: CMSG_SIGNER_ENCODE_INFO (wincrypt.h)
description: Contains signer information. It is passed to CryptMsgCountersign, CryptMsgCountersignEncoded, and optionally to CryptMsgOpenToEncode as a member of the CMSG_SIGNED_ENCODE_INFO structure, if the dwMsgType parameter is CMSG_SIGNED.
helpviewer_keywords: ["*PCMSG_SIGNER_ENCODE_INFO","AT_KEYEXCHANGE","AT_SIGNATURE","CMSG_SIGNER_ENCODE_INFO","CMSG_SIGNER_ENCODE_INFO structure [Security]","PCMSG_SIGNER_ENCODE_INFO","PCMSG_SIGNER_ENCODE_INFO structure pointer [Security]","_crypto2_cmsg_signer_encode_info","security.cmsg_signer_encode_info","wincrypt/CMSG_SIGNER_ENCODE_INFO","wincrypt/PCMSG_SIGNER_ENCODE_INFO"]
old-location: security\cmsg_signer_encode_info.htm
tech.root: security
ms.assetid: f599226d-ddd7-455f-b650-74b91674d8f9
ms.date: 12/05/2018
ms.keywords: '*PCMSG_SIGNER_ENCODE_INFO, AT_KEYEXCHANGE, AT_SIGNATURE, CMSG_SIGNER_ENCODE_INFO, CMSG_SIGNER_ENCODE_INFO structure [Security], PCMSG_SIGNER_ENCODE_INFO, PCMSG_SIGNER_ENCODE_INFO structure pointer [Security], _crypto2_cmsg_signer_encode_info, security.cmsg_signer_encode_info, wincrypt/CMSG_SIGNER_ENCODE_INFO, wincrypt/PCMSG_SIGNER_ENCODE_INFO'
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
req.typenames: CMSG_SIGNER_ENCODE_INFO, *PCMSG_SIGNER_ENCODE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMSG_SIGNER_ENCODE_INFO
 - wincrypt/_CMSG_SIGNER_ENCODE_INFO
 - PCMSG_SIGNER_ENCODE_INFO
 - wincrypt/PCMSG_SIGNER_ENCODE_INFO
 - CMSG_SIGNER_ENCODE_INFO
 - wincrypt/CMSG_SIGNER_ENCODE_INFO
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
 - CMSG_SIGNER_ENCODE_INFO
---

# CMSG_SIGNER_ENCODE_INFO structure


## -description

The <b>CMSG_SIGNER_ENCODE_INFO</b> structure contains signer information. It is passed to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcountersign">CryptMsgCountersign</a>, 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcountersignencoded">CryptMsgCountersignEncoded</a>, and optionally to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a> as a member of 
the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signed_encode_info">CMSG_SIGNED_ENCODE_INFO</a> structure, if the <i>dwMsgType</i> parameter is CMSG_SIGNED.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field pCertInfo

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a> structure that contains the  


<b>Issuer</b>, <b>SerialNumber</b>, and <b>SubjectPublicKeyInfo</b> members.

The <b>pbData</b> members of the <b>Issuer</b> and <b>SerialNumber</b> structures combined uniquely identify a certificate. The <b>Algorithm</b> member of the <b>SubjectPublicKeyInfo</b> structure specifies the <a href="/windows/desktop/SecGloss/h-gly">hash</a> encryption algorithm used.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.hCryptProv

A handle to the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP).
If <b>HashEncryptionAlgorithm</b> is set to szOID_PKIX_NO_SIGNATURE, this handle can be the handle of a CSP acquired by using the <i>dwFlags</i> parameter set to <b>CRYPT_VERIFYCONTEXT</b>. The CNG function <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptiskeyhandle">NCryptIsKeyHandle</a> is called to determine the union choice.

### -field DUMMYUNIONNAME.hNCryptKey

A handle to the CNG CSP. The CNG function <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptiskeyhandle">NCryptIsKeyHandle</a> is called to determine the union choice. New encrypt algorithms are only supported in CNG functions. The CNG function <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncrypttranslatehandle">NCryptTranslateHandle</a> will be called to convert the CryptoAPI <i>hCryptProv</i> choice where necessary. We recommend that applications pass, to the <i>hNCryptKey</i> member, the CNG CSP handle that is returned from the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptopenkey">NCryptOpenKey</a> function.

### -field DUMMYUNIONNAME.hBCryptKey

### -field dwKeySpec

Specifies the private key to be used. This member is not used when the <i>hNCryptKey</i> member is used. 




If <b>dwKeySpec</b> is zero, then the default AT_KEYEXCHANGE value is used.

The following <b>dwKeySpec</b> values are defined for the default provider.

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
Keys used to encrypt/decrypt session keys.

</td>
</tr>
<tr>
<td width="40%"><a id="AT_SIGNATURE"></a><a id="at_signature"></a><dl>
<dt><b>AT_SIGNATURE</b></dt>
</dl>
</td>
<td width="60%">
Keys used to create and verify digital signatures.

</td>
</tr>
</table>

### -field HashAlgorithm

A 
						<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that specifies the hash algorithm.

### -field pvHashAuxInfo

Not used. This member must be set to <b>NULL</b>.

### -field cAuthAttr

The number of elements in the <b>rgAuthAttr</b> array. If no authenticated attributes are present in <b>rgAuthAttr</b>, then <b>cAuthAttr</b> is zero.

### -field rgAuthAttr

An array of pointers to 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute">CRYPT_ATTRIBUTE</a> structures, each of which contains authenticated attribute information. 




The PKCS #9 standard dictates that if there are any attributes, there must be at least two: the content type <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and the hash of the message. These attributes are automatically added by the system.

### -field cUnauthAttr

The number of elements in the <b>rgUnauthAttr</b> array. If there are no unauthenticated attributes, <b>cUnauthAttr</b> is zero.

### -field rgUnauthAttr

An array of pointers to <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute">CRYPT_ATTRIBUTE</a> structures, each of which contains unauthenticated attribute information. Unauthenticated attributes can contain <a href="/windows/desktop/SecGloss/c-gly">countersignatures</a>, among other uses.

### -field SignerId

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_id">CERT_ID</a> structure that contains a unique identifier of the signer's certificate. This member can optionally be used with PKCS #7 with Cryptographic Message Syntax (CMS). If this member is not <b>NULL</b> and its <b>dwIdChoice</b> member is not zero, it is used to identify  the certificate instead of the <b>Issuer</b> and <b>SerialNumber</b> members of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a> structure pointed to by <b>pCertInfo</b>.
						CMS supports the KEY_IDENTIFIER and ISSUER_SERIAL_NUMBER CERT_ID structures. PKCS version 1.5 supports only the ISSUER_SERIAL_NUMBER CERT_ID choice. This member is  used with CMS for PKCS #7 processing and can be used only if CMSG_SIGNER_ENCODE_INFO_HAS_CMS_FIELDS is defined.

### -field HashEncryptionAlgorithm

A 
						<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure optionally used with PKCS #7 with CMS. If this member is not <b>NULL</b>, the algorithm identified is used instead of the SubjectPublicKeyInfo.Algorithm algorithm.
If this member is set to szOID_PKIX_NO_SIGNATURE, the signature value contains only the hash octets. 

For RSA, the <a href="/windows/desktop/SecGloss/h-gly">hash</a> encryption algorithm is normally the same as the public key algorithm. For DSA, the hash encryption algorithm is normally a DSS signature algorithm.

This member is  used with CMS for PKCS #7 processing and can be used only if CMSG_SIGNER_ENCODE_INFO_HAS_CMS_FIELDS is defined.

### -field pvHashEncryptionAuxInfo

This member is not used. This member must be set to <b>NULL</b> if it is present in the data structure.
This member is present only if CMSG_SIGNER_ENCODE_INFO_HAS_CMS_FIELDS is defined.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute">CRYPT_ATTRIBUTE</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcontrol">CryptMsgControl</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcountersign">CryptMsgCountersign</a>