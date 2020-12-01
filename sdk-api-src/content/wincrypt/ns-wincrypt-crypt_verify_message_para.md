---
UID: NS:wincrypt._CRYPT_VERIFY_MESSAGE_PARA
title: CRYPT_VERIFY_MESSAGE_PARA (wincrypt.h)
description: The CRYPT_VERIFY_MESSAGE_PARA structure contains information needed to verify signed messages.
helpviewer_keywords: ["*PCRYPT_VERIFY_MESSAGE_PARA","CRYPT_VERIFY_MESSAGE_PARA","CRYPT_VERIFY_MESSAGE_PARA structure [Security]","PCRYPT_VERIFY_MESSAGE_PARA","PCRYPT_VERIFY_MESSAGE_PARA structure pointer [Security]","_crypto2_crypt_verify_message_para","security.crypt_verify_message_para","wincrypt/CRYPT_VERIFY_MESSAGE_PARA","wincrypt/PCRYPT_VERIFY_MESSAGE_PARA"]
old-location: security\crypt_verify_message_para.htm
tech.root: security
ms.assetid: bbd56b5e-2bbe-420f-8842-1be50dca779f
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_VERIFY_MESSAGE_PARA, CRYPT_VERIFY_MESSAGE_PARA, CRYPT_VERIFY_MESSAGE_PARA structure [Security], PCRYPT_VERIFY_MESSAGE_PARA, PCRYPT_VERIFY_MESSAGE_PARA structure pointer [Security], _crypto2_crypt_verify_message_para, security.crypt_verify_message_para, wincrypt/CRYPT_VERIFY_MESSAGE_PARA, wincrypt/PCRYPT_VERIFY_MESSAGE_PARA'
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
req.typenames: CRYPT_VERIFY_MESSAGE_PARA, *PCRYPT_VERIFY_MESSAGE_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_VERIFY_MESSAGE_PARA
 - wincrypt/_CRYPT_VERIFY_MESSAGE_PARA
 - PCRYPT_VERIFY_MESSAGE_PARA
 - wincrypt/PCRYPT_VERIFY_MESSAGE_PARA
 - CRYPT_VERIFY_MESSAGE_PARA
 - wincrypt/CRYPT_VERIFY_MESSAGE_PARA
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
 - CRYPT_VERIFY_MESSAGE_PARA
---

# CRYPT_VERIFY_MESSAGE_PARA structure


## -description

The <b>CRYPT_VERIFY_MESSAGE_PARA</b> structure contains information needed to verify signed messages.

## -struct-fields

### -field cbSize

Size of this structure in bytes.

### -field dwMsgAndCertEncodingType

Type of encoding used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -field hCryptProv

This member is not used and should be set to <b>NULL</b>.

<b>Windows Server 2003 and Windows XP:  </b>A handle to the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> to be used to verify a signed message. The CSP identified by this handle is used for <a href="/windows/desktop/SecGloss/h-gly">hashing</a> and for signature verification.Unless there is a strong reason for using a specific cryptographic provider, set to  zero to use the default RSA or DSS provider.

This member's data type is <b>HCRYPTPROV</b>.

### -field pfnGetSignerCertificate

A pointer to the callback function used to get the signer's certificate <a href="/windows/desktop/SecGloss/c-gly">context</a>. If <b>NULL</b>, the default callback is used. The default callback tries to get the signer <a href="/windows/desktop/SecGloss/c-gly">certificate context</a> from the message's <a href="/windows/desktop/SecGloss/c-gly">certificate store</a>.

An application defined–callback function that gets the signer's certificate can be used in place of the default. It is passed the certificate identifier of the signer (its issuer and serial number) and a handle to its cryptographic signed message's certificate store.

See <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_get_signer_certificate">CryptGetSignerCertificateCallback</a> for the callback functions signature and arguments.

### -field pvGetArg

Argument to pass to the callback function. Typically, this gets and verifies the message signer's certificate.

### -field pStrongSignPara

Optional pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_strong_sign_para">CERT_STRONG_SIGN_PARA</a> structure that contains parameters used for strong signing. If you set this member and the function successfully verifies the signature, the function will then check for a strong signature. If the signature is not strong, the operation will fail and set the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> value to <b>NTE_BAD_ALGID</b>.

<div class="alert"><b>Note</b>  You can use the <b>pStrongSignPara</b> member  only if <b>CRYPT_VERIFY_MESSAGE_PARA_HAS_EXTRA_FIELDS</b> is defined by using the <b>#define</b> directive before including Wincrypt.h. If <b>CRYPT_VERIFY_MESSAGE_PARA_HAS_EXTRA_FIELDS</b> is defined, you must zero all unused fields.</div>
<div> </div>
<b>Windows 8 and Windows Server 2012:  </b>Support for this member begins.

## -remarks

This structure is passed to the following functions:

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

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecryptandverifymessagesignature">CryptDecryptAndVerifyMessageSignature</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifydetachedmessagesignature">CryptVerifyDetachedMessageSignature</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifymessagesignature">CryptVerifyMessageSignature</a>