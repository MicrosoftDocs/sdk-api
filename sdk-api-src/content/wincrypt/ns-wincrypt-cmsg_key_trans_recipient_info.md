---
UID: NS:wincrypt._CMSG_KEY_TRANS_RECIPIENT_INFO
title: CMSG_KEY_TRANS_RECIPIENT_INFO (wincrypt.h)
description: The CMSG_KEY_TRANS_RECIPIENT_INFO structure contains information used in key transport algorithms.
helpviewer_keywords: ["*PCMSG_KEY_TRANS_RECIPIENT_INFO","CMSG_KEY_TRANS_RECIPIENT_INFO","CMSG_KEY_TRANS_RECIPIENT_INFO structure [Security]","PCMSG_KEY_TRANS_RECIPIENT_INFO","PCMSG_KEY_TRANS_RECIPIENT_INFO structure pointer [Security]","_crypto2_cmsg_key_trans_recipient_info","security.cmsg_key_trans_recipient_info","wincrypt/CMSG_KEY_TRANS_RECIPIENT_INFO","wincrypt/PCMSG_KEY_TRANS_RECIPIENT_INFO"]
old-location: security\cmsg_key_trans_recipient_info.htm
tech.root: security
ms.assetid: 956b0646-50a5-46d1-aa9a-91194c35d2b2
ms.date: 12/05/2018
ms.keywords: '*PCMSG_KEY_TRANS_RECIPIENT_INFO, CMSG_KEY_TRANS_RECIPIENT_INFO, CMSG_KEY_TRANS_RECIPIENT_INFO structure [Security], PCMSG_KEY_TRANS_RECIPIENT_INFO, PCMSG_KEY_TRANS_RECIPIENT_INFO structure pointer [Security], _crypto2_cmsg_key_trans_recipient_info, security.cmsg_key_trans_recipient_info, wincrypt/CMSG_KEY_TRANS_RECIPIENT_INFO, wincrypt/PCMSG_KEY_TRANS_RECIPIENT_INFO'
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
req.typenames: CMSG_KEY_TRANS_RECIPIENT_INFO, *PCMSG_KEY_TRANS_RECIPIENT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMSG_KEY_TRANS_RECIPIENT_INFO
 - wincrypt/_CMSG_KEY_TRANS_RECIPIENT_INFO
 - PCMSG_KEY_TRANS_RECIPIENT_INFO
 - wincrypt/PCMSG_KEY_TRANS_RECIPIENT_INFO
 - CMSG_KEY_TRANS_RECIPIENT_INFO
 - wincrypt/CMSG_KEY_TRANS_RECIPIENT_INFO
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
 - CMSG_KEY_TRANS_RECIPIENT_INFO
---

# CMSG_KEY_TRANS_RECIPIENT_INFO structure


## -description

The <b>CMSG_KEY_TRANS_RECIPIENT_INFO</b> structure contains information used in key transport algorithms.

## -struct-fields

### -field dwVersion

Indicates the version of the structure. If <b>RecipientId</b> uses the ISSUER_SERIAL_NUMBER to identify the recipient, <b>dwVersion</b> is set to zero. If <b>RecipientId</b> uses KEYID, <b>dwVersion</b> is set to two.

### -field RecipientId

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_id">CERT_ID</a> that identifies the recipient. Currently, only ISSUER_SERIAL_NUMBER or KEYID choices in the <b>CERT_ID</b> are valid.

### -field KeyEncryptionAlgorithm

A 
						<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> that identifies the key-encryption algorithm and any associated parameters used to encrypt the content encryption key.

### -field EncryptedKey

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> that contains the bytes of the encrypted session key.