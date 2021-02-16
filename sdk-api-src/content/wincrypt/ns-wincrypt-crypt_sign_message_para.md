---
UID: NS:wincrypt._CRYPT_SIGN_MESSAGE_PARA
title: CRYPT_SIGN_MESSAGE_PARA (wincrypt.h)
description: The CRYPT_SIGN_MESSAGE_PARA structure contains information for signing messages using a specified signing certificate context.
helpviewer_keywords: ["*PCRYPT_SIGN_MESSAGE_PARA","CRYPT_SIGN_MESSAGE_PARA","CRYPT_SIGN_MESSAGE_PARA structure [Security]","PCRYPT_SIGN_MESSAGE_PARA","PCRYPT_SIGN_MESSAGE_PARA structure pointer [Security]","_crypto2_crypt_sign_message_para","security.crypt_sign_message_para","wincrypt/CRYPT_SIGN_MESSAGE_PARA","wincrypt/PCRYPT_SIGN_MESSAGE_PARA"]
old-location: security\crypt_sign_message_para.htm
tech.root: security
ms.assetid: 1601d860-6054-4650-a033-ea088655b7e4
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_SIGN_MESSAGE_PARA, CRYPT_SIGN_MESSAGE_PARA, CRYPT_SIGN_MESSAGE_PARA structure [Security], PCRYPT_SIGN_MESSAGE_PARA, PCRYPT_SIGN_MESSAGE_PARA structure pointer [Security], _crypto2_crypt_sign_message_para, security.crypt_sign_message_para, wincrypt/CRYPT_SIGN_MESSAGE_PARA, wincrypt/PCRYPT_SIGN_MESSAGE_PARA'
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
req.typenames: CRYPT_SIGN_MESSAGE_PARA, *PCRYPT_SIGN_MESSAGE_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_SIGN_MESSAGE_PARA
 - wincrypt/_CRYPT_SIGN_MESSAGE_PARA
 - PCRYPT_SIGN_MESSAGE_PARA
 - wincrypt/PCRYPT_SIGN_MESSAGE_PARA
 - CRYPT_SIGN_MESSAGE_PARA
 - wincrypt/CRYPT_SIGN_MESSAGE_PARA
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
 - CRYPT_SIGN_MESSAGE_PARA
---

# CRYPT_SIGN_MESSAGE_PARA structure


## -description

The <b>CRYPT_SIGN_MESSAGE_PARA</b> structure contains information for signing messages using a specified signing <a href="/windows/desktop/SecGloss/c-gly">certificate context</a>.

## -struct-fields

### -field cbSize

Size of this structure in bytes.

### -field dwMsgEncodingType

Type of encoding used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -field pSigningCert

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> to be used in the signing.

Either the CERT_KEY_PROV_INFO_PROP_ID, or CERT_KEY_CONTEXT_PROP_ID property must be set for the context to provide access to the <a href="/windows/desktop/SecGloss/p-gly">private signature key</a>.

### -field HashAlgorithm

CRYPT_ALGORITHM_IDENTIFIER containing the hashing algorithm used to hash the data to be signed.

### -field pvHashAuxInfo

Not currently used, and must be set to <b>NULL</b>.

### -field cMsgCert

Number of elements in the <b>rgpMsgCert</b> array of 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structures. If set to zero no certificates are included in the signed message.

### -field rgpMsgCert

Array of pointers to <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structures to be included in the signed message. If the <b>pSigningCert</b> is to be included, a pointer to it must be in the <b>rgpMsgCert</b> array.

### -field cMsgCrl

Number of elements in the <b>rgpMsgCrl</b> array of pointers to 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a> structures. If set to zero, no <b>CRL_CONTEXT</b> structures are included in the signed message.

### -field rgpMsgCrl

Array of pointers to <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a> structures to be included in the signed message.

### -field cAuthAttr

Number of elements in the <b>rgAuthAttr</b> array. If no authenticated attributes are present in <b>rgAuthAttr</b>, this member is set to zero.

### -field rgAuthAttr

Array of pointers to 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute">CRYPT_ATTRIBUTE</a> structures, each holding authenticated attribute information. If there are authenticated attributes present, the PKCS #9 standard dictates that there must be at least two attributes present, the content type <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID), and the hash of the message itself. These attributes are automatically added by the system.

### -field cUnauthAttr

Number of elements in the <b>rgUnauthAttr</b> array. If no unauthenticated attributes are present in <b>rgUnauthAttr</b>, this member is zero.

### -field rgUnauthAttr

Array of pointers to 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute">CRYPT_ATTRIBUTE</a> structures each holding an unauthenticated attribute information. Unauthenticated attributes can be used to contain <a href="/windows/desktop/SecGloss/c-gly">countersignatures</a>, among other uses.

### -field dwFlags

Normally zero. If the encoded output is to be a CMSG_SIGNED <a href="/windows/desktop/SecGloss/i-gly">inner content</a> of an outer cryptographic message such as a CMSG_ENVELOPED message, the CRYPT_MESSAGE_BARE_CONTENT_OUT_FLAG must be set. If it is not set, the message will be encoded as an <i>inner content</i> type of CMSG_DATA. 




CRYPT_MESSAGE_ENCAPSULATED_CONTENT_OUT_FLAG can be set to encapsulate non-data <a href="/windows/desktop/SecGloss/i-gly">inner content</a> into an OCTET STRING. CRYPT_MESSAGE_KEYID_SIGNER_FLAG can be set to identify signers by their Key Identifier and not their Issuer and Serial Number.

CRYPT_MESSAGE_SILENT_KEYSET_FLAG can be set to suppress any UI by the CSP. For more information about the CRYPT_SILENT flag, see 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a>.

### -field dwInnerContentType

Normally zero. Set to the encoding type of the input message if that input to be signed is the encoded output of another cryptographic message.

### -field HashEncryptionAlgorithm

A 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>. If present and not <b>NULL</b>, it is used instead of the signer's certificate <b>PublicKeyInfo.Algorithm</b> member. Note that for RSA, the hash encryption algorithm is normally the same as the public key algorithm. For DSA, the hash encryption algorithm is normally a DSS signature algorithm. This member can only be used if CRYPT_SIGN_MESSAGE_PARA_HAS_CMS_FIELDS is defined.

### -field pvHashEncryptionAuxInfo

Currently not used and must be set to <b>NULL</b>. This member can only be used if CRYPT_SIGN_MESSAGE_PARA_HAS_CMS_FIELDS is defined.

## -remarks

The <b>HashEncryptionAlgorithm</b> and <b>pvHashEncryptionAuxInfo</b> members can only be used if CRYPT_SIGN_MESSAGE_PARA_HAS_CMS_FIELDS is defined.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute">CRYPT_ATTRIBUTE</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsignandencryptmessage">CryptSignAndEncryptMessage</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsignmessage">CryptSignMessage</a>