---
UID: NF:wincodec.IWICPalette.GetType
title: IWICPalette::GetType (wincodec.h)
description: Retrieves the WICBitmapPaletteType that describes the palette.
helpviewer_keywords: ["GetType","GetType method [Windows Imaging Component]","GetType method [Windows Imaging Component]","IWICPalette interface","IWICPalette interface [Windows Imaging Component]","GetType method","IWICPalette.GetType","IWICPalette::GetType","_wic_codec_iwicpalette_gettype","wic._wic_codec_iwicpalette_gettype","wincodec/IWICPalette::GetType"]
old-location: wic\_wic_codec_iwicpalette_gettype.htm
tech.root: wic
ms.assetid: 62b15cbb-60fd-496f-8dc6-2f5292fe4e76
ms.date: 12/05/2018
ms.keywords: GetType, GetType method [Windows Imaging Component], GetType method [Windows Imaging Component],IWICPalette interface, IWICPalette interface [Windows Imaging Component],GetType method, IWICPalette.GetType, IWICPalette::GetType, _wic_codec_iwicpalette_gettype, wic._wic_codec_iwicpalette_gettype, wincodec/IWICPalette::GetType
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
 - IWICPalette::GetType
 - wincodec/IWICPalette::GetType
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
 - IWICPalette.GetType
---

# IWICPalette::GetType


## -description

Retrieves the <a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmappalettetype">WICBitmapPaletteType</a> that describes the palette.

## -parameters

### -param pePaletteType [out]

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmappalettetype">WICBitmapPaletteType</a>*</b>

Pointer that receives the palette type of the bimtap.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>WICBitmapPaletteCustom</b> is used for palettes initialized from both <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicpalette-initializecustom">InitializeCustom</a> and <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicpalette-initializefrombitmap">InitializeFromBitmap</a>. There is no distinction is made between optimized and custom palettes.