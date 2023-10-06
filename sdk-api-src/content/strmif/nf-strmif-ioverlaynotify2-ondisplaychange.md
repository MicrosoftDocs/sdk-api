---
UID: NF:strmif.IOverlayNotify2.OnDisplayChange
title: IOverlayNotify2::OnDisplayChange (strmif.h)
description: The OnDisplayChange method provides notification that the exposed window area has changed.
helpviewer_keywords: ["IOverlayNotify2 interface [DirectShow]","OnDisplayChange method","IOverlayNotify2.OnDisplayChange","IOverlayNotify2::OnDisplayChange","IOverlayNotify2OnDisplayChange","OnDisplayChange","OnDisplayChange method [DirectShow]","OnDisplayChange method [DirectShow]","IOverlayNotify2 interface","dshow.ioverlaynotify2_ondisplaychange","strmif/IOverlayNotify2::OnDisplayChange"]
old-location: dshow\ioverlaynotify2_ondisplaychange.htm
tech.root: dshow
ms.assetid: 8f32a373-5d98-4491-8bfb-9445cb15ff10
ms.date: 4/26/2023
ms.keywords: IOverlayNotify2 interface [DirectShow],OnDisplayChange method, IOverlayNotify2.OnDisplayChange, IOverlayNotify2::OnDisplayChange, IOverlayNotify2OnDisplayChange, OnDisplayChange, OnDisplayChange method [DirectShow], OnDisplayChange method [DirectShow],IOverlayNotify2 interface, dshow.ioverlaynotify2_ondisplaychange, strmif/IOverlayNotify2::OnDisplayChange
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
 - IOverlayNotify2::OnDisplayChange
 - strmif/IOverlayNotify2::OnDisplayChange
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
 - IOverlayNotify2.OnDisplayChange
---

# IOverlayNotify2::OnDisplayChange


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>OnDisplayChange</code> method provides notification that the exposed window area has changed.

## -parameters

### -param hMonitor [in]

Handle to the monitor used for displaying the overlay.

## -returns

Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ioverlaynotify2">IOverlayNotify2 Interface</a>