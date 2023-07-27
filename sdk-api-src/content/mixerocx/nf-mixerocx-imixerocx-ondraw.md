---
UID: NF:mixerocx.IMixerOCX.OnDraw
title: IMixerOCX::OnDraw (mixerocx.h)
description: The OnDraw method instructs the Overlay Mixer to draw the video rectangle.
helpviewer_keywords: ["IMixerOCX interface [DirectShow]","OnDraw method","IMixerOCX.OnDraw","IMixerOCX::OnDraw","IMixerOCXOnDraw","OnDraw","OnDraw method [DirectShow]","OnDraw method [DirectShow]","IMixerOCX interface","dshow.imixerocx_ondraw","mixerocx/IMixerOCX::OnDraw"]
old-location: dshow\imixerocx_ondraw.htm
tech.root: dshow
ms.assetid: 69b8752b-9f97-422e-8a9a-f49c7a472cb6
ms.date: 4/26/2023
ms.keywords: IMixerOCX interface [DirectShow],OnDraw method, IMixerOCX.OnDraw, IMixerOCX::OnDraw, IMixerOCXOnDraw, OnDraw, OnDraw method [DirectShow], OnDraw method [DirectShow],IMixerOCX interface, dshow.imixerocx_ondraw, mixerocx/IMixerOCX::OnDraw
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
 - IMixerOCX::OnDraw
 - mixerocx/IMixerOCX::OnDraw
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
 - IMixerOCX.OnDraw
---

# IMixerOCX::OnDraw


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>OnDraw</code> method instructs the Overlay Mixer to draw the video rectangle.

## -parameters

### -param hdcDraw [in]

Specifies the device context associated with the parent window.

### -param prcDraw [in]

Specifies the rectangle coordinates of the video rectangle.

## -returns

If the method succeeds, it returns S_OK.

## -remarks

The HDC provided here should not be cached.

## -see-also

<a href="/windows/desktop/api/mixerocx/nn-mixerocx-imixerocx">IMixerOCX Interface</a>



<a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a>