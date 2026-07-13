---
UID: NF:wincodec.IWICBitmap.SetPalette
title: IWICBitmap::SetPalette (wincodec.h)
description: Provides access for palette modifications.
helpviewer_keywords: ["IWICBitmap interface [Windows Imaging Component]","SetPalette method","IWICBitmap.SetPalette","IWICBitmap::SetPalette","SetPalette","SetPalette method [Windows Imaging Component]","SetPalette method [Windows Imaging Component]","IWICBitmap interface","_wic_codec_iwicbitmap_setpalette","wic._wic_codec_iwicbitmap_setpalette","wincodec/IWICBitmap::SetPalette"]
old-location: wic\_wic_codec_iwicbitmap_setpalette.htm
tech.root: wic
ms.assetid: a46c968e-9ff0-479e-8f98-0d2fbbc5d6b0
ms.date: 12/05/2018
ms.keywords: IWICBitmap interface [Windows Imaging Component],SetPalette method, IWICBitmap.SetPalette, IWICBitmap::SetPalette, SetPalette, SetPalette method [Windows Imaging Component], SetPalette method [Windows Imaging Component],IWICBitmap interface, _wic_codec_iwicbitmap_setpalette, wic._wic_codec_iwicbitmap_setpalette, wincodec/IWICBitmap::SetPalette
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
 - IWICBitmap::SetPalette
 - wincodec/IWICBitmap::SetPalette
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
 - IWICBitmap.SetPalette
---

# IWICBitmap::SetPalette


## -description

Provides access for palette modifications.

## -parameters

### -param pIPalette [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicpalette">IWICPalette</a>*</b>

The palette to use for conversion.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.