---
UID: NF:mixerocx.IMixerOCX.GetVideoSize
title: IMixerOCX::GetVideoSize (mixerocx.h)
description: The GetVideoSize method retrieves the current size of the video rectangle.
helpviewer_keywords: ["GetVideoSize","GetVideoSize method [DirectShow]","GetVideoSize method [DirectShow]","IMixerOCX interface","IMixerOCX interface [DirectShow]","GetVideoSize method","IMixerOCX.GetVideoSize","IMixerOCX::GetVideoSize","IMixerOCXGetVideoSize","dshow.imixerocx_getvideosize","mixerocx/IMixerOCX::GetVideoSize"]
old-location: dshow\imixerocx_getvideosize.htm
tech.root: dshow
ms.assetid: e4cc71b6-23a5-4610-ac59-06484af6d0b4
ms.date: 4/26/2023
ms.keywords: GetVideoSize, GetVideoSize method [DirectShow], GetVideoSize method [DirectShow],IMixerOCX interface, IMixerOCX interface [DirectShow],GetVideoSize method, IMixerOCX.GetVideoSize, IMixerOCX::GetVideoSize, IMixerOCXGetVideoSize, dshow.imixerocx_getvideosize, mixerocx/IMixerOCX::GetVideoSize
req.header: mixerocx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMixerOCX::GetVideoSize
 - mixerocx/IMixerOCX::GetVideoSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMixerOCX.GetVideoSize
---

# IMixerOCX::GetVideoSize


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetVideoSize</code> method retrieves the current size of the video rectangle.

## -parameters

### -param pdwVideoWidth [out]

Pointer that receives the video width in pixels.

### -param pdwVideoHeight [out]

Pointer that receives the video height in pixels.

## -returns

If the method succeeds, it returns S_OK.

## -see-also

<a href="/windows/desktop/api/mixerocx/nn-mixerocx-imixerocx">IMixerOCX Interface</a>



<a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a>