---
UID: NF:strmif.IOverlay.GetVideoPosition
title: IOverlay::GetVideoPosition (strmif.h)
description: The GetVideoPosition method retrieves the current video source and destination rectangles.
helpviewer_keywords: ["GetVideoPosition","GetVideoPosition method [DirectShow]","GetVideoPosition method [DirectShow]","IOverlay interface","IOverlay interface [DirectShow]","GetVideoPosition method","IOverlay.GetVideoPosition","IOverlay::GetVideoPosition","IOverlayGetVideoPosition","dshow.ioverlay_getvideoposition","strmif/IOverlay::GetVideoPosition"]
old-location: dshow\ioverlay_getvideoposition.htm
tech.root: dshow
ms.assetid: a140cc63-29a1-4c81-8393-7f4342c7b7cc
ms.date: 4/26/2023
ms.keywords: GetVideoPosition, GetVideoPosition method [DirectShow], GetVideoPosition method [DirectShow],IOverlay interface, IOverlay interface [DirectShow],GetVideoPosition method, IOverlay.GetVideoPosition, IOverlay::GetVideoPosition, IOverlayGetVideoPosition, dshow.ioverlay_getvideoposition, strmif/IOverlay::GetVideoPosition
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
 - IOverlay::GetVideoPosition
 - strmif/IOverlay::GetVideoPosition
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
 - IOverlay.GetVideoPosition
---

# IOverlay::GetVideoPosition


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetVideoPosition</code> method retrieves the current video source and destination rectangles.

## -parameters

### -param pSourceRect [out]

Pointer to a <b>RECT</b> structure that receives the source rectangle.

### -param pDestinationRect [in]

Pointer to a <b>RECT</b> structure that receives the destination rectangle.

## -returns

Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ioverlay">IOverlay Interface</a>