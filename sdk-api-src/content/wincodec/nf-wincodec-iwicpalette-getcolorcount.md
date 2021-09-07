---
UID: NF:wincodec.IWICPalette.GetColorCount
title: IWICPalette::GetColorCount (wincodec.h)
description: Retrieves the number of colors in the color table.
helpviewer_keywords: ["GetColorCount","GetColorCount method [Windows Imaging Component]","GetColorCount method [Windows Imaging Component]","IWICPalette interface","IWICPalette interface [Windows Imaging Component]","GetColorCount method","IWICPalette.GetColorCount","IWICPalette::GetColorCount","_wic_codec_iwicpalette_getcolorcount","wic._wic_codec_iwicpalette_getcolorcount","wincodec/IWICPalette::GetColorCount"]
old-location: wic\_wic_codec_iwicpalette_getcolorcount.htm
tech.root: wic
ms.assetid: 133ee983-8df2-4053-aa8a-471aa679b412
ms.date: 12/05/2018
ms.keywords: GetColorCount, GetColorCount method [Windows Imaging Component], GetColorCount method [Windows Imaging Component],IWICPalette interface, IWICPalette interface [Windows Imaging Component],GetColorCount method, IWICPalette.GetColorCount, IWICPalette::GetColorCount, _wic_codec_iwicpalette_getcolorcount, wic._wic_codec_iwicpalette_getcolorcount, wincodec/IWICPalette::GetColorCount
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
 - IWICPalette::GetColorCount
 - wincodec/IWICPalette::GetColorCount
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
 - IWICPalette.GetColorCount
---

# IWICPalette::GetColorCount


## -description

Retrieves the number of colors in the color table.

## -parameters

### -param pcCount [out]

Type: <b>UINT*</b>

Pointer that receives the number of colors in the color table.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

