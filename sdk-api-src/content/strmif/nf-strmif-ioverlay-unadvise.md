---
UID: NF:strmif.IOverlay.Unadvise
title: IOverlay::Unadvise (strmif.h)
description: The Unadvise method terminates the advise link established with the IOverlayNotify interface.
helpviewer_keywords: ["IOverlay interface [DirectShow]","Unadvise method","IOverlay.Unadvise","IOverlay::Unadvise","IOverlayUnadvise","Unadvise","Unadvise method [DirectShow]","Unadvise method [DirectShow]","IOverlay interface","dshow.ioverlay_unadvise","strmif/IOverlay::Unadvise"]
old-location: dshow\ioverlay_unadvise.htm
tech.root: dshow
ms.assetid: da987152-d5cd-42c5-848a-6d70ad25ca33
ms.date: 4/26/2023
ms.keywords: IOverlay interface [DirectShow],Unadvise method, IOverlay.Unadvise, IOverlay::Unadvise, IOverlayUnadvise, Unadvise, Unadvise method [DirectShow], Unadvise method [DirectShow],IOverlay interface, dshow.ioverlay_unadvise, strmif/IOverlay::Unadvise
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
 - IOverlay::Unadvise
 - strmif/IOverlay::Unadvise
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
 - IOverlay.Unadvise
---

# IOverlay::Unadvise


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Unadvise</code> method terminates the advise link established with the <a href="/windows/desktop/api/strmif/nn-strmif-ioverlaynotify">IOverlayNotify</a> interface.



## -returns

Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.

## -remarks

This method terminates the advise link established by using the <a href="/windows/desktop/api/strmif/nf-strmif-ioverlay-advise">IOverlay::Advise</a> method. Only one advise link can be maintained at any one time.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ioverlay">IOverlay Interface</a>
