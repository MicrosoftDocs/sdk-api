---
UID: NS:wincrypt._CMSG_KEY_AGREE_KEY_ENCRYPT_INFO
title: "_CMSG_KEY_AGREE_KEY_ENCRYPT_INFO"
author: windows-sdk-content
description: Contains the encrypted key for a key agreement recipient of an enveloped message.
old-location: security\cmsg_key_agree_key_encrypt_info.htm
tech.root: seccrypto
ms.assetid: 586d40cc-8ef6-475b-8b7b-cc1a0bdddfcb
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "*PCMSG_KEY_AGREE_KEY_ENCRYPT_INFO, CMSG_KEY_AGREE_KEY_ENCRYPT_INFO, CMSG_KEY_AGREE_KEY_ENCRYPT_INFO structure [Security], PCMSG_KEY_AGREE_KEY_ENCRYPT_INFO, PCMSG_KEY_AGREE_KEY_ENCRYPT_INFO structure pointer [Security], _CMSG_KEY_AGREE_KEY_ENCRYPT_INFO, security.cmsg_key_agree_key_encrypt_info, wincrypt/CMSG_KEY_AGREE_KEY_ENCRYPT_INFO, wincrypt/PCMSG_KEY_AGREE_KEY_ENCRYPT_INFO"
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
 - CMSG_KEY_AGREE_KEY_ENCRYPT_INFO
product: Windows
targetos: Windows
req.typenames: CMSG_KEY_AGREE_KEY_ENCRYPT_INFO, *PCMSG_KEY_AGREE_KEY_ENCRYPT_INFO
req.redist: 
---

# _CMSG_KEY_AGREE_KEY_ENCRYPT_INFO structure


## -description


The <b>CMSG_KEY_AGREE_KEY_ENCRYPT_INFO</b> structure contains the encrypted key for a key agreement recipient of an enveloped message. The <a href="https://msdn.microsoft.com/7604ac82-a1a2-451b-8615-98303ce1d83e">CMSG_KEY_AGREE_ENCRYPT_INFO</a> structure references this structure.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field EncryptedKey

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that contains the session key encrypted by the negotiated key of the recipient.

