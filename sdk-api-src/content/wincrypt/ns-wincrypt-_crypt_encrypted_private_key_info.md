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

# _CRYPT_ENCRYPTED_PRIVATE_KEY_INFO structure


## -description


<p class="CCE_Message">[The <b>CRYPT_ENCRYPTED_PRIVATE_KEY_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPT_ENCRYPTED_PRIVATE_KEY_INFO</b> structure contains the information in a PKCS #8
EncryptedPrivateKeyInfo ASN.1 type found in the PKCS #8 standard.


## -struct-fields




### -field EncryptionAlgorithm

A <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that indicates the algorithm used for encryption.


### -field EncryptedPrivateKey

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that contains the encrypted private key data.


## -see-also




<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="https://msdn.microsoft.com/82fee86a-8704-4f22-8f11-f89509c5a0aa">CryptExportPKCS8Ex</a>



<a href="https://msdn.microsoft.com/f59fd46b-5430-4aa2-85ba-961b416dbaac">PCRYPT_DECRYPT_PRIVATE_KEY_FUNC</a>



<a href="https://msdn.microsoft.com/aa6b8bca-4f0d-491e-ab38-5c273a01ca05">PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC</a>
 

 

