---
UID: NE:codecapi.eAVAudioChannelConfig
title: eAVAudioChannelConfig
author: windows-sdk-content
description: Specifies the speaker configuration for the audio channels in the audio bit stream. This enumeration is used with the AVAudioChannelConfig property.
old-location: dshow\eavaudiochannelconfig.htm
tech.root: DirectShow
ms.assetid: 8835b00b-048b-404a-9ecc-84baeb70df66
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: codecapi/eAVAudioChannelConfig, codecapi/eAVAudioChannelConfig_BACK_CENTER, codecapi/eAVAudioChannelConfig_BACK_LEFT, codecapi/eAVAudioChannelConfig_BACK_RIGHT, codecapi/eAVAudioChannelConfig_FRONT_CENTER, codecapi/eAVAudioChannelConfig_FRONT_LEFT, codecapi/eAVAudioChannelConfig_FRONT_LEFT_OF_CENTER, codecapi/eAVAudioChannelConfig_FRONT_RIGHT, codecapi/eAVAudioChannelConfig_FRONT_RIGHT_OF_CENTER, codecapi/eAVAudioChannelConfig_LOW_FREQUENCY, codecapi/eAVAudioChannelConfig_SIDE_LEFT, codecapi/eAVAudioChannelConfig_SIDE_RIGHT, codecapi/eAVAudioChannelConfig_TOP_BACK_CENTER, codecapi/eAVAudioChannelConfig_TOP_BACK_LEFT, codecapi/eAVAudioChannelConfig_TOP_BACK_RIGHT, codecapi/eAVAudioChannelConfig_TOP_CENTER, codecapi/eAVAudioChannelConfig_TOP_FRONT_CENTER, codecapi/eAVAudioChannelConfig_TOP_FRONT_LEFT, codecapi/eAVAudioChannelConfig_TOP_FRONT_RIGHT, dshow.eavaudiochannelconfig, eAVAudioChannelConfig, eAVAudioChannelConfig enumeration [DirectShow], eAVAudioChannelConfigEnumeration, eAVAudioChannelConfig_BACK_CENTER, eAVAudioChannelConfig_BACK_LEFT, eAVAudioChannelConfig_BACK_RIGHT, eAVAudioChannelConfig_FRONT_CENTER, eAVAudioChannelConfig_FRONT_LEFT, eAVAudioChannelConfig_FRONT_LEFT_OF_CENTER, eAVAudioChannelConfig_FRONT_RIGHT, eAVAudioChannelConfig_FRONT_RIGHT_OF_CENTER, eAVAudioChannelConfig_LOW_FREQUENCY, eAVAudioChannelConfig_SIDE_LEFT, eAVAudioChannelConfig_SIDE_RIGHT, eAVAudioChannelConfig_TOP_BACK_CENTER, eAVAudioChannelConfig_TOP_BACK_LEFT, eAVAudioChannelConfig_TOP_BACK_RIGHT, eAVAudioChannelConfig_TOP_CENTER, eAVAudioChannelConfig_TOP_FRONT_CENTER, eAVAudioChannelConfig_TOP_FRONT_LEFT, eAVAudioChannelConfig_TOP_FRONT_RIGHT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - codecapi.h
api_name:
 - eAVAudioChannelConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



These values correspond to the flags used for the <b>dwChannelMask</b> member of the <a href="https://msdn.microsoft.com/b16cdcab-fa4f-4c9a-b1f3-af459bd33245">WAVEFORMATEXTENSIBLE</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI Interface</a>
 

 

