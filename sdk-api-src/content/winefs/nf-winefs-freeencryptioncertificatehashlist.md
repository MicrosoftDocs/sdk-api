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

# FreeEncryptionCertificateHashList function


## -description


Frees a certificate hash list.


## -parameters




### -param pUsers

TBD




#### - pHashes [in]

A pointer to a certificate hash list structure, 
<a href="https://msdn.microsoft.com/988159b3-3cb9-4a4d-9c68-ebfb309cff25">ENCRYPTION_CERTIFICATE_HASH_LIST</a>, which was returned by the 
<a href="https://msdn.microsoft.com/1bdab753-e7f2-4c08-8b37-3903c0842227">QueryUsersOnEncryptedFile</a> or 
<a href="https://msdn.microsoft.com/2f8d0673-3c87-46a4-b7d5-3888d20bd9b8">QueryRecoveryAgentsOnEncryptedFile</a> function.


## -returns



This function does not return a value.




## -remarks



<b>ReFS:  </b>This function is not supported.




## -see-also




<a href="https://msdn.microsoft.com/988159b3-3cb9-4a4d-9c68-ebfb309cff25">ENCRYPTION_CERTIFICATE_HASH_LIST</a>



<a href="https://msdn.microsoft.com/5f20109f-727d-44a9-90a1-0adc19b00d28">File Encryption</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/2f8d0673-3c87-46a4-b7d5-3888d20bd9b8">QueryRecoveryAgentsOnEncryptedFile</a>



<a href="https://msdn.microsoft.com/1bdab753-e7f2-4c08-8b37-3903c0842227">QueryUsersOnEncryptedFile</a>
 

 

