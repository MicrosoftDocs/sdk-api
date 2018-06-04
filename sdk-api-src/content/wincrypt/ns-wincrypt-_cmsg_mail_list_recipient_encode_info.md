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

# _CMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO structure


## -description


The <b>CMSG_MAIL_LIST_RECIPIENT_ENCODE_INFO</b> structure is used with previously distributed <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">symmetric keys</a> for decrypting the content key encryption key (KEK).


## -struct-fields




### -field cbSize

The size, in bytes, of this data structure.


### -field KeyEncryptionAlgorithm

A 
						<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that indicates the encryption algorithm used.


### -field pvKeyEncryptionAuxInfo

A pointer to a structure that contains any additional encryption information.


### -field hCryptProv

The provider used to do the recipient key encryption and export. If <b>NULL</b>, the provider specified in <a href="https://msdn.microsoft.com/87712541-2806-4709-a7cf-c9ba966c96fd">CMSG_ENVELOPED_ENCODE_INFO</a> is used.
					


### -field dwKeyChoice

Indicates which member of the following union will be used. Currently only CMSG_MAIL_LIST_HANDLE_KEY_CHOICE can be used.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.hKeyEncryptionKey

An <b>HCRYPTKEY</b> value used with the CMSG_MAIL_LIST_HANDLE_KEY_CHOICE value of the <i>dwKeyChoice</i> parameter.


### -field DUMMYUNIONNAME.pvKeyEncryptionKey

A pointer to a void. Reserved for a future potential pointer choice. 



### -field KeyId


						A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> key identifier of the key-encryption key that was previously distributed to the message sender and one or more recipients.


### -field Date

Optional <b>FILETIME</b> value. When present, specifies a single key encryption key (KEK) from a set that was previously distributed.


### -field pOtherAttr

Optional pointer to a 
<a href="https://msdn.microsoft.com/84057581-d0a9-464a-9399-ba806e37516f">CRYPT_ATTRIBUTE_TYPE_VALUE</a> structure that contains encryption attributes.

