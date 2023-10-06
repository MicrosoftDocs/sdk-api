---
UID: NF:amvideo.IFullScreenVideoEx.IsKeepPixelAspectRatio
title: IFullScreenVideoEx::IsKeepPixelAspectRatio (amvideo.h)
description: The IsKeepPixelAspectRatio method queries whether the pixel aspect ratio is maintained. The Full Screen Renderer filter does not support this method; it always maintains the pixel aspect ratio.
helpviewer_keywords: ["IFullScreenVideoEx interface [DirectShow]","IsKeepPixelAspectRatio method","IFullScreenVideoEx.IsKeepPixelAspectRatio","IFullScreenVideoEx::IsKeepPixelAspectRatio","IFullScreenVideoExIsKeepPixelAspectRatio","IsKeepPixelAspectRatio","IsKeepPixelAspectRatio method [DirectShow]","IsKeepPixelAspectRatio method [DirectShow]","IFullScreenVideoEx interface","amvideo/IFullScreenVideoEx::IsKeepPixelAspectRatio","dshow.ifullscreenvideoex_iskeeppixelaspectratio"]
old-location: dshow\ifullscreenvideoex_iskeeppixelaspectratio.htm
tech.root: dshow
ms.assetid: 3f3b55d9-b504-42a3-b60a-65073d1e1447
ms.date: 4/26/2023
ms.keywords: IFullScreenVideoEx interface [DirectShow],IsKeepPixelAspectRatio method, IFullScreenVideoEx.IsKeepPixelAspectRatio, IFullScreenVideoEx::IsKeepPixelAspectRatio, IFullScreenVideoExIsKeepPixelAspectRatio, IsKeepPixelAspectRatio, IsKeepPixelAspectRatio method [DirectShow], IsKeepPixelAspectRatio method [DirectShow],IFullScreenVideoEx interface, amvideo/IFullScreenVideoEx::IsKeepPixelAspectRatio, dshow.ifullscreenvideoex_iskeeppixelaspectratio
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
 - IFullScreenVideoEx::IsKeepPixelAspectRatio
 - amvideo/IFullScreenVideoEx::IsKeepPixelAspectRatio
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
 - IFullScreenVideoEx.IsKeepPixelAspectRatio
---

# IFullScreenVideoEx::IsKeepPixelAspectRatio


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IsKeepPixelAspectRatio</code> method queries whether the pixel aspect ratio is maintained. The Full Screen Renderer filter does not support this method; it always maintains the pixel aspect ratio.

## -parameters

### -param pKeepAspect [in]

Pointer to a variable that receives the value OATRUE or OAFALSE.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-ifullscreenvideoex">IFullScreenVideoEx Interface</a>