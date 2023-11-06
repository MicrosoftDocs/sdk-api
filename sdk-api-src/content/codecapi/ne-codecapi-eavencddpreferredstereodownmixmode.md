---
UID: NE:codecapi.eAVEncDDPreferredStereoDownMixMode
title: eAVEncDDPreferredStereoDownMixMode (codecapi.h)
description: Specifies the preferred stereo downmix mode for a Dolby Digital audio stream. This enumeration is used with the AVEncDDPreferredStereoDownMixMode property.
helpviewer_keywords: ["codecapi/eAVEncDDPreferredStereoDownMixMode","codecapi/eAVEncDDPreferredStereoDownMixMode_LoRo","codecapi/eAVEncDDPreferredStereoDownMixMode_LtRt","dshow.eavencddpreferredstereodownmixmode","eAVEncDDPreferredStereoDownMixMode","eAVEncDDPreferredStereoDownMixMode enumeration [DirectShow]","eAVEncDDPreferredStereoDownMixMode_LoRo","eAVEncDDPreferredStereoDownMixMode_LtRt"]
old-location: dshow\eavencddpreferredstereodownmixmode.htm
tech.root: dshow
ms.assetid: 3960d0d5-9d82-4ed5-843d-04fdb0538438
ms.date: 4/26/2023
ms.keywords: codecapi/eAVEncDDPreferredStereoDownMixMode, codecapi/eAVEncDDPreferredStereoDownMixMode_LoRo, codecapi/eAVEncDDPreferredStereoDownMixMode_LtRt, dshow.eavencddpreferredstereodownmixmode, eAVEncDDPreferredStereoDownMixMode, eAVEncDDPreferredStereoDownMixMode enumeration [DirectShow], eAVEncDDPreferredStereoDownMixMode_LoRo, eAVEncDDPreferredStereoDownMixMode_LtRt
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
 - eAVEncDDPreferredStereoDownMixMode
 - codecapi/eAVEncDDPreferredStereoDownMixMode
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
 - eAVEncDDPreferredStereoDownMixMode
---

# eAVEncDDPreferredStereoDownMixMode enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies the preferred stereo downmix mode for a Dolby Digital audio stream. This enumeration is used with the <a href="/windows/desktop/DirectShow/avencddpreferredstereodownmixmode-property">AVEncDDPreferredStereoDownMixMode</a> property.

## -enum-fields

### -field eAVEncDDPreferredStereoDownMixMode_LtRt:0

Left total/right total (Lt/Rt) downmix.

### -field eAVEncDDPreferredStereoDownMixMode_LoRo:1

Left only/right only (Lo/Ro) downmix.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
