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

# eAVDecAudioDualMono enumeration


## -description



Specifies whether the input audio stream is stereo or dual mono. This enumeration is used with the <a href="https://msdn.microsoft.com/96cb9e17-588c-4a1a-a7ba-7f8439d5b79a">AVDecAudioDualMono</a> property.




## -enum-fields




### -field eAVDecAudioDualMono_IsNotDualMono

The input bit stream is not dual mono.


### -field eAVDecAudioDualMono_IsDualMono

The input bit stream is dual mono.


### -field eAVDecAudioDualMono_UnSpecified

There is no indication in the bit stream whether the audio is dual mono.


## -remarks



In dual mono encoding, each channel is encoded separately. In stereo encoding, both channels are encoded together.




## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI Interface</a>
 

 

