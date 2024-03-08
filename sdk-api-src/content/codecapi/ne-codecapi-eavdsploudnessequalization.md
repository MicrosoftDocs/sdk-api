---
UID: NE:codecapi.eAVDSPLoudnessEqualization
title: eAVDSPLoudnessEqualization (codecapi.h)
description: Specifies whether loudness equalization is enabled in an audio decoder or digital signal processor (DSP).
helpviewer_keywords: ["codecapi/eAVDSPLoudnessEqualization","codecapi/eAVDSPLoudnessEqualization_AUTO","codecapi/eAVDSPLoudnessEqualization_OFF","codecapi/eAVDSPLoudnessEqualization_ON","dshow.eavdsploudnessequalization","eAVDSPLoudnessEqualization","eAVDSPLoudnessEqualization enumeration [DirectShow]","eAVDSPLoudnessEqualization_AUTO","eAVDSPLoudnessEqualization_OFF","eAVDSPLoudnessEqualization_ON"]
old-location: dshow\eavdsploudnessequalization.htm
tech.root: dshow
ms.assetid: bb46653e-d17d-4899-8a0b-cee8c4d68993
ms.date: 4/26/2023
ms.keywords: codecapi/eAVDSPLoudnessEqualization, codecapi/eAVDSPLoudnessEqualization_AUTO, codecapi/eAVDSPLoudnessEqualization_OFF, codecapi/eAVDSPLoudnessEqualization_ON, dshow.eavdsploudnessequalization, eAVDSPLoudnessEqualization, eAVDSPLoudnessEqualization enumeration [DirectShow], eAVDSPLoudnessEqualization_AUTO, eAVDSPLoudnessEqualization_OFF, eAVDSPLoudnessEqualization_ON
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
 - eAVDSPLoudnessEqualization
 - codecapi/eAVDSPLoudnessEqualization
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
 - eAVDSPLoudnessEqualization
---

# eAVDSPLoudnessEqualization enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies whether loudness equalization is enabled in an audio decoder or digital signal processor (DSP). This enumeration is used with the <a href="/windows/desktop/DirectShow/avdsploudnessequalization-property">AVDSPLoudnessEqualization</a> property.

## -enum-fields

### -field eAVDSPLoudnessEqualization_OFF:0

Loudness equalization is disabled.

### -field eAVDSPLoudnessEqualization_ON:1

Loudness equalization is enabled.

### -field eAVDSPLoudnessEqualization_AUTO:2

The decoder or DSP automatically selects the equalization mode.

## -remarks

Loudness equalization is a DSP process that maintains a consistent volume level when the audio stream changes.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
