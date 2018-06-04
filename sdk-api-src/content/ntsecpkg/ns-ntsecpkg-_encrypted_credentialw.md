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

# _ENCRYPTED_CREDENTIALW structure


## -description


Represents an encrypted credential.


## -struct-fields




### -field Cred

A pointer to a <a href="https://msdn.microsoft.com/6361b93c-4441-4a01-bd39-b95c42962497">CREDENTIAL</a> structure that contains the encrypted credential.


### -field ClearCredentialBlobSize

The size, in bytes, of the unencrypted credential.


## -see-also




<a href="https://msdn.microsoft.com/9da22201-884d-4822-a769-c2ce0d36ec73">CrediFreeCredentials</a>



<a href="https://msdn.microsoft.com/b6abfde9-74ac-4af0-b8ab-4f6be937f17f">CrediRead</a>



<a href="https://msdn.microsoft.com/fa5c92be-c74b-4143-8526-b60c25461b8c">CrediReadDomainCredentials</a>



<a href="https://msdn.microsoft.com/19c7fe4d-9c7b-4547-baab-443483deb013">CrediWrite</a>



<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

