---
UID: NF:strmif.IOverlayNotify.OnClipChange
title: IOverlayNotify::OnClipChange (strmif.h)
description: The OnClipChange method provides notification that the window's visible region has changed. It is essential that any overlay hardware be updated to reflect the change to the visible region before returning from this method.
helpviewer_keywords: ["IOverlayNotify interface [DirectShow]","OnClipChange method","IOverlayNotify.OnClipChange","IOverlayNotify::OnClipChange","IOverlayNotifyOnClipChange","OnClipChange","OnClipChange method [DirectShow]","OnClipChange method [DirectShow]","IOverlayNotify interface","dshow.ioverlaynotify_onclipchange","strmif/IOverlayNotify::OnClipChange"]
old-location: dshow\ioverlaynotify_onclipchange.htm
tech.root: dshow
ms.assetid: d5bed27f-2918-4c1f-9340-a0d5714d911b
ms.date: 4/26/2023
ms.keywords: IOverlayNotify interface [DirectShow],OnClipChange method, IOverlayNotify.OnClipChange, IOverlayNotify::OnClipChange, IOverlayNotifyOnClipChange, OnClipChange, OnClipChange method [DirectShow], OnClipChange method [DirectShow],IOverlayNotify interface, dshow.ioverlaynotify_onclipchange, strmif/IOverlayNotify::OnClipChange
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
 - IOverlayNotify::OnClipChange
 - strmif/IOverlayNotify::OnClipChange
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
 - IOverlayNotify.OnClipChange
---

# IOverlayNotify::OnClipChange


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>OnClipChange</code> method provides notification that the window's visible region has changed. It is essential that any overlay hardware be updated to reflect the change to the visible region before returning from this method.

## -parameters

### -param pSourceRect [in]

Pointer to the region of the video to use.

### -param pDestinationRect [in]

Pointer to the video destination.

### -param pRgnData [in]

Pointer to the clipping information.

## -returns

Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.

## -remarks

The calls to <code>OnClipChange</code> happen in synchronization with the window. It is called with an empty clip list to freeze the video before the window moves, and then called again when the window has stabilized with the new clip list.

If the window rectangle is all zeros, the window is invisible. As is the case for AVI decoders, the decoder should save the image if it relies on the current image to decode the next one.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ioverlaynotify">IOverlayNotify Interface</a>