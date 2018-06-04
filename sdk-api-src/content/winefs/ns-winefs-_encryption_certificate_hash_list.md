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

# _ENCRYPTION_CERTIFICATE_HASH_LIST structure


## -description


Contains a list of certificate hashes.


## -struct-fields




### -field nCert_Hash

The number of certificate hashes in the list.


### -field nCert_Hash.range

 


### -field nCert_Hash.range.0

 


### -field nCert_Hash.range.500

 


### -field pUsers

A pointer to the first 
<a href="https://msdn.microsoft.com/6930446c-5338-4ff9-a662-791fc9e7cefe">ENCRYPTION_CERTIFICATE_HASH</a> structure in the list. 


### -field pUsers.size_is

 


### -field pUsers.size_is.nCert_Hash

 




## -see-also




<a href="https://msdn.microsoft.com/6930446c-5338-4ff9-a662-791fc9e7cefe">ENCRYPTION_CERTIFICATE_HASH</a>



<a href="https://msdn.microsoft.com/5f20109f-727d-44a9-90a1-0adc19b00d28">File Encryption</a>



<a href="https://msdn.microsoft.com/63d5811f-a135-45b0-8f23-fd8851f7bcca">FreeEncryptionCertificateHashList</a>



<a href="https://msdn.microsoft.com/2f8d0673-3c87-46a4-b7d5-3888d20bd9b8">QueryRecoveryAgentsOnEncryptedFile</a>



<a href="https://msdn.microsoft.com/1bdab753-e7f2-4c08-8b37-3903c0842227">QueryUsersOnEncryptedFile</a>



<a href="https://msdn.microsoft.com/c6672581-24b4-464c-b32d-48a04e56eef8">RemoveUsersFromEncryptedFile</a>
 

 

