---
UID: NF:strmif.IOverlay.SetPalette
title: IOverlay::SetPalette (strmif.h)
description: The SetPalette method sets the palette.
helpviewer_keywords: ["IOverlay interface [DirectShow]","SetPalette method","IOverlay.SetPalette","IOverlay::SetPalette","IOverlaySetPalette","SetPalette","SetPalette method [DirectShow]","SetPalette method [DirectShow]","IOverlay interface","dshow.ioverlay_setpalette","strmif/IOverlay::SetPalette"]
old-location: dshow\ioverlay_setpalette.htm
tech.root: dshow
ms.assetid: 572f77ab-08a8-453a-993b-724da967bcde
ms.date: 4/26/2023
ms.keywords: IOverlay interface [DirectShow],SetPalette method, IOverlay.SetPalette, IOverlay::SetPalette, IOverlaySetPalette, SetPalette, SetPalette method [DirectShow], SetPalette method [DirectShow],IOverlay interface, dshow.ioverlay_setpalette, strmif/IOverlay::SetPalette
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
 - IOverlay::SetPalette
 - strmif/IOverlay::SetPalette
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
 - IOverlay.SetPalette
---

# IOverlay::SetPalette


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetPalette</code> method sets the palette.

## -parameters

### -param dwColors [in]

Number of colors present.

### -param pPalette [in]

Pointer to colors to use for the palette.

## -returns

Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.

## -remarks

This method sets a logical palette for the window. The window is not guaranteed to always have the colors requested in the actual system device palette. The Microsoft® Windows® operating system only guarantees those colors when the window is the foreground active window. The current device palette can be obtained by calling <a href="/windows/desktop/api/strmif/nf-strmif-ioverlay-getpalette">IOverlay::GetPalette</a>.

If the device does not have a palette, it returns VFW_E_NO_DISPLAY_PALETTE.

The <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> filter returns E_NOTIMPL.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ioverlay">IOverlay Interface</a>