---
UID: NS:wincrypt._CRYPT_ENCRYPT_MESSAGE_PARA
title: CRYPT_ENCRYPT_MESSAGE_PARA (wincrypt.h)
description: Contains information used to encrypt messages.
helpviewer_keywords: ["*PCRYPT_ENCRYPT_MESSAGE_PARA","CRYPT_ENCRYPT_MESSAGE_PARA","CRYPT_ENCRYPT_MESSAGE_PARA structure [Security]","PCRYPT_ENCRYPT_MESSAGE_PARA","PCRYPT_ENCRYPT_MESSAGE_PARA structure pointer [Security]","_crypto2_crypt_encrypt_message_para","security.crypt_encrypt_message_para","wincrypt/CRYPT_ENCRYPT_MESSAGE_PARA","wincrypt/PCRYPT_ENCRYPT_MESSAGE_PARA"]
old-location: security\crypt_encrypt_message_para.htm
tech.root: security
ms.assetid: c683c515-3061-48e3-a64a-2798bd1245b0
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_ENCRYPT_MESSAGE_PARA, CRYPT_ENCRYPT_MESSAGE_PARA, CRYPT_ENCRYPT_MESSAGE_PARA structure [Security], PCRYPT_ENCRYPT_MESSAGE_PARA, PCRYPT_ENCRYPT_MESSAGE_PARA structure pointer [Security], _crypto2_crypt_encrypt_message_para, security.crypt_encrypt_message_para, wincrypt/CRYPT_ENCRYPT_MESSAGE_PARA, wincrypt/PCRYPT_ENCRYPT_MESSAGE_PARA'
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
req.typenames: CRYPT_ENCRYPT_MESSAGE_PARA, *PCRYPT_ENCRYPT_MESSAGE_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_ENCRYPT_MESSAGE_PARA
 - wincrypt/_CRYPT_ENCRYPT_MESSAGE_PARA
 - PCRYPT_ENCRYPT_MESSAGE_PARA
 - wincrypt/PCRYPT_ENCRYPT_MESSAGE_PARA
 - CRYPT_ENCRYPT_MESSAGE_PARA
 - wincrypt/CRYPT_ENCRYPT_MESSAGE_PARA
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
 - CRYPT_ENCRYPT_MESSAGE_PARA
---

# CRYPT_ENCRYPT_MESSAGE_PARA structure


## -description

The <b>CRYPT_ENCRYPT_MESSAGE_PARA</b> structure contains information used to encrypt messages.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field dwMsgEncodingType

The type of encoding used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -field hCryptProv

This member is not used and should be set to <b>NULL</b>.

<b>Windows Server 2003 and Windows XP:  </b>The handle to the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) to be used for encryption. The CSP identified by <b>hCryptProv</b> is used to do content encryption, recipient key encryption, and recipient key export. Its private key is not used. 


Unless there is a strong reason for passing in a specific <a href="/windows/desktop/SecGloss/c-gly">cryptographic provider</a> in <b>hCryptProv</b>, pass zero to use the default RSA or DSS provider.

This member's data type is <b>HCRYPTPROV</b>.

### -field ContentEncryptionAlgorithm

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) of the encryption algorithm to use. The CSP specified by the <b>hCryptProv</b> must support this encryption algorithm.

The <b>szOID_OIWSEC_desCBC</b> (CALG_DES) and <b>szOID_RSA_DES_EDE3_CBC</b> (CALG_3DES) encryption algorithms require the <b>Parameters</b> member of this structure to contain an encoded eight-byte <a href="/windows/desktop/SecGloss/i-gly">initialization vector</a> (IV).  If the <b>cbData</b> member of the <b>Parameters</b> member is zero, an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1)-encoded OCTET STRING that contains the IV is generated using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom">CryptGenRandom</a>. For more information about the KP_IV parameter, see 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetkeyparam">CryptSetKeyParam</a>.

The <b>szOID_NIST_AES128_CBC</b> (BCRYPT_AES_ALGORITHM, 128 bit),  <b>szOID_NIST_AES192_CBC</b> (BCRYPT_AES_ALGORITHM, 192 bit),  and <b>szOID_NIST_AES256_CBC</b> (BCRYPT_AES_ALGORITHM, 256 bit) encryption algorithms require the <b>Parameters</b> member of this structure to contain an encoded sixteen-byte initialization vector (IV). If the <b>cbData</b> member of the Parameters member is zero, an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1)-encoded OCTET STRING that contains the IV is generated.

The <b>szOID_RSA_RC2CBC</b> (CALG_RC2) algorithm requires the <b>pbData</b> member of the <b>Parameters</b> member of this structure to be a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_rc2_cbc_parameters">CRYPT_RC2_CBC_PARAMETERS</a> structure. If the <b>cbData</b> member of the <b>Parameters</b> member is zero, an ASN.1-encoded <b>CRYPT_RC2_CBC_PARAMETERS</b> structure that contains  the IV is generated as the <b>pbData</b> member. This generated <b>pbData</b> uses the default <b>dwVersion</b>  that corresponds to the 40-bit key length. To override the default 40-bit key length, <b>pvEncryptionAuxInfo</b> can be set to point to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_rc2_aux_info">CMSG_RC2_AUX_INFO</a> structure that contains a key bit length.

<div class="alert"><b>Note</b>  When a message is decrypted, if it has an <a href="/windows/desktop/SecGloss/i-gly">initialization vector</a> parameter, the cryptographic message functions call 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetkeyparam">CryptSetKeyParam</a> with the <i>initialization vector</i> before decrypting.</div>
<div> </div>

### -field pvEncryptionAuxInfo

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_rc2_aux_info">CMSG_RC2_AUX_INFO</a> structure for RC2 encryption or a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_sp3_compatible_aux_info">CMSG_SP3_COMPATIBLE_AUX_INFO</a> structure for SP3-compatible encryption. For other than RC2 or SP3-compatible encryption, this member must be set to <b>NULL</b>.

If the <b>ContentEncryptionAlgorithm</b> member contains <b>szOID_RSA_RC4</b>, this member points to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_rc4_aux_info">CMSG_RC4_AUX_INFO</a> structure  that specifies the number of <a href="/windows/desktop/SecGloss/s-gly">salt bytes</a> to be included.

### -field dwFlags

Normally set to zero. However, if the encoded output is to be a CMSG_ENVELOPED <a href="/windows/desktop/SecGloss/i-gly">inner content</a> of an outer cryptographic message, such as a CMSG_SIGNED message, the CRYPT_MESSAGE_BARE_CONTENT_OUT_FLAG must be set. If it is not set, content will be encoded as an <i>inner content</i> type of CMSG_DATA.

CRYPT_MESSAGE_ENCAPSULATED_CONTENT_OUT_FLAG can be set to encapsulate non-data <a href="/windows/desktop/SecGloss/i-gly">inner content</a> within an OCTET STRING before encrypting.

CRYPT_MESSAGE_KEYID_RECIPIENT_FLAG can be set to identify recipients by their Key Identifier and not their Issuer and Serial Number.

### -field dwInnerContentType

Normally set to zero. The <b>dwInnerContentType</b> member must be set to set the cryptographic message types if the input to be encrypted is the encoded output of another cryptographic message such as CMSG_SIGNED.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencryptmessage">CryptEncryptMessage</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsignandencryptmessage">CryptSignAndEncryptMessage</a>