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

# _CERT_LOGOTYPE_DETAILS structure


## -description


The <b>CERT_LOGOTYPE_DETAILS</b> structure contains additional information about a logotype.


## -struct-fields




### -field pwszMimeType

The address of a null-terminated Unicode string that contains the Multipurpose Internet Mail Extensions (MIME) type of the logotype.


### -field cHashedUrl

The number of elements in the <b>rgHashedUrl</b> array.


### -field rgHashedUrl

An array of <a href="https://msdn.microsoft.com/961feb88-b924-4834-bc68-d87f410259f1">CERT_HASHED_URL</a> structures that contain the hashed URLs of the logotype. The <b>cHashedUrl</b> member contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/97357faa-2720-4240-a3c3-77abdce8d86d">CERT_LOGOTYPE_AUDIO</a>



<a href="https://msdn.microsoft.com/d1dff71c-41e1-4f02-93b4-019d688ed012">CERT_LOGOTYPE_IMAGE</a>
 

 

