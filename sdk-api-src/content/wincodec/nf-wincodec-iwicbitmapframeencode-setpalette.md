---
UID: NF:wincodec.IWICBitmapFrameEncode.SetPalette
title: IWICBitmapFrameEncode::SetPalette (wincodec.h)
description: Sets the IWICPalette for indexed pixel formats.
helpviewer_keywords: ["IWICBitmapFrameEncode interface [Windows Imaging Component]","SetPalette method","IWICBitmapFrameEncode.SetPalette","IWICBitmapFrameEncode::SetPalette","SetPalette","SetPalette method [Windows Imaging Component]","SetPalette method [Windows Imaging Component]","IWICBitmapFrameEncode interface","_wic_codec_iwicbitmapframeencode_setpalette","wic._wic_codec_iwicbitmapframeencode_setpalette","wincodec/IWICBitmapFrameEncode::SetPalette"]
old-location: wic\_wic_codec_iwicbitmapframeencode_setpalette.htm
tech.root: wic
ms.assetid: c463fc95-695d-4ba3-bf62-5b09d69c60c2
ms.date: 12/05/2018
ms.keywords: IWICBitmapFrameEncode interface [Windows Imaging Component],SetPalette method, IWICBitmapFrameEncode.SetPalette, IWICBitmapFrameEncode::SetPalette, SetPalette, SetPalette method [Windows Imaging Component], SetPalette method [Windows Imaging Component],IWICBitmapFrameEncode interface, _wic_codec_iwicbitmapframeencode_setpalette, wic._wic_codec_iwicbitmapframeencode_setpalette, wincodec/IWICBitmapFrameEncode::SetPalette
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
 - IWICBitmapFrameEncode::SetPalette
 - wincodec/IWICBitmapFrameEncode::SetPalette
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
 - IWICBitmapFrameEncode.SetPalette
---

# IWICBitmapFrameEncode::SetPalette


## -description

Sets the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicpalette">IWICPalette</a> for indexed pixel formats.

## -parameters

### -param pIPalette [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicpalette">IWICPalette</a>*</b>

The <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicpalette">IWICPalette</a> to use for indexed pixel formats.

The encoder may change the palette to reflect the pixel formats the encoder supports.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method doesn't fail if called on a frame whose pixel format is set to a non-indexed pixel format. If the target pixel format is a non-indexed format, the palette will be ignored.

If you already called <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapencoder-setpalette">IWICBitmapEncoder::SetPalette</a> to set a global palette, this method overrides that palette for the current frame.

The palette must be specified before your first call to <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicplanarbitmapframeencode-writepixels">WritePixels</a>/<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-writesource">WriteSource</a>. Doing so will cause <b>WriteSource</b> to use the specified palette when converting the source image to the encoder pixel format. If no palette is specified, a palette will be generated on the first call to <b>WriteSource</b>.