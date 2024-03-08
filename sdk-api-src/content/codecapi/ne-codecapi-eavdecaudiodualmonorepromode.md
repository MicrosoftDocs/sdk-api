---
UID: NE:codecapi.eAVDecAudioDualMonoReproMode
title: eAVDecAudioDualMonoReproMode (codecapi.h)
description: Specifies how the decoder reproduces dual mono audio. This enumeration is used with the AVDecAudioDualMonoReproMode property.
helpviewer_keywords: ["codecapi/eAVDecAudioDualMonoReproMode","codecapi/eAVDecAudioDualMonoReproMode_LEFT_MONO","codecapi/eAVDecAudioDualMonoReproMode_MIX_MONO","codecapi/eAVDecAudioDualMonoReproMode_RIGHT_MONO","codecapi/eAVDecAudioDualMonoReproMode_STEREO","dshow.eavdecaudiodualmonorepromode","eAVDecAudioDualMonoReproMode","eAVDecAudioDualMonoReproMode enumeration [DirectShow]","eAVDecAudioDualMonoReproModeEnumeration","eAVDecAudioDualMonoReproMode_LEFT_MONO","eAVDecAudioDualMonoReproMode_MIX_MONO","eAVDecAudioDualMonoReproMode_RIGHT_MONO","eAVDecAudioDualMonoReproMode_STEREO"]
old-location: dshow\eavdecaudiodualmonorepromode.htm
tech.root: dshow
ms.assetid: 16374617-8342-4e8c-b52a-c5a419998699
ms.date: 4/26/2023
ms.keywords: codecapi/eAVDecAudioDualMonoReproMode, codecapi/eAVDecAudioDualMonoReproMode_LEFT_MONO, codecapi/eAVDecAudioDualMonoReproMode_MIX_MONO, codecapi/eAVDecAudioDualMonoReproMode_RIGHT_MONO, codecapi/eAVDecAudioDualMonoReproMode_STEREO, dshow.eavdecaudiodualmonorepromode, eAVDecAudioDualMonoReproMode, eAVDecAudioDualMonoReproMode enumeration [DirectShow], eAVDecAudioDualMonoReproModeEnumeration, eAVDecAudioDualMonoReproMode_LEFT_MONO, eAVDecAudioDualMonoReproMode_MIX_MONO, eAVDecAudioDualMonoReproMode_RIGHT_MONO, eAVDecAudioDualMonoReproMode_STEREO
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
 - eAVDecAudioDualMonoReproMode
 - codecapi/eAVDecAudioDualMonoReproMode
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
 - eAVDecAudioDualMonoReproMode
---

# eAVDecAudioDualMonoReproMode enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies how the decoder reproduces dual mono audio. This enumeration is used with the <a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property">AVDecAudioDualMonoReproMode</a> property.

## -enum-fields

### -field eAVDecAudioDualMonoReproMode_STEREO:0

Output channel 1 (Ch1) to the left speaker and channel 2 (Ch2) to the right speaker.

### -field eAVDecAudioDualMonoReproMode_LEFT_MONO:1

Output Ch1 to the left and right speakers.

### -field eAVDecAudioDualMonoReproMode_RIGHT_MONO:2

Output Ch2 to the left and right speakers.

### -field eAVDecAudioDualMonoReproMode_MIX_MONO:3

Mix Ch1 and Ch2 and output the mix to the left and right speakers.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
