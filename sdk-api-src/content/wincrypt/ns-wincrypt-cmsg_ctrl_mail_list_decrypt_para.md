---
UID: NS:wincrypt._CMSG_CTRL_MAIL_LIST_DECRYPT_PARA
title: CMSG_CTRL_MAIL_LIST_DECRYPT_PARA (wincrypt.h)
description: Contains information on a mail list message recipient.
helpviewer_keywords: ["*PCMSG_CTRL_MAIL_LIST_DECRYPT_PARA","CMSG_CTRL_MAIL_LIST_DECRYPT_PARA","CMSG_CTRL_MAIL_LIST_DECRYPT_PARA structure [Security]","PCMSG_CTRL_MAIL_LIST_DECRYPT_PARA","PCMSG_CTRL_MAIL_LIST_DECRYPT_PARA structure pointer [Security]","_crypto2_cmsg_ctrl_mail_list_decrypt_para","security.cmsg_ctrl_mail_list_decrypt_para","wincrypt/CMSG_CTRL_MAIL_LIST_DECRYPT_PARA","wincrypt/PCMSG_CTRL_MAIL_LIST_DECRYPT_PARA"]
old-location: security\cmsg_ctrl_mail_list_decrypt_para.htm
tech.root: security
ms.assetid: 30735e01-db6b-40fc-b4c8-cdc24e73defa
ms.date: 12/05/2018
ms.keywords: '*PCMSG_CTRL_MAIL_LIST_DECRYPT_PARA, CMSG_CTRL_MAIL_LIST_DECRYPT_PARA, CMSG_CTRL_MAIL_LIST_DECRYPT_PARA structure [Security], PCMSG_CTRL_MAIL_LIST_DECRYPT_PARA, PCMSG_CTRL_MAIL_LIST_DECRYPT_PARA structure pointer [Security], _crypto2_cmsg_ctrl_mail_list_decrypt_para, security.cmsg_ctrl_mail_list_decrypt_para, wincrypt/CMSG_CTRL_MAIL_LIST_DECRYPT_PARA, wincrypt/PCMSG_CTRL_MAIL_LIST_DECRYPT_PARA'
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
req.typenames: CMSG_CTRL_MAIL_LIST_DECRYPT_PARA, *PCMSG_CTRL_MAIL_LIST_DECRYPT_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMSG_CTRL_MAIL_LIST_DECRYPT_PARA
 - wincrypt/_CMSG_CTRL_MAIL_LIST_DECRYPT_PARA
 - PCMSG_CTRL_MAIL_LIST_DECRYPT_PARA
 - wincrypt/PCMSG_CTRL_MAIL_LIST_DECRYPT_PARA
 - CMSG_CTRL_MAIL_LIST_DECRYPT_PARA
 - wincrypt/CMSG_CTRL_MAIL_LIST_DECRYPT_PARA
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
 - CMSG_CTRL_MAIL_LIST_DECRYPT_PARA
---

# CMSG_CTRL_MAIL_LIST_DECRYPT_PARA structure


## -description

The <b>CMSG_CTRL_MAIL_LIST_DECRYPT_PARA</b> structure contains information on a mail list message recipient.

## -struct-fields

### -field cbSize

The size, in bytes, of this data structure.

### -field hCryptProv

The provider used to do the recipient key encryption and export. If <b>hCryptProv</b> is <b>NULL</b>, the provider specified in <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_enveloped_encode_info">CMSG_ENVELOPED_ENCODE_INFO</a> is used.

### -field pMailList

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_mail_list_recipient_info">CMSG_MAIL_LIST_RECIPIENT_INFO</a> structure.

### -field dwRecipientIndex

Indicates a specific recipient in any array of recipients.

### -field dwKeyChoice

Indicates the member of the following union that will be used. Currently only CMSG_MAIL_LIST_HANDLE_KEY_CHOICE is defined.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.hKeyEncryptionKey

Handle of the key encryption key. Used with <b>dwKeyChoice</b> set to CMSG_MAIL_LIST_HANDLE_KEY_CHOICE.

### -field DUMMYUNIONNAME.pvKeyEncryptionKey

A pointer to a void. Reserved for future use.