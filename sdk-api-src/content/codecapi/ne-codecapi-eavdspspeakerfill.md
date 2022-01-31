---
UID: NE:codecapi.eAVDSPSpeakerFill
title: eAVDSPSpeakerFill (codecapi.h)
description: Specifies whether speaker fill is enabled in an audio decoder or digital signal processor (DSP).
helpviewer_keywords: ["codecapi/eAVDSPSpeakerFill","codecapi/eAVDSPSpeakerFill_AUTO","codecapi/eAVDSPSpeakerFill_OFF","codecapi/eAVDSPSpeakerFill_ON","dshow.eavdspspeakerfill","eAVDSPSpeakerFill","eAVDSPSpeakerFill enumeration [DirectShow]","eAVDSPSpeakerFill_AUTO","eAVDSPSpeakerFill_OFF","eAVDSPSpeakerFill_ON"]
old-location: dshow\eavdspspeakerfill.htm
tech.root: dshow
ms.assetid: 74afd030-bce6-4fb1-b937-2279c1e96264
ms.date: 12/05/2018
ms.keywords: codecapi/eAVDSPSpeakerFill, codecapi/eAVDSPSpeakerFill_AUTO, codecapi/eAVDSPSpeakerFill_OFF, codecapi/eAVDSPSpeakerFill_ON, dshow.eavdspspeakerfill, eAVDSPSpeakerFill, eAVDSPSpeakerFill enumeration [DirectShow], eAVDSPSpeakerFill_AUTO, eAVDSPSpeakerFill_OFF, eAVDSPSpeakerFill_ON
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - eAVDSPSpeakerFill
 - codecapi/eAVDSPSpeakerFill
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - codecapi.h
api_name:
 - eAVDSPSpeakerFill
---

# eAVDSPSpeakerFill enumeration


## -description

Specifies whether speaker fill is enabled in an audio decoder or digital signal processor (DSP). This enumeration is used with the <a href="/windows/desktop/DirectShow/avdspspeakerfill-property">AVDSPSpeakerFill</a> property.

## -enum-fields

### -field eAVDSPSpeakerFill_OFF:0

Speaker fill is disabled.

### -field eAVDSPSpeakerFill_ON:1

Speaker fill is enabled.

### -field eAVDSPSpeakerFill_AUTO:2

The decoder or DSP automatically selects the speaker fill mode.

## -remarks

Speaker fill is a DSP process that converts mono or stereo audio into multichannel audio.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
