---
UID: NF:wincodec.IWICPlanarFormatConverter.Initialize
title: IWICPlanarFormatConverter::Initialize (wincodec.h)
description: Initializes a format converter with a planar source, and specifies the interleaved output pixel format.
helpviewer_keywords: ["IWICPlanarFormatConverter interface [Windows Imaging Component]","Initialize method","IWICPlanarFormatConverter.Initialize","IWICPlanarFormatConverter::Initialize","Initialize","Initialize method [Windows Imaging Component]","Initialize method [Windows Imaging Component]","IWICPlanarFormatConverter interface","wic.iwicplanarformatconverter_initialize","wincodec/IWICPlanarFormatConverter::Initialize"]
old-location: wic\iwicplanarformatconverter_initialize.htm
tech.root: wic
ms.assetid: 0EEF6940-627A-4615-90C0-196AAB36843E
ms.date: 12/05/2018
ms.keywords: IWICPlanarFormatConverter interface [Windows Imaging Component],Initialize method, IWICPlanarFormatConverter.Initialize, IWICPlanarFormatConverter::Initialize, Initialize, Initialize method [Windows Imaging Component], Initialize method [Windows Imaging Component],IWICPlanarFormatConverter interface, wic.iwicplanarformatconverter_initialize, wincodec/IWICPlanarFormatConverter::Initialize
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - IWICPlanarFormatConverter::Initialize
 - wincodec/IWICPlanarFormatConverter::Initialize
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
 - IWICPlanarFormatConverter.Initialize
---

# IWICPlanarFormatConverter::Initialize


## -description

Initializes a format converter with a planar source, and specifies the interleaved output pixel format.

## -parameters

### -param ppPlanes [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>**</b>

An array of <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a> that represents image planes.

### -param cPlanes

Type: <b>UINT</b>

The number of component planes specified by the planes parameter.

### -param dstFormat

Type: <b>REFWICPixelFormatGUID </b>

The destination interleaved pixel format.

### -param dither

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmapdithertype">WICBitmapDitherType</a></b>

The <a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmapdithertype">WICBitmapDitherType</a> used for conversion.

### -param pIPalette

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicpalette">IWICPalette</a>*</b>

The palette to use for conversion.

### -param alphaThresholdPercent

Type: <b>double</b>

The alpha threshold to use for conversion.

### -param paletteTranslate

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmappalettetype">WICBitmapPaletteType</a></b>

The palette translation type to use for conversion.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicplanarformatconverter-initialize">IWICFormatConverter::Initialize</a>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicplanarformatconverter">IWICPlanarFormatConverter</a>