---
UID: NE:codecapi.eAVEncAudioDualMono
title: eAVEncAudioDualMono (codecapi.h)
description: Specifies whether 2-channel audio is encoded as stereo or dual mono. This enumeration is used with the AVEncAudioDualMono property.
helpviewer_keywords: ["codecapi/eAVEncAudioDualMono","codecapi/eAVEncAudioDualMono_Off","codecapi/eAVEncAudioDualMono_On","codecapi/eAVEncAudioDualMono_SameAsInput","dshow.eavencaudiodualmono","eAVEncAudioDualMono","eAVEncAudioDualMono enumeration [DirectShow]","eAVEncAudioDualMonoEnumeration","eAVEncAudioDualMono_Off","eAVEncAudioDualMono_On","eAVEncAudioDualMono_SameAsInput"]
old-location: dshow\eavencaudiodualmono.htm
tech.root: dshow
ms.assetid: 5204ca69-947a-4099-a571-b2c0047d9f7f
ms.date: 4/26/2023
ms.keywords: codecapi/eAVEncAudioDualMono, codecapi/eAVEncAudioDualMono_Off, codecapi/eAVEncAudioDualMono_On, codecapi/eAVEncAudioDualMono_SameAsInput, dshow.eavencaudiodualmono, eAVEncAudioDualMono, eAVEncAudioDualMono enumeration [DirectShow], eAVEncAudioDualMonoEnumeration, eAVEncAudioDualMono_Off, eAVEncAudioDualMono_On, eAVEncAudioDualMono_SameAsInput
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
 - eAVEncAudioDualMono
 - codecapi/eAVEncAudioDualMono
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
 - eAVEncAudioDualMono
---

# eAVEncAudioDualMono enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies whether 2-channel audio is encoded as stereo or dual mono. This enumeration is used with the <a href="/windows/desktop/DirectShow/avencaudiodualmono-property">AVEncAudioDualMono</a> property.

## -enum-fields

### -field eAVEncAudioDualMono_SameAsInput:0

Use the setting specified in the input media type.

### -field eAVEncAudioDualMono_Off:1

Do not use dual mono encoding.

### -field eAVEncAudioDualMono_On:2   

Use dual mono encoding.

## -remarks

In dual mono encoding, each channel is encoded separately. In stereo encoding, both channels are encoded together.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
