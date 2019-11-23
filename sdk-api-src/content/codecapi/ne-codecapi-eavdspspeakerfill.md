---
UID: NE:codecapi.eAVDSPSpeakerFill
title: eAVDSPSpeakerFill (codecapi.h)

description: Specifies whether speaker fill is enabled in an audio decoder or digital signal processor (DSP).
old-location: dshow\eavdspspeakerfill.htm
tech.root: DirectShow
ms.assetid: 74afd030-bce6-4fb1-b937-2279c1e96264

ms.date: 12/05/2018
ms.keywords: codecapi/eAVDSPSpeakerFill, codecapi/eAVDSPSpeakerFill_AUTO, codecapi/eAVDSPSpeakerFill_OFF, codecapi/eAVDSPSpeakerFill_ON, dshow.eavdspspeakerfill, eAVDSPSpeakerFill, eAVDSPSpeakerFill enumeration [DirectShow], eAVDSPSpeakerFill_AUTO, eAVDSPSpeakerFill_OFF, eAVDSPSpeakerFill_ON
ms.topic: enum
f1_keywords: 
 - "codecapi/eAVDSPSpeakerFill"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# eAVDSPSpeakerFill enumeration


## -description


Specifies whether speaker fill is enabled in an audio decoder or digital signal processor (DSP). This enumeration is used with the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/avdspspeakerfill-property">AVDSPSpeakerFill</a> property.


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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
 

 

