---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

