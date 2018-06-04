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

# eAVEncMPVFrameFieldMode enumeration


## -description



Specifies whether the encoder produces encoded fields or encoded frames. This enumeration is used with the <a href="https://msdn.microsoft.com/bf21ea55-662f-4a69-8528-67592b8b8645">AVEncMPVFrameFieldMode</a> property.




## -enum-fields




### -field eAVEncMPVFrameFieldMode_FieldMode

The encoder produces an MPEG picture for each field in the source video.


### -field eAVEncMPVFrameFieldMode_FrameMode

The encoder produces an MPEG picture for each frame (or pair of fields) in the source video.


## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI Interface</a>
 

 

