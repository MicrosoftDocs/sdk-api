---
UID: NS:wincrypt._CMSG_CTRL_MAIL_LIST_DECRYPT_PARA
title: "_CMSG_CTRL_MAIL_LIST_DECRYPT_PARA"
author: windows-sdk-content
description: Contains information on a mail list message recipient.
old-location: security\cmsg_ctrl_mail_list_decrypt_para.htm
tech.root: seccrypto
ms.assetid: 30735e01-db6b-40fc-b4c8-cdc24e73defa
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: "*PCMSG_CTRL_MAIL_LIST_DECRYPT_PARA, CMSG_CTRL_MAIL_LIST_DECRYPT_PARA, CMSG_CTRL_MAIL_LIST_DECRYPT_PARA structure [Security], PCMSG_CTRL_MAIL_LIST_DECRYPT_PARA, PCMSG_CTRL_MAIL_LIST_DECRYPT_PARA structure pointer [Security], _CMSG_CTRL_MAIL_LIST_DECRYPT_PARA, _crypto2_cmsg_ctrl_mail_list_decrypt_para, security.cmsg_ctrl_mail_list_decrypt_para, wincrypt/CMSG_CTRL_MAIL_LIST_DECRYPT_PARA, wincrypt/PCMSG_CTRL_MAIL_LIST_DECRYPT_PARA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CMSG_CTRL_MAIL_LIST_DECRYPT_PARA
product: Windows
targetos: Windows
req.typenames: CMSG_CTRL_MAIL_LIST_DECRYPT_PARA, *PCMSG_CTRL_MAIL_LIST_DECRYPT_PARA
req.redist: 
---

# _CMSG_CTRL_MAIL_LIST_DECRYPT_PARA structure


## -description


The <b>CMSG_CTRL_MAIL_LIST_DECRYPT_PARA</b> structure contains information on a mail list message recipient.


## -struct-fields




### -field cbSize

The size, in bytes, of this data structure.


### -field hCryptProv

The provider used to do the recipient key encryption and export. If <b>hCryptProv</b> is <b>NULL</b>, the provider specified in <a href="https://msdn.microsoft.com/87712541-2806-4709-a7cf-c9ba966c96fd">CMSG_ENVELOPED_ENCODE_INFO</a> is used.


### -field pMailList

A pointer to a <a href="https://msdn.microsoft.com/e0946278-75e9-4990-af81-d9e61da9724b">CMSG_MAIL_LIST_RECIPIENT_INFO</a> structure.


### -field dwRecipientIndex

Indicates a specific recipient in any array of recipients.


### -field dwKeyChoice

Indicates the member of the following union that will be used. Currently only CMSG_MAIL_LIST_HANDLE_KEY_CHOICE is defined.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.hKeyEncryptionKey

Handle of the key encryption key. Used with <b>dwKeyChoice</b> set to CMSG_MAIL_LIST_HANDLE_KEY_CHOICE.


### -field DUMMYUNIONNAME.pvKeyEncryptionKey

A pointer to a void. Reserved for future use.

