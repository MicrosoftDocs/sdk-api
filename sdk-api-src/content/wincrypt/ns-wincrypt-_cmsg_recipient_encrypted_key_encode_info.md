---
UID: NS:wincrypt._CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO
title: "_CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO"
author: windows-sdk-content
description: Contains information on a message receiver used to decrypt the session key needed to decrypt the message contents.
old-location: security\cmsg_recipient_encrypted_key_encode_info.htm
old-project: SecCrypto
ms.assetid: 839ab3d8-0fdc-4d43-a12b-238091289ff5
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: "*PCMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO, CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO, CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO structure [Security], PCMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO, PCMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO structure pointer [Security], _CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO, _crypto2_cmsg_recipient_encrypted_key_encode_info, security.cmsg_recipient_encrypted_key_encode_info, wincrypt/CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO, wincrypt/PCMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO"
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
req.typenames: CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO, *PCMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO structure


## -description


The <b>CMSG_RECIPIENT_ENCRYPTED_KEY_ENCODE_INFO</b> structure contains information on a message receiver used to decrypt the session key needed to decrypt the message contents. This structure is used with CMS low level messages using any of the key management methods.


## -struct-fields




### -field cbSize

The size, in bytes, of this data structure.


### -field RecipientPublicKey


						A <a href="https://msdn.microsoft.com/6f102ff3-bfff-4415-a5d8-ca2c226074b3">CRYPT_BIT_BLOB</a> structure that contains the recipient's public key.


### -field RecipientId

The <a href="https://msdn.microsoft.com/9e33f661-c365-4725-8c3f-27b6cdd9a84e">CERT_ID</a> that identifies a message recipient's public key. 
					


### -field Date

Optional <b>FILETIME</b>. Applicable only if the <a href="https://msdn.microsoft.com/9e33f661-c365-4725-8c3f-27b6cdd9a84e">CERT_ID</a> identifies the receiver's public key with a KEY_IDENTIFIER.


### -field pOtherAttr

Optional. Pointer to a <a href="https://msdn.microsoft.com/84057581-d0a9-464a-9399-ba806e37516f">CRYPT_ATTRIBUTE_TYPE_VALUE</a>. Applicable only if the CERT_ID identifies the receiver's public key with a KEY_IDENTIFIER.

