---
UID: NF:wincodec.IWICPalette.HasAlpha
title: IWICPalette::HasAlpha (wincodec.h)
description: Indicates whether the palette contains an entry that is non-opaque (that is, an entry with an alpha that is less than 1).
helpviewer_keywords: ["HasAlpha","HasAlpha method [Windows Imaging Component]","HasAlpha method [Windows Imaging Component]","IWICPalette interface","IWICPalette interface [Windows Imaging Component]","HasAlpha method","IWICPalette.HasAlpha","IWICPalette::HasAlpha","_wic_codec_iwicpalette_hasalpha","wic._wic_codec_iwicpalette_hasalpha","wincodec/IWICPalette::HasAlpha"]
old-location: wic\_wic_codec_iwicpalette_hasalpha.htm
tech.root: wic
ms.assetid: 7c2cd523-04e4-4f19-b7f3-cc2af7604283
ms.date: 12/05/2018
ms.keywords: HasAlpha, HasAlpha method [Windows Imaging Component], HasAlpha method [Windows Imaging Component],IWICPalette interface, IWICPalette interface [Windows Imaging Component],HasAlpha method, IWICPalette.HasAlpha, IWICPalette::HasAlpha, _wic_codec_iwicpalette_hasalpha, wic._wic_codec_iwicpalette_hasalpha, wincodec/IWICPalette::HasAlpha
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
 - IWICPalette::HasAlpha
 - wincodec/IWICPalette::HasAlpha
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
 - IWICPalette.HasAlpha
---

# IWICPalette::HasAlpha


## -description

Indicates whether the palette contains an entry that is non-opaque (that is, an entry with an alpha that is less than 1).

## -parameters

### -param pfHasAlpha [out]

Type: <b>BOOL*</b>

Pointer that receives <code>TRUE</code> if the palette contains a transparent color; otherwise, <code>FALSE</code>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Various image formats support alpha in different ways. PNG has full alpha support by supporting partially transparent palette entries. GIF stores colors as 24bpp, without alpha, but allows one palette entry to be specified as fully transparent. If a palette has multiple fully transparent entries (0x00RRGGBB), GIF will use the last one as its transparent index.

