---
UID: NS:wincrypt._CMSG_RECIPIENT_ENCRYPTED_KEY_INFO
title: CMSG_RECIPIENT_ENCRYPTED_KEY_INFO (wincrypt.h)
description: The CMSG_RECIPIENT_ENCRYPTED_KEY_INFO structure contains information used for an individual key agreement recipient.
helpviewer_keywords: ["*PCMSG_RECIPIENT_ENCRYPTED_KEY_INFO","CMSG_RECIPIENT_ENCRYPTED_KEY_INFO","CMSG_RECIPIENT_ENCRYPTED_KEY_INFO structure [Security]","PCMSG_RECIPIENT_ENCRYPTED_KEY_INFO","PCMSG_RECIPIENT_ENCRYPTED_KEY_INFO structure pointer [Security]","_crypto2_cmsg_recipient_encrypted_key_info","security.cmsg_recipient_encrypted_key_info","wincrypt/CMSG_RECIPIENT_ENCRYPTED_KEY_INFO","wincrypt/PCMSG_RECIPIENT_ENCRYPTED_KEY_INFO"]
old-location: security\cmsg_recipient_encrypted_key_info.htm
tech.root: security
ms.assetid: 1921f9b6-86d9-47a0-a36e-e20d481382a3
ms.date: 12/05/2018
ms.keywords: '*PCMSG_RECIPIENT_ENCRYPTED_KEY_INFO, CMSG_RECIPIENT_ENCRYPTED_KEY_INFO, CMSG_RECIPIENT_ENCRYPTED_KEY_INFO structure [Security], PCMSG_RECIPIENT_ENCRYPTED_KEY_INFO, PCMSG_RECIPIENT_ENCRYPTED_KEY_INFO structure pointer [Security], _crypto2_cmsg_recipient_encrypted_key_info, security.cmsg_recipient_encrypted_key_info, wincrypt/CMSG_RECIPIENT_ENCRYPTED_KEY_INFO, wincrypt/PCMSG_RECIPIENT_ENCRYPTED_KEY_INFO'
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
req.typenames: CMSG_RECIPIENT_ENCRYPTED_KEY_INFO, *PCMSG_RECIPIENT_ENCRYPTED_KEY_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMSG_RECIPIENT_ENCRYPTED_KEY_INFO
 - wincrypt/_CMSG_RECIPIENT_ENCRYPTED_KEY_INFO
 - PCMSG_RECIPIENT_ENCRYPTED_KEY_INFO
 - wincrypt/PCMSG_RECIPIENT_ENCRYPTED_KEY_INFO
 - CMSG_RECIPIENT_ENCRYPTED_KEY_INFO
 - wincrypt/CMSG_RECIPIENT_ENCRYPTED_KEY_INFO
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
 - CMSG_RECIPIENT_ENCRYPTED_KEY_INFO
---

# CMSG_RECIPIENT_ENCRYPTED_KEY_INFO structure


## -description

The <b>CMSG_RECIPIENT_ENCRYPTED_KEY_INFO</b> structure contains information used for an individual key agreement recipient.

## -struct-fields

### -field RecipientId

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_id">CERT_ID</a> structure identifying the recipient. Currently, only the ISSUER_SERIAL_NUMBER or KEYID choices in the <b>CERT_ID</b> structure are valid.

### -field EncryptedKey

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that contains the encrypted content encryption key.

### -field Date

Optional. When present, this member specifies which of the recipient's previously distributed UKMs was used by the sender. Only applicable to KEYID choice in the <b>RecipientId </b><a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_id">CERT_ID</a> structure.

### -field pOtherAttr

Optional pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute_type_value">CRYPT_ATTRIBUTE_TYPE_VALUE</a> structure containing additional information. Only applicable to KEYID choice in the <b>RecipientId </b><a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_id">CERT_ID</a> structure.