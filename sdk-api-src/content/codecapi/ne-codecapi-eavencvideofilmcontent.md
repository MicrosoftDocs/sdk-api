---
UID: NE:codecapi.eAVEncVideoFilmContent
title: eAVEncVideoFilmContent (codecapi.h)
description: Specifies whether the original source of the input video was film or video. This enumeration is used with the AVEncVideoSourceFilmContent property.
helpviewer_keywords: ["codecapi/eAVEncVideoFilmContent","codecapi/eAVEncVideoFilmContent_FilmOnly","codecapi/eAVEncVideoFilmContent_Mixed","codecapi/eAVEncVideoFilmContent_VideoOnly","dshow.eavencvideofilmcontent","eAVEncVideoFilmContent","eAVEncVideoFilmContent enumeration [DirectShow]","eAVEncVideoFilmContentEnumeration","eAVEncVideoFilmContent_FilmOnly","eAVEncVideoFilmContent_Mixed","eAVEncVideoFilmContent_VideoOnly"]
old-location: dshow\eavencvideofilmcontent.htm
tech.root: dshow
ms.assetid: 64a7c075-342d-49c1-90eb-9ac34d0c2318
ms.date: 4/26/2023
ms.keywords: codecapi/eAVEncVideoFilmContent, codecapi/eAVEncVideoFilmContent_FilmOnly, codecapi/eAVEncVideoFilmContent_Mixed, codecapi/eAVEncVideoFilmContent_VideoOnly, dshow.eavencvideofilmcontent, eAVEncVideoFilmContent, eAVEncVideoFilmContent enumeration [DirectShow], eAVEncVideoFilmContentEnumeration, eAVEncVideoFilmContent_FilmOnly, eAVEncVideoFilmContent_Mixed, eAVEncVideoFilmContent_VideoOnly
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
 - eAVEncVideoFilmContent
 - codecapi/eAVEncVideoFilmContent
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
 - eAVEncVideoFilmContent
---

# eAVEncVideoFilmContent enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies whether the original source of the input video was film or video. This enumeration is used with the <a href="/windows/desktop/DirectShow/avencvideosourcefilmcontent-property">AVEncVideoSourceFilmContent</a> property.

## -enum-fields

### -field eAVEncVideoFilmContent_VideoOnly:0

The original source was video.

### -field eAVEncVideoFilmContent_FilmOnly:1

The original source was film.

### -field eAVEncVideoFilmContent_Mixed:2

The original source contains a mix of video and film.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
