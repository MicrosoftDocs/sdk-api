---
UID: NS:wincrypt._CMSG_CTRL_KEY_AGREE_DECRYPT_PARA
title: "_CMSG_CTRL_KEY_AGREE_DECRYPT_PARA"
author: windows-sdk-content
description: Contains information about a key agreement recipient.
old-location: security\cmsg_ctrl_key_agree_decrypt_para.htm
old-project: seccrypto
ms.assetid: 14e58281-4315-4ece-8ea8-92765cffd212
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PCMSG_CTRL_KEY_AGREE_DECRYPT_PARA, CMSG_CTRL_KEY_AGREE_DECRYPT_PARA, CMSG_CTRL_KEY_AGREE_DECRYPT_PARA structure [Security], PCMSG_CTRL_KEY_AGREE_DECRYPT_PARA, PCMSG_CTRL_KEY_AGREE_DECRYPT_PARA structure pointer [Security], _CMSG_CTRL_KEY_AGREE_DECRYPT_PARA, _crypto2_cmsg_ctrl_key_agree_decrypt_para, security.cmsg_ctrl_key_agree_decrypt_para, wincrypt/CMSG_CTRL_KEY_AGREE_DECRYPT_PARA, wincrypt/PCMSG_CTRL_KEY_AGREE_DECRYPT_PARA"
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
tech.root: 
req.typenames: CMSG_CTRL_KEY_AGREE_DECRYPT_PARA, *PCMSG_CTRL_KEY_AGREE_DECRYPT_PARA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CMSG_CTRL_KEY_AGREE_DECRYPT_PARA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CMSG_CTRL_KEY_AGREE_DECRYPT_PARA structure


## -description


The <b>CMSG_CTRL_KEY_AGREE_DECRYPT_PARA</b> structure contains information about a key agreement recipient.


## -struct-fields




### -field cbSize

The size, in bytes,  of this data structure.
					


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.hCryptProv

A handle to the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) used to do the recipient key encryption and export. If <b>NULL</b>, the provider specified in <a href="https://msdn.microsoft.com/87712541-2806-4709-a7cf-c9ba966c96fd">CMSG_ENVELOPED_ENCODE_INFO</a> is used.
					The CNG function <a href="https://msdn.microsoft.com/ad841c2e-8097-4b07-914e-8e7240d55585">NCryptIsKeyHandle</a> is called to determine the union choice.


### -field DUMMYUNIONNAME.hNCryptKey

A handle to the CNG CSP used to do the recipient key encryption and export. The CNG function <a href="https://msdn.microsoft.com/ad841c2e-8097-4b07-914e-8e7240d55585">NCryptIsKeyHandle</a> is called to determine the union choice. New encrypt algorithms are only supported in CNG functions. The CNG function <a href="https://msdn.microsoft.com/0c339864-b598-430c-a597-09d3571fdbb2">NCryptTranslateHandle</a> will be called to convert the CryptoAPI CSP <i>hCryptProv</i> choice where necessary. We recommend that applications pass, to the <i>hNCryptKey</i> member, the CNG CSP handle that is returned from the <a href="https://msdn.microsoft.com/581c5d89-730d-4d8c-b3bb-a28edec25910">NCryptOpenKey</a> function.


### -field dwKeySpec

Specifies the encrypted key. The encrypted key is the result of encrypting the content-encryption key. This member is not used when the <i>hNCryptKey</i> member is used.


### -field pKeyAgree

A pointer to a <a href="https://msdn.microsoft.com/d29d04d6-065e-4bb7-843b-f563643eeb4c">CMSG_KEY_AGREE_RECIPIENT_INFO</a> structure.


### -field dwRecipientIndex

Indicates a specific recipient in an array of recipients.


### -field dwRecipientEncryptedKeyIndex

Indicates a specific encrypted key in an array of encrypted keys.


### -field OriginatorPublicKey

A <a href="https://msdn.microsoft.com/6f102ff3-bfff-4415-a5d8-ca2c226074b3">CRYPT_BIT_BLOB</a> structure that contains the sender's public key information.

