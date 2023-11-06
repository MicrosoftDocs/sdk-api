---
UID: NN:strmif.IOverlayNotify
title: IOverlayNotify (strmif.h)
description: The IOverlayNotify interface provides an upstream filter, such as a decoder, with notifications of changes to the rendering window.
helpviewer_keywords: ["IOverlayNotify","IOverlayNotify interface [DirectShow]","IOverlayNotify interface [DirectShow]","described","IOverlayNotifyInterface","dshow.ioverlaynotify","strmif/IOverlayNotify"]
old-location: dshow\ioverlaynotify.htm
tech.root: dshow
ms.assetid: 77dcee49-35ef-4664-b0e6-3044352d543c
ms.date: 4/26/2023
ms.keywords: IOverlayNotify, IOverlayNotify interface [DirectShow], IOverlayNotify interface [DirectShow],described, IOverlayNotifyInterface, dshow.ioverlaynotify, strmif/IOverlayNotify
req.header: strmif.h
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
 - IOverlayNotify
 - strmif/IOverlayNotify
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
 - IOverlayNotify
---

# IOverlayNotify interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IOverlayNotify</code> interface provides an upstream filter, such as a decoder, with notifications of changes to the rendering window. This includes notifications of changes to the palette, color key, and window position, and visible region (clipping) changes.

Most software video decoders let the video renderer draw the decompressed images they produce by passing the media samples to the <a href="/windows/desktop/api/strmif/nn-strmif-imeminputpin">IMemInputPin</a> interface on the renderer's input pin.

However, some video decoding filters (typically hardware decompression boards) handle the drawing of the images themselves, perhaps by using a VGA connector. These filters do not need to use <a href="/windows/desktop/api/strmif/nn-strmif-imeminputpin">IMemInputPin</a>, but can instead use the <a href="/windows/desktop/api/strmif/nn-strmif-ioverlay">IOverlay</a> interface provided by the renderer input pin. Through this interface, the decoder can be notified when the window position or size changes, or when the current system palette changes in order to install and change color keys and palettes.

Decoders that do their own drawing should implement the <code>IOverlayNotify</code> and <a href="/windows/desktop/api/strmif/nn-strmif-ioverlaynotify2">IOverlayNotify2</a> interfaces. The renderer uses this interface to notify the decoder whenever the window size or position changes, the system palette changes, or a different color key is used. The decoder should call the <a href="/windows/desktop/api/strmif/nf-strmif-ioverlay-advise">IOverlay::Advise</a> method on the renderer's input pin, to set up the callback. Once the callback is established, the renderer calls the decoder's <code>IOverlayNotify</code> methods when the appropriate events occur. To cancel the callback, use the <a href="/windows/desktop/api/strmif/nf-strmif-ioverlay-unadvise">IOverlay::Unadvise</a> method.

The video renderer is the only filter that calls the methods on this interface. This is done automatically by the default video renderer. If you are writing a replacement video renderer, you will need to use the methods on this interface if your filter supports <b>IOverlay</b> and this interface is passed to your filter in an <a href="/windows/desktop/api/strmif/nf-strmif-ioverlay-advise">IOverlay::Advise</a> call.

## -inheritance

The <b>IOverlayNotify</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOverlayNotify</b> also has these types of members:

