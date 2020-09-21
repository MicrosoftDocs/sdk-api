---
UID: NS:wincrypt._CRYPT_DECRYPT_MESSAGE_PARA
title: CRYPT_DECRYPT_MESSAGE_PARA (wincrypt.h)
description: The CRYPT_DECRYPT_MESSAGE_PARA structure contains information for decrypting messages.
helpviewer_keywords: ["*PCRYPT_DECRYPT_MESSAGE_PARA","CRYPT_DECRYPT_MESSAGE_PARA","CRYPT_DECRYPT_MESSAGE_PARA structure [Security]","PCRYPT_DECRYPT_MESSAGE_PARA","PCRYPT_DECRYPT_MESSAGE_PARA structure pointer [Security]","_crypto2_crypt_decrypt_message_para","security.crypt_decrypt_message_para","wincrypt/CRYPT_DECRYPT_MESSAGE_PARA","wincrypt/PCRYPT_DECRYPT_MESSAGE_PARA"]
old-location: security\crypt_decrypt_message_para.htm
tech.root: security
ms.assetid: 67e136cd-12e3-4a31-9d8b-b53e1129e940
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_DECRYPT_MESSAGE_PARA, CRYPT_DECRYPT_MESSAGE_PARA, CRYPT_DECRYPT_MESSAGE_PARA structure [Security], PCRYPT_DECRYPT_MESSAGE_PARA, PCRYPT_DECRYPT_MESSAGE_PARA structure pointer [Security], _crypto2_crypt_decrypt_message_para, security.crypt_decrypt_message_para, wincrypt/CRYPT_DECRYPT_MESSAGE_PARA, wincrypt/PCRYPT_DECRYPT_MESSAGE_PARA'
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
req.typenames: CRYPT_DECRYPT_MESSAGE_PARA, *PCRYPT_DECRYPT_MESSAGE_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_DECRYPT_MESSAGE_PARA
 - wincrypt/_CRYPT_DECRYPT_MESSAGE_PARA
 - PCRYPT_DECRYPT_MESSAGE_PARA
 - wincrypt/PCRYPT_DECRYPT_MESSAGE_PARA
 - CRYPT_DECRYPT_MESSAGE_PARA
 - wincrypt/CRYPT_DECRYPT_MESSAGE_PARA
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
 - CRYPT_DECRYPT_MESSAGE_PARA
---

# CRYPT_DECRYPT_MESSAGE_PARA structure


## -description

The <b>CRYPT_DECRYPT_MESSAGE_PARA</b> structure contains information for decrypting messages.

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

### -field cCertStore

Number of elements in the <b>rghCertStore</b> array.

### -field rghCertStore

Array of <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> handles. 




These certificate store handles are used to obtain the <a href="/windows/desktop/SecGloss/c-gly">certificate context</a> to use for decrypting a message. For more information, see the decryption functions 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecryptmessage">CryptDecryptMessage</a>, and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecryptandverifymessagesignature">CryptDecryptAndVerifyMessageSignature</a>. An encrypted message can have one or more recipients. The recipients are identified by a unique certificate identifier, often the <a href="/windows/desktop/SecGloss/h-gly">hash</a> of the certificate issuer and serial number. The certificate stores are searched to find a certificate context corresponding to the unique identifier.

Recipients can also be identified by their KeyId. Both Key Agreement (Diffie-Hellman) and Key Transport (RSA) recipients are supported.

Only certificate contexts in the store with one of the following properties, CERT_KEY_PROV_INFO_PROP_ID, or CERT_KEY_CONTEXT_PROP_ID can be used. These properties specify the location of a needed private exchange key.

### -field dwFlags

The CRYPT_MESSAGE_SILENT_KEYSET_FLAG can be set to suppress any UI by the CSP. For more information about the CRYPT_SILENT flag, see 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecryptandverifymessagesignature">CryptDecryptAndVerifyMessageSignature</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecryptmessage">CryptDecryptMessage</a>