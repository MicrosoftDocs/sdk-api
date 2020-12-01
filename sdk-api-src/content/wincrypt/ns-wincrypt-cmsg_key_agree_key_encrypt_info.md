---
UID: NS:wincrypt._CMSG_KEY_AGREE_KEY_ENCRYPT_INFO
title: CMSG_KEY_AGREE_KEY_ENCRYPT_INFO (wincrypt.h)
description: Contains the encrypted key for a key agreement recipient of an enveloped message.
helpviewer_keywords: ["*PCMSG_KEY_AGREE_KEY_ENCRYPT_INFO","CMSG_KEY_AGREE_KEY_ENCRYPT_INFO","CMSG_KEY_AGREE_KEY_ENCRYPT_INFO structure [Security]","PCMSG_KEY_AGREE_KEY_ENCRYPT_INFO","PCMSG_KEY_AGREE_KEY_ENCRYPT_INFO structure pointer [Security]","security.cmsg_key_agree_key_encrypt_info","wincrypt/CMSG_KEY_AGREE_KEY_ENCRYPT_INFO","wincrypt/PCMSG_KEY_AGREE_KEY_ENCRYPT_INFO"]
old-location: security\cmsg_key_agree_key_encrypt_info.htm
tech.root: security
ms.assetid: 586d40cc-8ef6-475b-8b7b-cc1a0bdddfcb
ms.date: 12/05/2018
ms.keywords: '*PCMSG_KEY_AGREE_KEY_ENCRYPT_INFO, CMSG_KEY_AGREE_KEY_ENCRYPT_INFO, CMSG_KEY_AGREE_KEY_ENCRYPT_INFO structure [Security], PCMSG_KEY_AGREE_KEY_ENCRYPT_INFO, PCMSG_KEY_AGREE_KEY_ENCRYPT_INFO structure pointer [Security], security.cmsg_key_agree_key_encrypt_info, wincrypt/CMSG_KEY_AGREE_KEY_ENCRYPT_INFO, wincrypt/PCMSG_KEY_AGREE_KEY_ENCRYPT_INFO'
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
req.typenames: CMSG_KEY_AGREE_KEY_ENCRYPT_INFO, *PCMSG_KEY_AGREE_KEY_ENCRYPT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMSG_KEY_AGREE_KEY_ENCRYPT_INFO
 - wincrypt/_CMSG_KEY_AGREE_KEY_ENCRYPT_INFO
 - PCMSG_KEY_AGREE_KEY_ENCRYPT_INFO
 - wincrypt/PCMSG_KEY_AGREE_KEY_ENCRYPT_INFO
 - CMSG_KEY_AGREE_KEY_ENCRYPT_INFO
 - wincrypt/CMSG_KEY_AGREE_KEY_ENCRYPT_INFO
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
 - CMSG_KEY_AGREE_KEY_ENCRYPT_INFO
---

# CMSG_KEY_AGREE_KEY_ENCRYPT_INFO structure


## -description

The <b>CMSG_KEY_AGREE_KEY_ENCRYPT_INFO</b> structure contains the encrypted key for a key agreement recipient of an enveloped message. The <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_key_agree_encrypt_info">CMSG_KEY_AGREE_ENCRYPT_INFO</a> structure references this structure.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field EncryptedKey

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that contains the session key encrypted by the negotiated key of the recipient.