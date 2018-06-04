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

# _ENCRYPTION_CERTIFICATE_HASH structure


## -description


Contains a certificate hash and display information for the certificate.


## -struct-fields




### -field cbTotalLength

The length of this structure, in bytes.


### -field pUserSid

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> of the user who created the certificate. This member is optional and can be <b>NULL</b>.


### -field pHash

A pointer to an 
<a href="https://msdn.microsoft.com/23a172be-6e94-4a1f-afde-fc9437443c7a">EFS_HASH_BLOB</a> structure.


### -field lpDisplayInformation

User-displayable information for the certificate.  This is usually the user's common name and universal principal name (UPN).


### -field lpDisplayInformation.string

 




## -see-also




<a href="https://msdn.microsoft.com/23a172be-6e94-4a1f-afde-fc9437443c7a">EFS_HASH_BLOB</a>



<a href="https://msdn.microsoft.com/988159b3-3cb9-4a4d-9c68-ebfb309cff25">ENCRYPTION_CERTIFICATE_HASH_LIST</a>



<a href="https://msdn.microsoft.com/5f20109f-727d-44a9-90a1-0adc19b00d28">File Encryption</a>
 

 

