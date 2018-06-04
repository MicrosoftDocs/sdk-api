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

