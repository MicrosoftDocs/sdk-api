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

# tagRemSNB structure


## -description



			The 
<b>RemSNB</b> structure is used for marshaling the 
<a href="https://msdn.microsoft.com/8428a820-3d8a-41e0-9955-d355440e2ebc">SNB</a> data type.

Defined in the 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface (Storag.idl).


## -struct-fields




### -field ulCntStr

Number of strings in the <b>rgString</b> buffer.


### -field ulCntChar

Size in bytes of the <b>rgString</b> buffer.


### -field rgString

Pointer to an array of bytes containing the stream name strings from the <b>SNB</b> structure.


## -see-also




<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a>
 

 

