---
UID: NF:strmif.IOverlay.GetDefaultColorKey
title: IOverlay::GetDefaultColorKey (strmif.h)
description: The GetDefaultColorKey method retrieves the default color key used for a chroma key overlay.helpviewer_keywords: ["GetDefaultColorKey","GetDefaultColorKey method [DirectShow]","GetDefaultColorKey method [DirectShow]","IOverlay interface","IOverlay interface [DirectShow]","GetDefaultColorKey method","IOverlay.GetDefaultColorKey","IOverlay::GetDefaultColorKey","IOverlayGetDefaultColorKey","dshow.ioverlay_getdefaultcolorkey","strmif/IOverlay::GetDefaultColorKey"]
old-location: dshow\ioverlay_getdefaultcolorkey.htm
tech.root: DirectShow
ms.assetid: d3aec72f-472e-44fa-bbd8-81e64732e5bc
ms.date: 12/05/2018
ms.keywords: GetDefaultColorKey, GetDefaultColorKey method [DirectShow], GetDefaultColorKey method [DirectShow],IOverlay interface, IOverlay interface [DirectShow],GetDefaultColorKey method, IOverlay.GetDefaultColorKey, IOverlay::GetDefaultColorKey, IOverlayGetDefaultColorKey, dshow.ioverlay_getdefaultcolorkey, strmif/IOverlay::GetDefaultColorKey
f1_keywords:
- strmif/IOverlay.GetDefaultColorKey
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
- IOverlay.GetDefaultColorKey
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOverlay::GetDefaultColorKey


## -description



The <code>GetDefaultColorKey</code> method retrieves the default color key used for a chroma key overlay.




## -parameters




### -param pColorKey [out]

Pointer to a variable that receives the default color key.


## -returns



Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.




## -remarks



A filter using color keys can get a default color from the video renderer. The default color key can then be installed into the window using <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ioverlay-setcolorkey">IOverlay::SetColorKey</a>. The colors returned through this method vary depending on the current display mode. If the colors are 8-bit palettized, they will be bright system colors (such as magenta). If the display is in a true-color mode, they will be shades of black.

The <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ioverlay">IOverlay</a> interface is used to ensure that separate instances of the renderer on the same computer get different color keys so that overlays do not conflict.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ioverlay">IOverlay Interface</a>
 

 

