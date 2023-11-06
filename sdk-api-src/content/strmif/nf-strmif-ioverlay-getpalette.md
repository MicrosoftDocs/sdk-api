---
UID: NF:strmif.IOverlay.GetPalette
title: IOverlay::GetPalette (strmif.h)
description: The GetPalette method retrieves the current system palette.
helpviewer_keywords: ["GetPalette","GetPalette method [DirectShow]","GetPalette method [DirectShow]","IOverlay interface","IOverlay interface [DirectShow]","GetPalette method","IOverlay.GetPalette","IOverlay::GetPalette","IOverlayGetPalette","dshow.ioverlay_getpalette","strmif/IOverlay::GetPalette"]
old-location: dshow\ioverlay_getpalette.htm
tech.root: dshow
ms.assetid: 993c80fb-fa67-4dd6-815b-8e15d2f7f495
ms.date: 4/26/2023
ms.keywords: GetPalette, GetPalette method [DirectShow], GetPalette method [DirectShow],IOverlay interface, IOverlay interface [DirectShow],GetPalette method, IOverlay.GetPalette, IOverlay::GetPalette, IOverlayGetPalette, dshow.ioverlay_getpalette, strmif/IOverlay::GetPalette
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
 - IOverlay::GetPalette
 - strmif/IOverlay::GetPalette
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
 - IOverlay.GetPalette
---

# IOverlay::GetPalette


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetPalette</code> method retrieves the current system palette.

## -parameters

### -param pdwColors [out]

Pointer to a variable that receives the number of colors present.

### -param ppPalette [out]

Receives a pointer to a <a href="/previous-versions/dd162769(v=vs.85)">PALETTEENTRY</a> structure describing the palette.

## -returns

Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ioverlay">IOverlay Interface</a>