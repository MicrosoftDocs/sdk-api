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

# _CRYPT_IMAGE_REG structure


## -description


The <b>CRYPT_IMAGE_REG</b> structure contains image registration information about a CNG provider.


## -struct-fields




### -field pszImage

A pointer to a null-terminated Unicode string that contains only the file name of the provider module.


### -field cInterfaces

Contains the number of elements in the <b>rgpInterfaces</b> array.


### -field rgpInterfaces

A pointer to an array of <a href="https://msdn.microsoft.com/80204d2a-ebc8-40f6-bccb-7cd112d7769b">CRYPT_INTERFACE_REG</a> structure pointers that specify the types of cryptographic interfaces that are supported by the provider. For example, if the provider supports both a cipher interface (<b>BCRYPT_CIPHER_INTERFACE</b>) and a hash interface (<b>BCRYPT_HASH_INTERFACE</b>), this array would contain two <b>CRYPT_INTERFACE_REG</b> structure pointers, one for the cipher interface and one for the hash interface.


## -see-also




<a href="https://msdn.microsoft.com/ca0ac386-9435-49f0-95fe-503aa7183517">CRYPT_PROVIDER_REG</a>
 

 

