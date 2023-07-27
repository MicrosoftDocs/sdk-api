---
UID: NF:strmif.IOverlayNotify.OnColorKeyChange
title: IOverlayNotify::OnColorKeyChange (strmif.h)
description: The OnColorKeyChange method provides notification that the window's color key has changed.
helpviewer_keywords: ["IOverlayNotify interface [DirectShow]","OnColorKeyChange method","IOverlayNotify.OnColorKeyChange","IOverlayNotify::OnColorKeyChange","IOverlayNotifyOnColorKeyChange","OnColorKeyChange","OnColorKeyChange method [DirectShow]","OnColorKeyChange method [DirectShow]","IOverlayNotify interface","dshow.ioverlaynotify_oncolorkeychange","strmif/IOverlayNotify::OnColorKeyChange"]
old-location: dshow\ioverlaynotify_oncolorkeychange.htm
tech.root: dshow
ms.assetid: a1e7fc88-a50a-4832-9b29-21b94184f1c7
ms.date: 4/26/2023
ms.keywords: IOverlayNotify interface [DirectShow],OnColorKeyChange method, IOverlayNotify.OnColorKeyChange, IOverlayNotify::OnColorKeyChange, IOverlayNotifyOnColorKeyChange, OnColorKeyChange, OnColorKeyChange method [DirectShow], OnColorKeyChange method [DirectShow],IOverlayNotify interface, dshow.ioverlaynotify_oncolorkeychange, strmif/IOverlayNotify::OnColorKeyChange
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
 - IOverlayNotify::OnColorKeyChange
 - strmif/IOverlayNotify::OnColorKeyChange
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
 - IOverlayNotify.OnColorKeyChange
---

# IOverlayNotify::OnColorKeyChange


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>OnColorKeyChange</code> method provides notification that the window's color key has changed.

## -parameters

### -param pColorKey [in]

Pointer to the new chroma key.

## -returns

Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ioverlaynotify">IOverlayNotify Interface</a>