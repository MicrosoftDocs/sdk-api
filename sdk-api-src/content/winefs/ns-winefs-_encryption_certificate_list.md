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

# _ENCRYPTION_CERTIFICATE_LIST structure


## -description


Contains a list of certificates.


## -struct-fields




### -field nUsers

The number of certificates in the list.


### -field nUsers.range

 


### -field nUsers.range.0

 


### -field nUsers.range.500

 


### -field pUsers

A pointer to the first 
						<a href="https://msdn.microsoft.com/33b36659-48bb-4297-8142-f8702db03d20">ENCRYPTION_CERTIFICATE</a> structure in the list.


### -field pUsers.size_is

 


### -field pUsers.size_is.nUsers

 




## -see-also




<a href="https://msdn.microsoft.com/a92d6a52-20d1-4d5c-a222-ab9afaf85c4b">AddUsersToEncryptedFile</a>



<a href="https://msdn.microsoft.com/33b36659-48bb-4297-8142-f8702db03d20">ENCRYPTION_CERTIFICATE</a>



<a href="https://msdn.microsoft.com/5f20109f-727d-44a9-90a1-0adc19b00d28">File Encryption</a>
 

 

