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

# _SEC_WINNT_AUTH_CERTIFICATE_DATA structure


## -description


Specifies serialized certificate information.


## -struct-fields




### -field cbHeaderLength

The size, in bytes,  of the structure header.


### -field cbStructureLength

The size, in bytes, of the certificate information.


### -field Certificate

A structure that specifies the offset from the beginning of this structure and the size, in bytes, of the certificate data.


## -see-also




<a href="https://msdn.microsoft.com/ee511497-2b70-4c51-bcc2-7585143b4f43">SEC_WINNT_AUTH_BYTE_VECTOR</a>
 

 

