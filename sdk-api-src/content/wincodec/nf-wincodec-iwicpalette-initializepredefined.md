---
UID: NF:wincodec.IWICPalette.InitializePredefined
title: IWICPalette::InitializePredefined (wincodec.h)
description: Initializes the palette to one of the pre-defined palettes specified by WICBitmapPaletteType and optionally adds a transparent color.
helpviewer_keywords: ["IWICPalette interface [Windows Imaging Component]","InitializePredefined method","IWICPalette.InitializePredefined","IWICPalette::InitializePredefined","InitializePredefined","InitializePredefined method [Windows Imaging Component]","InitializePredefined method [Windows Imaging Component]","IWICPalette interface","_wic_codec_iwicpalette_initializepredefined","wic._wic_codec_iwicpalette_initializepredefined","wincodec/IWICPalette::InitializePredefined"]
old-location: wic\_wic_codec_iwicpalette_initializepredefined.htm
tech.root: wic
ms.assetid: 507888ad-4e3f-4e31-83c4-63a473eb7681
ms.date: 12/05/2018
ms.keywords: IWICPalette interface [Windows Imaging Component],InitializePredefined method, IWICPalette.InitializePredefined, IWICPalette::InitializePredefined, InitializePredefined, InitializePredefined method [Windows Imaging Component], InitializePredefined method [Windows Imaging Component],IWICPalette interface, _wic_codec_iwicpalette_initializepredefined, wic._wic_codec_iwicpalette_initializepredefined, wincodec/IWICPalette::InitializePredefined
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
 - IWICPalette::InitializePredefined
 - wincodec/IWICPalette::InitializePredefined
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
 - IWICPalette.InitializePredefined
---

# IWICPalette::InitializePredefined


## -description

Initializes the palette to one of the pre-defined palettes specified by <a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmappalettetype">WICBitmapPaletteType</a> and optionally adds a transparent color.

## -parameters

### -param ePaletteType [in]

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmappalettetype">WICBitmapPaletteType</a></b>

The desired pre-defined palette type.

### -param fAddTransparentColor [in]

Type: <b>BOOL</b>

The optional transparent color to add to the palette. If no transparent color is needed, use 0. When initializing to a grayscale or black and white palette, set this parameter to <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If a transparent color is added to a palette, the palette is no longer predefined and is returned as <a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmappalettetype">WICBitmapPaletteTypeCustom</a>. For palettes with less than 256 entries, the transparent entry is added to the end of the palette (that is, a 16-color palette becomes a 17-color palette). For palettes with 256 colors, the transparent palette entry will replace the last entry in the pre-defined palette.