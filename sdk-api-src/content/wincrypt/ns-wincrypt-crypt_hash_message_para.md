---
UID: NS:wincrypt._CRYPT_HASH_MESSAGE_PARA
title: CRYPT_HASH_MESSAGE_PARA (wincrypt.h)
description: Contains data for hashing messages.
helpviewer_keywords: ["*PCRYPT_HASH_MESSAGE_PARA","CRYPT_HASH_MESSAGE_PARA","CRYPT_HASH_MESSAGE_PARA structure [Security]","PCRYPT_HASH_MESSAGE_PARA","PCRYPT_HASH_MESSAGE_PARA structure pointer [Security]","_crypto2_crypt_hash_message_para","security.crypt_hash_message_para","wincrypt/CRYPT_HASH_MESSAGE_PARA","wincrypt/PCRYPT_HASH_MESSAGE_PARA"]
old-location: security\crypt_hash_message_para.htm
tech.root: security
ms.assetid: 60415136-3ac0-4fab-bdbf-faa16e8e43e1
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_HASH_MESSAGE_PARA, CRYPT_HASH_MESSAGE_PARA, CRYPT_HASH_MESSAGE_PARA structure [Security], PCRYPT_HASH_MESSAGE_PARA, PCRYPT_HASH_MESSAGE_PARA structure pointer [Security], _crypto2_crypt_hash_message_para, security.crypt_hash_message_para, wincrypt/CRYPT_HASH_MESSAGE_PARA, wincrypt/PCRYPT_HASH_MESSAGE_PARA'
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
req.typenames: CRYPT_HASH_MESSAGE_PARA, *PCRYPT_HASH_MESSAGE_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_HASH_MESSAGE_PARA
 - wincrypt/_CRYPT_HASH_MESSAGE_PARA
 - PCRYPT_HASH_MESSAGE_PARA
 - wincrypt/PCRYPT_HASH_MESSAGE_PARA
 - CRYPT_HASH_MESSAGE_PARA
 - wincrypt/CRYPT_HASH_MESSAGE_PARA
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
 - CRYPT_HASH_MESSAGE_PARA
---

# CRYPT_HASH_MESSAGE_PARA structure


## -description

The <b>CRYPT_HASH_MESSAGE_PARA</b> structure contains data for <a href="/windows/desktop/SecGloss/h-gly">hashing</a> messages.

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

### -field hCryptProv

This member is not used and should be set to <b>NULL</b>.

<b>Windows Server 2003 and Windows XP:  </b>A handle to the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) to be used.Unless there is a strong reason for passing in a specific cryptographic provider in <b>hCryptProv</b>, pass zero to use the default RSA or DSS provider.

This member's data type is <b>HCRYPTPROV</b>.

### -field HashAlgorithm

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> containing the algorithm for generating the hash of the message.

### -field pvHashAuxInfo

Not currently used, and must be set to <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashmessage">CryptHashMessage</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifydetachedmessagehash">CryptVerifyDetachedMessageHash</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifymessagehash">CryptVerifyMessageHash</a>