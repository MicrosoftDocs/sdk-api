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

# eAVAudioChannelConfig enumeration


## -description



Specifies the speaker configuration for the audio channels in the audio bit stream. This enumeration is used with the <a href="https://msdn.microsoft.com/ec13bb55-47af-4d79-9560-d297bce8e236">AVAudioChannelConfig</a> property.




## -enum-fields




### -field eAVAudioChannelConfig_FRONT_LEFT

Front left


### -field eAVAudioChannelConfig_FRONT_RIGHT

Front right


### -field eAVAudioChannelConfig_FRONT_CENTER

Front center


### -field eAVAudioChannelConfig_LOW_FREQUENCY

Low frequency effect (LFE)


### -field eAVAudioChannelConfig_BACK_LEFT

Back left


### -field eAVAudioChannelConfig_BACK_RIGHT

Back right


### -field eAVAudioChannelConfig_FRONT_LEFT_OF_CENTER

Front, left of center


### -field eAVAudioChannelConfig_FRONT_RIGHT_OF_CENTER

Front, right of center


### -field eAVAudioChannelConfig_BACK_CENTER

Back center


### -field eAVAudioChannelConfig_SIDE_LEFT

Side left


### -field eAVAudioChannelConfig_SIDE_RIGHT

Side right


### -field eAVAudioChannelConfig_TOP_CENTER

Top center


### -field eAVAudioChannelConfig_TOP_FRONT_LEFT

Top, front left


### -field eAVAudioChannelConfig_TOP_FRONT_CENTER

Top, front center


### -field eAVAudioChannelConfig_TOP_FRONT_RIGHT

Top, front right


### -field eAVAudioChannelConfig_TOP_BACK_LEFT

Top, back left


### -field eAVAudioChannelConfig_TOP_BACK_CENTER

Top, back center


### -field eAVAudioChannelConfig_TOP_BACK_RIGHT

Top, back right


## -remarks



These values correspond to the flags used for the <b>dwChannelMask</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff538802">WAVEFORMATEXTENSIBLE</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI Interface</a>
 

 

