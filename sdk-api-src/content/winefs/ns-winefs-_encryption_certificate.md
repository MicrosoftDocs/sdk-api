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

# _ENCRYPTION_CERTIFICATE structure


## -description


Contains a certificate and the SID of its owner.


## -struct-fields




### -field cbTotalLength

The length of this structure, in bytes.


### -field pUserSid

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> of the user who owns the certificate.


### -field pCertBlob

A pointer to an 
<a href="https://msdn.microsoft.com/e0d0aa0a-ac87-4734-93d0-30c2080319e8">EFS_CERTIFICATE_BLOB</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/e0d0aa0a-ac87-4734-93d0-30c2080319e8">EFS_CERTIFICATE_BLOB</a>



<a href="https://msdn.microsoft.com/e1914b96-2fba-49ed-9dd2-464659323eda">ENCRYPTION_CERTIFICATE_LIST</a>



<a href="https://msdn.microsoft.com/5f20109f-727d-44a9-90a1-0adc19b00d28">File Encryption</a>



<a href="https://msdn.microsoft.com/dd23fab7-1675-4d0d-911c-e2aac2273e7f">SetUserFileEncryptionKey</a>
 

 

