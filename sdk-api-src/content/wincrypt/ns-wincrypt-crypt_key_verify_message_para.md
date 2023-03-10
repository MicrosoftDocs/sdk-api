---
UID: NS:wincrypt._CRYPT_KEY_VERIFY_MESSAGE_PARA
title: CRYPT_KEY_VERIFY_MESSAGE_PARA (wincrypt.h)
description: Contains information needed to verify signed messages without a certificate for the signer.
helpviewer_keywords: ["*PCRYPT_KEY_VERIFY_MESSAGE_PARA","CRYPT_KEY_VERIFY_MESSAGE_PARA","CRYPT_KEY_VERIFY_MESSAGE_PARA structure [Security]","PCRYPT_KEY_VERIFY_MESSAGE_PARA","PCRYPT_KEY_VERIFY_MESSAGE_PARA structure pointer [Security]","security.crypt_key_verify_message_para","wincrypt/CRYPT_KEY_VERIFY_MESSAGE_PARA","wincrypt/PCRYPT_KEY_VERIFY_MESSAGE_PARA"]
old-location: security\crypt_key_verify_message_para.htm
tech.root: security
ms.assetid: 4e0178fb-1f9f-4ee4-9a83-f37cf71d35ff
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_KEY_VERIFY_MESSAGE_PARA, CRYPT_KEY_VERIFY_MESSAGE_PARA, CRYPT_KEY_VERIFY_MESSAGE_PARA structure [Security], PCRYPT_KEY_VERIFY_MESSAGE_PARA, PCRYPT_KEY_VERIFY_MESSAGE_PARA structure pointer [Security], security.crypt_key_verify_message_para, wincrypt/CRYPT_KEY_VERIFY_MESSAGE_PARA, wincrypt/PCRYPT_KEY_VERIFY_MESSAGE_PARA'
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
req.typenames: CRYPT_KEY_VERIFY_MESSAGE_PARA, *PCRYPT_KEY_VERIFY_MESSAGE_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_KEY_VERIFY_MESSAGE_PARA
 - wincrypt/_CRYPT_KEY_VERIFY_MESSAGE_PARA
 - PCRYPT_KEY_VERIFY_MESSAGE_PARA
 - wincrypt/PCRYPT_KEY_VERIFY_MESSAGE_PARA
 - CRYPT_KEY_VERIFY_MESSAGE_PARA
 - wincrypt/CRYPT_KEY_VERIFY_MESSAGE_PARA
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
 - CRYPT_KEY_VERIFY_MESSAGE_PARA
---

# CRYPT_KEY_VERIFY_MESSAGE_PARA structure


## -description

The <b>CRYPT_KEY_VERIFY_MESSAGE_PARA</b> structure contains information needed to verify signed messages without a certificate for the signer.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

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

<b>Windows Server 2003 and Windows XP:  </b>A handle to the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) to be used to verify a signed message. The CSP identified by this handle is used for <a href="/windows/desktop/SecGloss/h-gly">hashing</a> and for signature verification.Unless there is a strong reason for using a specific cryptographic provider, set this member to  zero to use the default RSA or DSS provider.

This member's data type is <b>HCRYPTPROV</b>.