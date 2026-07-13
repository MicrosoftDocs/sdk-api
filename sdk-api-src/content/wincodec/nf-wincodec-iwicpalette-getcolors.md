---
UID: NF:wincodec.IWICPalette.GetColors
title: IWICPalette::GetColors (wincodec.h)
description: Fills out the supplied color array with the colors from the internal color table. The color array should be sized according to the return results from GetColorCount.
helpviewer_keywords: ["GetColors","GetColors method [Windows Imaging Component]","GetColors method [Windows Imaging Component]","IWICPalette interface","IWICPalette interface [Windows Imaging Component]","GetColors method","IWICPalette.GetColors","IWICPalette::GetColors","_wic_codec_iwicpalette_getcolors","wic._wic_codec_iwicpalette_getcolors","wincodec/IWICPalette::GetColors"]
old-location: wic\_wic_codec_iwicpalette_getcolors.htm
tech.root: wic
ms.assetid: efec97fd-251c-4e52-b92e-4e624cdb9881
ms.date: 12/05/2018
ms.keywords: GetColors, GetColors method [Windows Imaging Component], GetColors method [Windows Imaging Component],IWICPalette interface, IWICPalette interface [Windows Imaging Component],GetColors method, IWICPalette.GetColors, IWICPalette::GetColors, _wic_codec_iwicpalette_getcolors, wic._wic_codec_iwicpalette_getcolors, wincodec/IWICPalette::GetColors
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
 - IWICPalette::GetColors
 - wincodec/IWICPalette::GetColors
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
 - IWICPalette.GetColors
---

# IWICPalette::GetColors


## -description

Fills out the supplied color array with the colors from the internal color table. The color array should be sized according to the return results from <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicpalette-getcolorcount">GetColorCount</a>.

## -parameters

### -param cCount [in]

Type: <b>UINT</b>

The size of the <i>pColors</i> array.

### -param pColors [out]

Type: <b>WICColor*</b>

Pointer that receives the colors of the palette.

### -param pcActualColors [out]

Type: <b>UINT*</b>

The actual size needed to obtain the palette colors.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.