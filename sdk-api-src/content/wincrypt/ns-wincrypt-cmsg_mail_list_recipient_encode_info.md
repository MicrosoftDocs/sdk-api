---
UID: NS:wincrypt._CMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO
title: CMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO (wincrypt.h)
description: The CMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO structure is used with previously distributed symmetric keys for decrypting the content key encryption key (KEK).
helpviewer_keywords: ["*PCMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO","CMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO","CMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO structure [Security]","PCMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO","PCMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO structure pointer [Security]","_crypto2_cmsg_mail_list_recipient_encode_info","security.cmsg_mail_list_recipient_encode_info","wincrypt/CMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO","wincrypt/PCMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO"]
old-location: security\cmsg_mail_list_recipient_encode_info.htm
tech.root: security
ms.assetid: 4303a7e7-cb93-4ed1-85e6-42359c2c687c
ms.date: 12/05/2018
ms.keywords: '*PCMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO, CMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO, CMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO structure [Security], PCMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO, PCMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO structure pointer [Security], _crypto2_cmsg_mail_list_recipient_encode_info, security.cmsg_mail_list_recipient_encode_info, wincrypt/CMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO, wincrypt/PCMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO'
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
req.typenames: CMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO, *PCMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO
 - wincrypt/_CMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO
 - PCMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO
 - wincrypt/PCMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO
 - CMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO
 - wincrypt/CMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO
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
 - CMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO
---

# CMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO structure


## -description

The <b>CMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO</b> structure is used with previously distributed <a href="/windows/desktop/SecGloss/s-gly">symmetric keys</a> for decrypting the content key encryption key (KEK).

## -struct-fields

### -field cbSize

The size, in bytes, of this data structure.

### -field KeyEncryptionAlgorithm

A 
						<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that indicates the encryption algorithm used.

### -field pvKeyEncryptionAuxInfo

A pointer to a structure that contains any additional encryption information.

### -field hCryptProv

The provider used to do the recipient key encryption and export. If <b>NULL</b>, the provider specified in <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_enveloped_encode_info">CMSG_ENVELOPED_ENCODE_INFO</a> is used.

### -field dwKeyChoice

Indicates which member of the following union will be used. Currently only CMSG_MAIL_LIST_HANDLE_KEY_CHOICE can be used.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.hKeyEncryptionKey

An <b>HCRYPTKEY</b> value used with the CMSG_MAIL_LIST_HANDLE_KEY_CHOICE value of the <i>dwKeyChoice</i> parameter.

### -field DUMMYUNIONNAME.pvKeyEncryptionKey

A pointer to a void. Reserved for a future potential pointer choice.

### -field KeyId

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> key identifier of the key-encryption key that was previously distributed to the message sender and one or more recipients.

### -field Date

Optional <b>FILETIME</b> value. When present, specifies a single key encryption key (KEK) from a set that was previously distributed.

### -field pOtherAttr

Optional pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute_type_value">CRYPT_ATTRIBUTE_TYPE_VALUE</a> structure that contains encryption attributes.