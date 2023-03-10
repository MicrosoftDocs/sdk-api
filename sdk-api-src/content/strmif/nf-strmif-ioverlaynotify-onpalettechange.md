---
UID: NF:strmif.IOverlayNotify.OnPaletteChange
title: IOverlayNotify::OnPaletteChange (strmif.h)
description: The OnPaletteChange method provides notification that the palette of the window has changed.
helpviewer_keywords: ["IOverlayNotify interface [DirectShow]","OnPaletteChange method","IOverlayNotify.OnPaletteChange","IOverlayNotify::OnPaletteChange","IOverlayNotifyOnPaletteChange","OnPaletteChange","OnPaletteChange method [DirectShow]","OnPaletteChange method [DirectShow]","IOverlayNotify interface","dshow.ioverlaynotify_onpalettechange","strmif/IOverlayNotify::OnPaletteChange"]
old-location: dshow\ioverlaynotify_onpalettechange.htm
tech.root: dshow
ms.assetid: 128e3834-d561-46d3-b32b-5bfd290f0995
ms.date: 12/05/2018
ms.keywords: IOverlayNotify interface [DirectShow],OnPaletteChange method, IOverlayNotify.OnPaletteChange, IOverlayNotify::OnPaletteChange, IOverlayNotifyOnPaletteChange, OnPaletteChange, OnPaletteChange method [DirectShow], OnPaletteChange method [DirectShow],IOverlayNotify interface, dshow.ioverlaynotify_onpalettechange, strmif/IOverlayNotify::OnPaletteChange
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
 - IOverlayNotify::OnPaletteChange
 - strmif/IOverlayNotify::OnPaletteChange
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
 - IOverlayNotify.OnPaletteChange
---

# IOverlayNotify::OnPaletteChange


## -description

The <code>OnPaletteChange</code> method provides notification that the palette of the window has changed.

## -parameters

### -param dwColors [in]

Number of colors present.

### -param pPalette [in]

Pointer to the array of palette colors.

## -returns

Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.

## -remarks

Before returning, the filter should copy the array of <b>RGBQUAD</b> values, if necessary.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ioverlaynotify">IOverlayNotify Interface</a>