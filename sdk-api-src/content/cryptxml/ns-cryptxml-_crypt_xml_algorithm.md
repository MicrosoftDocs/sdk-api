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

# _CRYPT_XML_ALGORITHM structure


## -description


The <b>CRYPT_XML_ALGORITHM</b> structure specifies the algorithm used to sign or transform the message.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field wszAlgorithm

A pointer to a null-terminated Unicode string that contains the <b>Algorithm</b> attribute. 
    When the <b>Encoded</b> member contains an element that is proved by an application, this member is set to <b>NULL</b>.XML 


### -field Encoded

Optional.  The XML encoded element. 
    This member  is set when an element tag is present in the XML signature.


## -see-also




<b></b>



<a href="https://msdn.microsoft.com/012bad01-228a-4bb0-b883-0c2c7abd9271">Digital Signature Cryptographic Algorithms</a>
 

 

