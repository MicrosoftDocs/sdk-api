---
UID: NF:strmif.IOverlay.SetColorKey
title: IOverlay::SetColorKey (strmif.h)
description: The SetColorKey method changes the color key.helpviewer_keywords: ["IOverlay interface [DirectShow]","SetColorKey method","IOverlay.SetColorKey","IOverlay::SetColorKey","IOverlaySetColorKey","SetColorKey","SetColorKey method [DirectShow]","SetColorKey method [DirectShow]","IOverlay interface","dshow.ioverlay_setcolorkey","strmif/IOverlay::SetColorKey"]
old-location: dshow\ioverlay_setcolorkey.htm
tech.root: DirectShow
ms.assetid: dacbaf03-348f-403d-9c2c-aed8ec344879
ms.date: 12/05/2018
ms.keywords: IOverlay interface [DirectShow],SetColorKey method, IOverlay.SetColorKey, IOverlay::SetColorKey, IOverlaySetColorKey, SetColorKey, SetColorKey method [DirectShow], SetColorKey method [DirectShow],IOverlay interface, dshow.ioverlay_setcolorkey, strmif/IOverlay::SetColorKey
f1_keywords:
- strmif/IOverlay.SetColorKey
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
- IOverlay.SetColorKey
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOverlay::SetColorKey


## -description



The <code>SetColorKey</code> method changes the color key.




## -parameters




### -param pColorKey [in, out]

Pointer to the color key value to be set. If successful, the actual color key value selected is copied to this parameter.


## -returns



Returns S_OK if successful, E_POINTER if <i>pColorKey</i> is <b>NULL</b>, or E_INVALIDARG if the value of <i>pColorKey</i> is invalid for the current palette or pixel format.




## -remarks



If you change the color key using the <code>SetColorKey</code> method, all the advise links will receive an <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ioverlaynotify-oncolorkeychange">IOverlayNotify::OnColorKeyChange</a> callback method with the new color.

When using <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ioverlay-advise">IOverlay::Advise</a> on a palettized display, a filter can either install a color key (using <code>SetColorKey</code>) or install a palette (using <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ioverlay-setpalette">IOverlay::SetPalette</a>), but not both. This is because color keys in this mode require a palette to be realized that would conflict with <b>SetPalette</b>. Color keys can be uninstalled by requesting a color key with the CK_NOCOLORKEY flag. Likewise, any palette installed through <b>SetPalette</b> can be uninstalled by calling <b>SetPalette</b> and passing in <b>NULL</b> parameters (that is, SetPalette(0,<b>NULL</b>)).

Trying to set a palette when a color key is installed returns a VFW_E_PALETTE_SET error. Trying to set a color key when a palette is installed returns VFW_E_COLOR_KEY_SET.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ioverlay">IOverlay Interface</a>
 

 

