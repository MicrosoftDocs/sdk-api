---
UID: NE:codecapi.eAVEncVideoOutputFrameRateConversion
title: eAVEncVideoOutputFrameRateConversion (codecapi.h)
description: Specifies whether the encoder converts the frame rate, if the output frame rate does not match the input frame rate. This enumeration is used with the AVEncVideoOutputFrameRateConversion property.
helpviewer_keywords: ["codecapi/eAVEncVideoOutputFrameRateConversion","codecapi/eAVEncVideoOutputFrameRateConversion_Alias","codecapi/eAVEncVideoOutputFrameRateConversion_Disable","codecapi/eAVEncVideoOutputFrameRateConversion_Enable","dshow.eavencvideooutputframerateconversion","eAVEncVideoOutputFrameRateConversion","eAVEncVideoOutputFrameRateConversion enumeration [DirectShow]","eAVEncVideoOutputFrameRateConversionEnumeration","eAVEncVideoOutputFrameRateConversion_Alias","eAVEncVideoOutputFrameRateConversion_Disable","eAVEncVideoOutputFrameRateConversion_Enable"]
old-location: dshow\eavencvideooutputframerateconversion.htm
tech.root: dshow
ms.assetid: 0303f49c-9651-4781-8a6b-2af0a1b8f1ab
ms.date: 4/26/2023
ms.keywords: codecapi/eAVEncVideoOutputFrameRateConversion, codecapi/eAVEncVideoOutputFrameRateConversion_Alias, codecapi/eAVEncVideoOutputFrameRateConversion_Disable, codecapi/eAVEncVideoOutputFrameRateConversion_Enable, dshow.eavencvideooutputframerateconversion, eAVEncVideoOutputFrameRateConversion, eAVEncVideoOutputFrameRateConversion enumeration [DirectShow], eAVEncVideoOutputFrameRateConversionEnumeration, eAVEncVideoOutputFrameRateConversion_Alias, eAVEncVideoOutputFrameRateConversion_Disable, eAVEncVideoOutputFrameRateConversion_Enable
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
 - eAVEncVideoOutputFrameRateConversion
 - codecapi/eAVEncVideoOutputFrameRateConversion
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
 - eAVEncVideoOutputFrameRateConversion
---

# eAVEncVideoOutputFrameRateConversion enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies whether the encoder converts the frame rate, if the output frame rate does not match the input frame rate. This enumeration is used with the <b>AVEncVideoOutputFrameRateConversion</b> property.

## -enum-fields

### -field eAVEncVideoOutputFrameRateConversion_Disable:0

Disable frame rate conversion.

### -field eAVEncVideoOutputFrameRateConversion_Enable:1

Enable frame rate conversion.

### -field eAVEncVideoOutputFrameRateConversion_Alias:2

Change the time stamps on the samples, but do not interpolate the time stamps.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
