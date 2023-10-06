---
UID: NF:amvideo.IFullScreenVideoEx.SetDefault
title: IFullScreenVideoEx::SetDefault (amvideo.h)
description: The SetDefault method saves the current settings.
helpviewer_keywords: ["IFullScreenVideoEx interface [DirectShow]","SetDefault method","IFullScreenVideoEx.SetDefault","IFullScreenVideoEx::SetDefault","IFullScreenVideoSetDefault","SetDefault","SetDefault method [DirectShow]","SetDefault method [DirectShow]","IFullScreenVideoEx interface","amvideo/IFullScreenVideoEx::SetDefault","dshow.ifullscreenvideoex_setdefault"]
old-location: dshow\ifullscreenvideoex_setdefault.htm
tech.root: dshow
ms.assetid: 1821703c-0da1-4b3e-a921-a66770b8ee0d
ms.date: 4/26/2023
ms.keywords: IFullScreenVideoEx interface [DirectShow],SetDefault method, IFullScreenVideoEx.SetDefault, IFullScreenVideoEx::SetDefault, IFullScreenVideoSetDefault, SetDefault, SetDefault method [DirectShow], SetDefault method [DirectShow],IFullScreenVideoEx interface, amvideo/IFullScreenVideoEx::SetDefault, dshow.ifullscreenvideoex_setdefault
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
 - IFullScreenVideoEx::SetDefault
 - amvideo/IFullScreenVideoEx::SetDefault
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
 - IFullScreenVideoEx.SetDefault
---

# IFullScreenVideoEx::SetDefault


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetDefault</code> method saves the current settings.



## -returns

Returns an <b>HRESULT</b> value.

## -remarks

Normally, the properties set through this interface apply only to the current instance of the Full Screen Renderer. Calling this method saves the current values as the global default. This method persists the following information:

<ul>
<li>The clip factor.</li>
<li>The enabled flag for each display mode.</li>
</ul>
It does not persist the caption or the hide-when-deactivated flag.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-ifullscreenvideoex">IFullScreenVideoEx Interface</a>



<a href="/windows/desktop/api/amvideo/nf-amvideo-ifullscreenvideoex-hideondeactivate">IFullScreenVideoEx::HideOnDeactivate</a>



<a href="/windows/desktop/api/amvideo/nf-amvideo-ifullscreenvideoex-setcaption">IFullScreenVideoEx::SetCaption</a>



<a href="/windows/desktop/api/amvideo/nf-amvideo-ifullscreenvideoex-setclipfactor">IFullScreenVideoEx::SetClipFactor</a>



<a href="/windows/desktop/api/amvideo/nf-amvideo-ifullscreenvideoex-setenabled">IFullScreenVideoEx::SetEnabled</a>
