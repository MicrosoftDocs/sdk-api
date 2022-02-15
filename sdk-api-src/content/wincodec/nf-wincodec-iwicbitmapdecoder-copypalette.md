---
UID: NF:wincodec.IWICBitmapDecoder.CopyPalette
title: IWICBitmapDecoder::CopyPalette (wincodec.h)
description: Copies the decoder's IWICPalette .
helpviewer_keywords: ["CopyPalette","CopyPalette method [Windows Imaging Component]","CopyPalette method [Windows Imaging Component]","IWICBitmapDecoder interface","IWICBitmapDecoder interface [Windows Imaging Component]","CopyPalette method","IWICBitmapDecoder.CopyPalette","IWICBitmapDecoder::CopyPalette","_wic_codec_iwicbitmapdecoder_copypalette","wic._wic_codec_iwicbitmapdecoder_copypalette","wincodec/IWICBitmapDecoder::CopyPalette"]
old-location: wic\_wic_codec_iwicbitmapdecoder_copypalette.htm
tech.root: wic
ms.assetid: 4a387936-b045-42c7-b57c-1ac470640a14
ms.date: 12/05/2018
ms.keywords: CopyPalette, CopyPalette method [Windows Imaging Component], CopyPalette method [Windows Imaging Component],IWICBitmapDecoder interface, IWICBitmapDecoder interface [Windows Imaging Component],CopyPalette method, IWICBitmapDecoder.CopyPalette, IWICBitmapDecoder::CopyPalette, _wic_codec_iwicbitmapdecoder_copypalette, wic._wic_codec_iwicbitmapdecoder_copypalette, wincodec/IWICBitmapDecoder::CopyPalette
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
 - IWICBitmapDecoder::CopyPalette
 - wincodec/IWICBitmapDecoder::CopyPalette
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
 - IWICBitmapDecoder.CopyPalette
---

# IWICBitmapDecoder::CopyPalette


## -description

Copies the decoder's <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicpalette">IWICPalette</a> .

## -parameters

### -param pIPalette [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicpalette">IWICPalette</a>*</b>

An<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicpalette">IWICPalette</a> to which the decoder's global palette is to be copied. Use <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createpalette">CreatePalette</a> to create the destination palette before calling <b>CopyPalette</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>CopyPalette</b> returns a global palette (a palette that applies to all the frames in the image) if there is one; otherwise, it returns WINCODEC_ERR_PALETTEUNAVAILABLE. If an image doesn't have a global palette, it may still have a frame-level palette, which can be retrieved using <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypalette">IWICBitmapFrameDecode::CopyPalette</a>.