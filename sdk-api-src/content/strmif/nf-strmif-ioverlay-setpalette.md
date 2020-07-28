---
UID: NF:strmif.IOverlay.SetPalette
title: IOverlay::SetPalette (strmif.h)
description: The SetPalette method sets the palette.
helpviewer_keywords: ["IOverlay interface [DirectShow]","SetPalette method","IOverlay.SetPalette","IOverlay::SetPalette","IOverlaySetPalette","SetPalette","SetPalette method [DirectShow]","SetPalette method [DirectShow]","IOverlay interface","dshow.ioverlay_setpalette","strmif/IOverlay::SetPalette"]
old-location: dshow\ioverlay_setpalette.htm
tech.root: dshow
ms.assetid: 572f77ab-08a8-453a-993b-724da967bcde
ms.date: 12/05/2018
ms.keywords: IOverlay interface [DirectShow],SetPalette method, IOverlay.SetPalette, IOverlay::SetPalette, IOverlaySetPalette, SetPalette, SetPalette method [DirectShow], SetPalette method [DirectShow],IOverlay interface, dshow.ioverlay_setpalette, strmif/IOverlay::SetPalette
f1_keywords:
- strmif/IOverlay.SetPalette
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOverlay::SetPalette


## -description



The <code>SetPalette</code> method sets the palette.




## -parameters




### -param dwColors [in]

Number of colors present.


### -param pPalette [in]

Pointer to colors to use for the palette.


## -returns



Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.




## -remarks



This method sets a logical palette for the window. The window is not guaranteed to always have the colors requested in the actual system device palette. The Microsoft® Windows® operating system only guarantees those colors when the window is the foreground active window. The current device palette can be obtained by calling <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ioverlay-getpalette">IOverlay::GetPalette</a>.

If the device does not have a palette, it returns VFW_E_NO_DISPLAY_PALETTE.

The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> filter returns E_NOTIMPL.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ioverlay">IOverlay Interface</a>
 

 

