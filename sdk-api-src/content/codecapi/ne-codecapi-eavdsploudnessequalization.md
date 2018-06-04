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

# eAVDSPLoudnessEqualization enumeration


## -description


Specifies whether loudness equalization is enabled in an audio decoder or digital signal processor (DSP). This enumeration is used with the <a href="https://msdn.microsoft.com/f02b187f-1bcb-47b3-8ac2-018ed30491c6">AVDSPLoudnessEqualization</a> property.


## -enum-fields




### -field eAVDSPLoudnessEqualization_OFF

Loudness equalization is disabled.


### -field eAVDSPLoudnessEqualization_ON

Loudness equalization is enabled.


### -field eAVDSPLoudnessEqualization_AUTO

The decoder or DSP automatically selects the equalization mode.


## -remarks



Loudness equalization is a DSP process that maintains a consistent volume level when the audio stream changes.




## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI Interface</a>
 

 

