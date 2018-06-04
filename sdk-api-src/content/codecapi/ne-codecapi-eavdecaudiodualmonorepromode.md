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

# eAVDecAudioDualMonoReproMode enumeration


## -description



Specifies how the decoder reproduces dual mono audio. This enumeration is used with the <a href="https://msdn.microsoft.com/3ef1f52c-13b2-4d9f-99fe-3317846be8a0">AVDecAudioDualMonoReproMode</a> property.




## -enum-fields




### -field eAVDecAudioDualMonoReproMode_STEREO

Output channel 1 (Ch1) to the left speaker and channel 2 (Ch2) to the right speaker.


### -field eAVDecAudioDualMonoReproMode_LEFT_MONO

Output Ch1 to the left and right speakers.


### -field eAVDecAudioDualMonoReproMode_RIGHT_MONO

Output Ch2 to the left and right speakers.


### -field eAVDecAudioDualMonoReproMode_MIX_MONO

Mix Ch1 and Ch2 and output the mix to the left and right speakers.


## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI Interface</a>
 

 

