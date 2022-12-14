---
UID: NF:wincodec.IWICPalette.InitializeFromBitmap
title: IWICPalette::InitializeFromBitmap (wincodec.h)
description: Initializes a palette using a computed optimized values based on the reference bitmap.
helpviewer_keywords: ["IWICPalette interface [Windows Imaging Component]","InitializeFromBitmap method","IWICPalette.InitializeFromBitmap","IWICPalette::InitializeFromBitmap","InitializeFromBitmap","InitializeFromBitmap method [Windows Imaging Component]","InitializeFromBitmap method [Windows Imaging Component]","IWICPalette interface","_wic_codec_iwicpalette_initializefrombitmap","wic._wic_codec_iwicpalette_initializefrombitmap","wincodec/IWICPalette::InitializeFromBitmap"]
old-location: wic\_wic_codec_iwicpalette_initializefrombitmap.htm
tech.root: wic
ms.assetid: f17d0f16-729e-466c-902f-61398daf2921
ms.date: 12/05/2018
ms.keywords: IWICPalette interface [Windows Imaging Component],InitializeFromBitmap method, IWICPalette.InitializeFromBitmap, IWICPalette::InitializeFromBitmap, InitializeFromBitmap, InitializeFromBitmap method [Windows Imaging Component], InitializeFromBitmap method [Windows Imaging Component],IWICPalette interface, _wic_codec_iwicpalette_initializefrombitmap, wic._wic_codec_iwicpalette_initializefrombitmap, wincodec/IWICPalette::InitializeFromBitmap
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICPalette::InitializeFromBitmap
 - wincodec/IWICPalette::InitializeFromBitmap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICPalette.InitializeFromBitmap
---

# IWICPalette::InitializeFromBitmap


## -description

Initializes a palette using a computed optimized values based on the reference bitmap.

## -parameters

### -param pISurface [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>*</b>

Pointer to the source bitmap.

### -param cCount [in]

Type: <b>UINT</b>

The number of colors to initialize the palette with.

### -param fAddTransparentColor [in]

Type: <b>BOOL</b>

A value to indicate whether to add a transparent color.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The resulting palette contains the specified number of colors which best represent the colors present in the bitmap. The algorithm operates on the opaque RGB color value of each pixel in the reference bitmap and hence ignores any alpha values. If a transparent color is required, set the fAddTransparentColor parameter to <b>TRUE</b> and one fewer optimized color will be computed, reducing the <i>colorCount</i>, and a fully transparent color entry will be added.