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

# _CMSG_KEY_TRANS_RECIPIENT_INFO structure


## -description


The <b>CMSG_KEY_TRANS_RECIPIENT_INFO</b> structure contains information used in key transport algorithms.


## -struct-fields




### -field dwVersion

Indicates the version of the structure. If <b>RecipientId</b> uses the ISSUER_SERIAL_NUMBER to identify the recipient, <b>dwVersion</b> is set to zero. If <b>RecipientId</b> uses KEYID, <b>dwVersion</b> is set to two.


### -field RecipientId


						A <a href="https://msdn.microsoft.com/9e33f661-c365-4725-8c3f-27b6cdd9a84e">CERT_ID</a> that identifies the recipient. Currently, only ISSUER_SERIAL_NUMBER or KEYID choices in the <b>CERT_ID</b> are valid.


### -field KeyEncryptionAlgorithm

A 
						<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> that identifies the key-encryption algorithm and any associated parameters used to encrypt the content encryption key.


### -field EncryptedKey

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> that contains the bytes of the encrypted session key.

