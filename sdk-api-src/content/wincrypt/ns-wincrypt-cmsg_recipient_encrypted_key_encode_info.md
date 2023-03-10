---
UID: NS:wincrypt._CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO
title: CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO (wincrypt.h)
description: Contains information on a message receiver used to decrypt the session key needed to decrypt the message contents.
helpviewer_keywords: ["*PCMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO","CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO","CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO structure [Security]","PCMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO","PCMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO structure pointer [Security]","_crypto2_cmsg_recipient_encrypted_key_encode_info","security.cmsg_recipient_encrypted_key_encode_info","wincrypt/CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO","wincrypt/PCMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO"]
old-location: security\cmsg_recipient_encrypted_key_encode_info.htm
tech.root: security
ms.assetid: 839ab3d8-0fdc-4d43-a12b-238091289ff5
ms.date: 12/05/2018
ms.keywords: '*PCMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO, CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO, CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO structure [Security], PCMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO, PCMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO structure pointer [Security], _crypto2_cmsg_recipient_encrypted_key_encode_info, security.cmsg_recipient_encrypted_key_encode_info, wincrypt/CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO, wincrypt/PCMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO'
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
req.typenames: CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO, *PCMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO
 - wincrypt/_CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO
 - PCMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO
 - wincrypt/PCMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO
 - CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO
 - wincrypt/CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO
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
 - CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO
---

# CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO structure


## -description

The <b>CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO</b> structure contains information on a message receiver used to decrypt the session key needed to decrypt the message contents. This structure is used with CMS low level messages using any of the key management methods.

## -struct-fields

### -field cbSize

The size, in bytes, of this data structure.

### -field RecipientPublicKey

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_bit_blob">CRYPT_BIT_BLOB</a> structure that contains the recipient's public key.

### -field RecipientId

The <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_id">CERT_ID</a> that identifies a message recipient's public key.

### -field Date

Optional <b>FILETIME</b>. Applicable only if the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_id">CERT_ID</a> identifies the receiver's public key with a KEY_IDENTIFIER.

### -field pOtherAttr

Optional. Pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute_type_value">CRYPT_ATTRIBUTE_TYPE_VALUE</a>. Applicable only if the CERT_ID identifies the receiver's public key with a KEY_IDENTIFIER.