---
UID: NE:codecapi.eAVDSPSpeakerFill
title: eAVDSPSpeakerFill
author: windows-sdk-content
description: Specifies whether speaker fill is enabled in an audio decoder or digital signal processor (DSP).
old-location: dshow\eavdspspeakerfill.htm
tech.root: DirectShow
ms.assetid: 74afd030-bce6-4fb1-b937-2279c1e96264
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: codecapi/eAVDSPSpeakerFill, codecapi/eAVDSPSpeakerFill_AUTO, codecapi/eAVDSPSpeakerFill_OFF, codecapi/eAVDSPSpeakerFill_ON, dshow.eavdspspeakerfill, eAVDSPSpeakerFill, eAVDSPSpeakerFill enumeration [DirectShow], eAVDSPSpeakerFill_AUTO, eAVDSPSpeakerFill_OFF, eAVDSPSpeakerFill_ON
ms.prod: windows
ms.technology: windows-sdk
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
 - eAVDSPSpeakerFill
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

