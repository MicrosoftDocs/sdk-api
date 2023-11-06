---
UID: NE:codecapi.eAVEncDDHeadphoneMode
title: eAVEncDDHeadphoneMode (codecapi.h)
description: Specifies headphone mode for a Dolby Digital audio stream. This enumeration is used with the AVEncDDHeadphoneMode property.
helpviewer_keywords: ["codecapi/eAVEncDDHeadphoneMode","codecapi/eAVEncDDHeadphoneMode_Encoded","codecapi/eAVEncDDHeadphoneMode_NotEncoded","codecapi/eAVEncDDHeadphoneMode_NotIndicated","dshow.eavencddheadphonemode","eAVEncDDHeadphoneMode","eAVEncDDHeadphoneMode enumeration [DirectShow]","eAVEncDDHeadphoneMode_Encoded","eAVEncDDHeadphoneMode_NotEncoded","eAVEncDDHeadphoneMode_NotIndicated"]
old-location: dshow\eavencddheadphonemode.htm
tech.root: dshow
ms.assetid: 8739334c-bbaa-482e-9113-d4a885f98913
ms.date: 4/26/2023
ms.keywords: codecapi/eAVEncDDHeadphoneMode, codecapi/eAVEncDDHeadphoneMode_Encoded, codecapi/eAVEncDDHeadphoneMode_NotEncoded, codecapi/eAVEncDDHeadphoneMode_NotIndicated, dshow.eavencddheadphonemode, eAVEncDDHeadphoneMode, eAVEncDDHeadphoneMode enumeration [DirectShow], eAVEncDDHeadphoneMode_Encoded, eAVEncDDHeadphoneMode_NotEncoded, eAVEncDDHeadphoneMode_NotIndicated
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
 - eAVEncDDHeadphoneMode
 - codecapi/eAVEncDDHeadphoneMode
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
 - eAVEncDDHeadphoneMode
---

# eAVEncDDHeadphoneMode enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies headphone mode for a Dolby Digital audio stream. This enumeration is used with the <a href="/windows/desktop/DirectShow/avencddheadphonemode-property">AVEncDDHeadphoneMode</a> property.

## -enum-fields

### -field eAVEncDDHeadphoneMode_NotIndicated:0

Headphone mode is not indicated.

### -field eAVEncDDHeadphoneMode_NotEncoded:1

Headphone mode is disabled.

### -field eAVEncDDHeadphoneMode_Encoded:2

Headphone mode is enabled.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
