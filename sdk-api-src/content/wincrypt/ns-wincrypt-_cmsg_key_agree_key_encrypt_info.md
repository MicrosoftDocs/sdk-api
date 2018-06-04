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

# _CMSG_KEY_AGREE_KEY_ENCRYPT_INFO structure


## -description


The <b>CMSG_KEY_AGREE_KEY_ENCRYPT_INFO</b> structure contains the encrypted key for a key agreement recipient of an enveloped message. The <a href="https://msdn.microsoft.com/7604ac82-a1a2-451b-8615-98303ce1d83e">CMSG_KEY_AGREE_ENCRYPT_INFO</a> structure references this structure.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field EncryptedKey

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that contains the session key encrypted by the negotiated key of the recipient.

