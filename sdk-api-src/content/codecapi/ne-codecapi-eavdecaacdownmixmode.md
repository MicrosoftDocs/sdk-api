---
UID: NE:codecapi.eAVDecAACDownmixMode
title: eAVDecAACDownmixMode (codecapi.h)
description: Specifies whether an AAC decoder uses standard MPEG-2/MPEG-4 stereo downmix equations.
helpviewer_keywords: ["codecapi/eAVDecAACDownmixMode","codecapi/eAVDecAACUseARIBDownmix","codecapi/eAVDecAACUseISODownmix","dshow.eavdecaacdownmixmode","eAVDecAACDownmixMode","eAVDecAACDownmixMode enumeration [DirectShow]","eAVDecAACUseARIBDownmix","eAVDecAACUseISODownmix"]
old-location: dshow\eavdecaacdownmixmode.htm
tech.root: dshow
ms.assetid: d0a62f4a-6b0a-4a77-8d5e-cb40dc1364c7
ms.date: 4/26/2023
ms.keywords: codecapi/eAVDecAACDownmixMode, codecapi/eAVDecAACUseARIBDownmix, codecapi/eAVDecAACUseISODownmix, dshow.eavdecaacdownmixmode, eAVDecAACDownmixMode, eAVDecAACDownmixMode enumeration [DirectShow], eAVDecAACUseARIBDownmix, eAVDecAACUseISODownmix
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
 - eAVDecAACDownmixMode
 - codecapi/eAVDecAACDownmixMode
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
 - eAVDecAACDownmixMode
---

# eAVDecAACDownmixMode enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies whether an AAC decoder uses standard MPEG-2/MPEG-4 stereo downmix equations. This enumeration is used with the <a href="/windows/desktop/DirectShow/avdecaacdownmixmode-property">AVDecAACDownmixMode</a> property.

## -enum-fields

### -field eAVDecAACUseISODownmix:0

Use the standard ISO MPEG-2/MPEG-4 downmix equations.

### -field eAVDecAACUseARIBDownmix:1        

Use the downmix equations defined by ARIB document STD-B21.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
