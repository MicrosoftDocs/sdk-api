---
UID: NS:wincrypt._CMSG_RECIPIENT_ENCRYPTED_KEY_INFO
title: "_CMSG_RECIPIENT_ENCRYPTED_KEY_INFO"
author: windows-sdk-content
description: The CMSG_RECIPIENT_ENCRYPTED_KEY_INFO structure contains information used for an individual key agreement recipient.
old-location: security\cmsg_recipient_encrypted_key_info.htm
tech.root: seccrypto
ms.assetid: 1921f9b6-86d9-47a0-a36e-e20d481382a3
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*PCMSG_RECIPIENT_ENCRYPTED_KEY_INFO, CMSG_RECIPIENT_ENCRYPTED_KEY_INFO, CMSG_RECIPIENT_ENCRYPTED_KEY_INFO structure [Security], PCMSG_RECIPIENT_ENCRYPTED_KEY_INFO, PCMSG_RECIPIENT_ENCRYPTED_KEY_INFO structure pointer [Security], _CMSG_RECIPIENT_ENCRYPTED_KEY_INFO, _crypto2_cmsg_recipient_encrypted_key_info, security.cmsg_recipient_encrypted_key_info, wincrypt/CMSG_RECIPIENT_ENCRYPTED_KEY_INFO, wincrypt/PCMSG_RECIPIENT_ENCRYPTED_KEY_INFO"
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
 - CMSG_RECIPIENT_ENCRYPTED_KEY_INFO
product: Windows
targetos: Windows
req.typenames: CMSG_RECIPIENT_ENCRYPTED_KEY_INFO, *PCMSG_RECIPIENT_ENCRYPTED_KEY_INFO
req.redist: 
---

# _CMSG_RECIPIENT_ENCRYPTED_KEY_INFO structure


## -description


The <b>CMSG_RECIPIENT_ENCRYPTED_KEY_INFO</b> structure contains information used for an individual key agreement recipient.


## -struct-fields




### -field RecipientId


<a href="https://msdn.microsoft.com/9e33f661-c365-4725-8c3f-27b6cdd9a84e">CERT_ID</a> structure identifying the recipient. Currently, only the ISSUER_SERIAL_NUMBER or KEYID choices in the <b>CERT_ID</b> structure are valid.


### -field EncryptedKey

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that contains the encrypted content encryption key.


### -field Date

Optional. When present, this member specifies which of the recipient's previously distributed UKMs was used by the sender. Only applicable to KEYID choice in the <b>RecipientId </b><a href="https://msdn.microsoft.com/9e33f661-c365-4725-8c3f-27b6cdd9a84e">CERT_ID</a> structure.


### -field pOtherAttr

Optional pointer to a 
<a href="https://msdn.microsoft.com/84057581-d0a9-464a-9399-ba806e37516f">CRYPT_ATTRIBUTE_TYPE_VALUE</a> structure containing additional information. Only applicable to KEYID choice in the <b>RecipientId </b><a href="https://msdn.microsoft.com/9e33f661-c365-4725-8c3f-27b6cdd9a84e">CERT_ID</a> structure.

