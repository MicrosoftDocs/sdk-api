---
UID: NE:codecapi.eAVEncVideoColorLighting
title: eAVEncVideoColorLighting (codecapi.h)
description: Specifies the intended lighting conditions for viewing a video source. This enumeration is used with the AVEncVideoInputColorLighting and AVEncVideoOutputColorLighting properties.
helpviewer_keywords: ["codecapi/eAVEncVideoColorLighting","codecapi/eAVEncVideoColorLighting_Bright","codecapi/eAVEncVideoColorLighting_Dark","codecapi/eAVEncVideoColorLighting_Dim","codecapi/eAVEncVideoColorLighting_Office","codecapi/eAVEncVideoColorLighting_SameAsSource","codecapi/eAVEncVideoColorLighting_Unknown","dshow.eavencvideocolorlighting","eAVEncVideoColorLighting","eAVEncVideoColorLighting enumeration [DirectShow]","eAVEncVideoColorLightingEnumeration","eAVEncVideoColorLighting_Bright","eAVEncVideoColorLighting_Dark","eAVEncVideoColorLighting_Dim","eAVEncVideoColorLighting_Office","eAVEncVideoColorLighting_SameAsSource","eAVEncVideoColorLighting_Unknown"]
old-location: dshow\eavencvideocolorlighting.htm
tech.root: dshow
ms.assetid: d2e85b3e-b458-4148-b9d7-0ed3d4213838
ms.date: 4/26/2023
ms.keywords: codecapi/eAVEncVideoColorLighting, codecapi/eAVEncVideoColorLighting_Bright, codecapi/eAVEncVideoColorLighting_Dark, codecapi/eAVEncVideoColorLighting_Dim, codecapi/eAVEncVideoColorLighting_Office, codecapi/eAVEncVideoColorLighting_SameAsSource, codecapi/eAVEncVideoColorLighting_Unknown, dshow.eavencvideocolorlighting, eAVEncVideoColorLighting, eAVEncVideoColorLighting enumeration [DirectShow], eAVEncVideoColorLightingEnumeration, eAVEncVideoColorLighting_Bright, eAVEncVideoColorLighting_Dark, eAVEncVideoColorLighting_Dim, eAVEncVideoColorLighting_Office, eAVEncVideoColorLighting_SameAsSource, eAVEncVideoColorLighting_Unknown
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
 - eAVEncVideoColorLighting
 - codecapi/eAVEncVideoColorLighting
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
 - eAVEncVideoColorLighting
---

# eAVEncVideoColorLighting enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies the intended lighting conditions for viewing a video source. This enumeration is used with the <a href="/windows/desktop/DirectShow/avencvideoinputcolorlighting-property">AVEncVideoInputColorLighting</a> and <a href="/windows/desktop/DirectShow/avencvideooutputcolorlighting-property">AVEncVideoOutputColorLighting</a> properties.

## -enum-fields

### -field eAVEncVideoColorLighting_SameAsSource:0

Use the same lighting as the input video. This flag applies to the <b>AVEncVideoOutputColorLighting</b> property only.

### -field eAVEncVideoColorLighting_Unknown:1

The optimal lighting is unknown.

### -field eAVEncVideoColorLighting_Bright:2

Bright lighting; for example, outdoors.

### -field eAVEncVideoColorLighting_Office:3

Medium brightness; for example, normal office lighting.

### -field eAVEncVideoColorLighting_Dim:4

Dim; for example, a living room with a television and additional low lighting.

### -field eAVEncVideoColorLighting_Dark:5

Dark; for example, a movie theater.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
