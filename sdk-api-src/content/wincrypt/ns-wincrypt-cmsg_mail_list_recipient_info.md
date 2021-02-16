---
UID: NS:wincrypt._CMSG_MAIL_LIST_RECIPIENT_INFO
title: CMSG_MAIL_LIST_RECIPIENT_INFO (wincrypt.h)
description: Contains information used for previously distributed symmetric key-encryption keys (KEK).
helpviewer_keywords: ["*PCMSG_MAIL_LIST_RECIPIENT_INFO","CMSG_MAIL_LIST_RECIPIENT_INFO","CMSG_MAIL_LIST_RECIPIENT_INFO structure [Security]","PCMSG_MAIL_LIST_RECIPIENT_INFO","PCMSG_MAIL_LIST_RECIPIENT_INFO structure pointer [Security]","_crypto2_cmsg_mail_list_recipient_info","security.cmsg_mail_list_recipient_info","wincrypt/CMSG_MAIL_LIST_RECIPIENT_INFO","wincrypt/PCMSG_MAIL_LIST_RECIPIENT_INFO"]
old-location: security\cmsg_mail_list_recipient_info.htm
tech.root: security
ms.assetid: e0946278-75e9-4990-af81-d9e61da9724b
ms.date: 12/05/2018
ms.keywords: '*PCMSG_MAIL_LIST_RECIPIENT_INFO, CMSG_MAIL_LIST_RECIPIENT_INFO, CMSG_MAIL_LIST_RECIPIENT_INFO structure [Security], PCMSG_MAIL_LIST_RECIPIENT_INFO, PCMSG_MAIL_LIST_RECIPIENT_INFO structure pointer [Security], _crypto2_cmsg_mail_list_recipient_info, security.cmsg_mail_list_recipient_info, wincrypt/CMSG_MAIL_LIST_RECIPIENT_INFO, wincrypt/PCMSG_MAIL_LIST_RECIPIENT_INFO'
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
req.typenames: CMSG_MAIL_LIST_RECIPIENT_INFO, *PCMSG_MAIL_LIST_RECIPIENT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMSG_MAIL_LIST_RECIPIENT_INFO
 - wincrypt/_CMSG_MAIL_LIST_RECIPIENT_INFO
 - PCMSG_MAIL_LIST_RECIPIENT_INFO
 - wincrypt/PCMSG_MAIL_LIST_RECIPIENT_INFO
 - CMSG_MAIL_LIST_RECIPIENT_INFO
 - wincrypt/CMSG_MAIL_LIST_RECIPIENT_INFO
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
 - CMSG_MAIL_LIST_RECIPIENT_INFO
---

# CMSG_MAIL_LIST_RECIPIENT_INFO structure


## -description

The <b>CMSG_MAIL_LIST_RECIPIENT_INFO</b> structure contains information used for previously distributed <a href="/windows/desktop/SecGloss/s-gly">symmetric</a> key-encryption keys (KEK).

## -struct-fields

### -field dwVersion

Indicates the version of the structure. This member is always four.

### -field KeyId

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that identifies a <a href="/windows/desktop/SecGloss/s-gly">symmetric key</a>-encryption key previously distributed to the sender and one or more recipients.

### -field KeyEncryptionAlgorithm

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> that identifies the key-encryption algorithm and any associated parameters used to encrypt the content encryption key.

### -field EncryptedKey

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that contains the encrypted content encryption key.

### -field Date

Optional. When present, this member specifies a single key-encryption key from a previously distributed set.

### -field pOtherAttr

Optional pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute_type_value">CRYPT_ATTRIBUTE_TYPE_VALUE</a> structure containing additional information.