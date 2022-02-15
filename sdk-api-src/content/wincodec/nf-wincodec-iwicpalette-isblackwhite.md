---
UID: NF:wincodec.IWICPalette.IsBlackWhite
title: IWICPalette::IsBlackWhite (wincodec.h)
description: Retrieves a value that describes whether the palette is black and white.
helpviewer_keywords: ["IWICPalette interface [Windows Imaging Component]","IsBlackWhite method","IWICPalette.IsBlackWhite","IWICPalette::IsBlackWhite","IsBlackWhite","IsBlackWhite method [Windows Imaging Component]","IsBlackWhite method [Windows Imaging Component]","IWICPalette interface","_wic_codec_iwicpalette_isblackwhite","wic._wic_codec_iwicpalette_isblackwhite","wincodec/IWICPalette::IsBlackWhite"]
old-location: wic\_wic_codec_iwicpalette_isblackwhite.htm
tech.root: wic
ms.assetid: a22603b9-5c23-4016-9f28-1cf420ac11fa
ms.date: 12/05/2018
ms.keywords: IWICPalette interface [Windows Imaging Component],IsBlackWhite method, IWICPalette.IsBlackWhite, IWICPalette::IsBlackWhite, IsBlackWhite, IsBlackWhite method [Windows Imaging Component], IsBlackWhite method [Windows Imaging Component],IWICPalette interface, _wic_codec_iwicpalette_isblackwhite, wic._wic_codec_iwicpalette_isblackwhite, wincodec/IWICPalette::IsBlackWhite
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
 - IWICPalette::IsBlackWhite
 - wincodec/IWICPalette::IsBlackWhite
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
 - IWICPalette.IsBlackWhite
---

# IWICPalette::IsBlackWhite


## -description

Retrieves a value that describes whether the palette is black and white.

## -parameters

### -param pfIsBlackWhite [out]

Type: <b>BOOL*</b>

A pointer to a variable  that receives a boolean value that indicates whether the palette is black and white. <b>TRUE</b> indicates that the palette is black and white; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A palette is considered to be black and white only if it contains exactly two entries, one full black (0xFF000000) and one full white (0xFFFFFFF).

