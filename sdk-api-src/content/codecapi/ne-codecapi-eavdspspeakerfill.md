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

# eAVDSPSpeakerFill enumeration


## -description


Specifies whether speaker fill is enabled in an audio decoder or digital signal processor (DSP). This enumeration is used with the <a href="https://msdn.microsoft.com/5a42d4c9-d593-4d7f-bfee-37271c48e5cf">AVDSPSpeakerFill</a> property.


## -enum-fields




### -field eAVDSPSpeakerFill_OFF

Speaker fill is disabled.


### -field eAVDSPSpeakerFill_ON

Speaker fill is enabled.


### -field eAVDSPSpeakerFill_AUTO

The decoder or DSP automatically selects the speaker fill mode.


## -remarks



Speaker fill is a DSP process that converts mono or stereo audio into multichannel audio.




## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI Interface</a>
 

 

