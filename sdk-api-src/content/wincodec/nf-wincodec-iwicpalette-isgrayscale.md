---
UID: NF:wincodec.IWICPalette.IsGrayscale
title: IWICPalette::IsGrayscale (wincodec.h)
description: Retrieves a value that describes whether a palette is grayscale.
helpviewer_keywords: ["IWICPalette interface [Windows Imaging Component]","IsGrayscale method","IWICPalette.IsGrayscale","IWICPalette::IsGrayscale","IsGrayscale","IsGrayscale method [Windows Imaging Component]","IsGrayscale method [Windows Imaging Component]","IWICPalette interface","_wic_codec_iwicpalette_isgrayscale","wic._wic_codec_iwicpalette_isgrayscale","wincodec/IWICPalette::IsGrayscale"]
old-location: wic\_wic_codec_iwicpalette_isgrayscale.htm
tech.root: wic
ms.assetid: a559fa20-a967-4f8f-b978-f36365d3f00a
ms.date: 12/05/2018
ms.keywords: IWICPalette interface [Windows Imaging Component],IsGrayscale method, IWICPalette.IsGrayscale, IWICPalette::IsGrayscale, IsGrayscale, IsGrayscale method [Windows Imaging Component], IsGrayscale method [Windows Imaging Component],IWICPalette interface, _wic_codec_iwicpalette_isgrayscale, wic._wic_codec_iwicpalette_isgrayscale, wincodec/IWICPalette::IsGrayscale
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
 - IWICPalette::IsGrayscale
 - wincodec/IWICPalette::IsGrayscale
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
 - IWICPalette.IsGrayscale
---

# IWICPalette::IsGrayscale


## -description

Retrieves a value that describes whether a palette is grayscale.

## -parameters

### -param pfIsGrayscale [out]

Type: <b>BOOL*</b>

A pointer to a variable that receives a boolean value that indicates whether the palette is grayscale. <b>TRUE</b> indicates that the palette is grayscale; otherwise <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A palette is considered grayscale only if, for every entry, the alpha value is 0xFF and the red, green and blue values match.

