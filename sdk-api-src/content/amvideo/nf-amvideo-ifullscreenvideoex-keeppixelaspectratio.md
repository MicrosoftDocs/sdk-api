---
UID: NF:amvideo.IFullScreenVideoEx.KeepPixelAspectRatio
title: IFullScreenVideoEx::KeepPixelAspectRatio (amvideo.h)
description: The KeepPixelAspectRatio method specifies whether to maintain the pixel aspect ratio. The Full Screen Renderer filter does not support this method; it always maintains the pixel aspect ratio.
helpviewer_keywords: ["IFullScreenVideoEx interface [DirectShow]","KeepPixelAspectRatio method","IFullScreenVideoEx.KeepPixelAspectRatio","IFullScreenVideoEx::KeepPixelAspectRatio","IFullScreenVideoExKeepPixelAspectRatio","KeepPixelAspectRatio","KeepPixelAspectRatio method [DirectShow]","KeepPixelAspectRatio method [DirectShow]","IFullScreenVideoEx interface","amvideo/IFullScreenVideoEx::KeepPixelAspectRatio","dshow.ifullscreenvideoex_keeppixelaspectratio"]
old-location: dshow\ifullscreenvideoex_keeppixelaspectratio.htm
tech.root: dshow
ms.assetid: f2c57560-7ffa-4bd4-8d0c-a048dafa35bc
ms.date: 4/26/2023
ms.keywords: IFullScreenVideoEx interface [DirectShow],KeepPixelAspectRatio method, IFullScreenVideoEx.KeepPixelAspectRatio, IFullScreenVideoEx::KeepPixelAspectRatio, IFullScreenVideoExKeepPixelAspectRatio, KeepPixelAspectRatio, KeepPixelAspectRatio method [DirectShow], KeepPixelAspectRatio method [DirectShow],IFullScreenVideoEx interface, amvideo/IFullScreenVideoEx::KeepPixelAspectRatio, dshow.ifullscreenvideoex_keeppixelaspectratio
req.header: amvideo.h
req.include-header: Dshow.h
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
 - IFullScreenVideoEx::KeepPixelAspectRatio
 - amvideo/IFullScreenVideoEx::KeepPixelAspectRatio
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
 - IFullScreenVideoEx.KeepPixelAspectRatio
---

# IFullScreenVideoEx::KeepPixelAspectRatio


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>KeepPixelAspectRatio</code> method specifies whether to maintain the pixel aspect ratio. The Full Screen Renderer filter does not support this method; it always maintains the pixel aspect ratio.

## -parameters

### -param KeepAspect [in]

Specifies whether to maintain the aspect ratio. The value must be OATRUE or OAFALSE.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-ifullscreenvideoex">IFullScreenVideoEx Interface</a>