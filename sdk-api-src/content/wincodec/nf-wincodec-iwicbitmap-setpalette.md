---
UID: NF:wincodec.IWICBitmap.SetPalette
title: IWICBitmap::SetPalette
author: windows-sdk-content
description: Provides access for palette modifications.
old-location: wic\_wic_codec_iwicbitmap_setpalette.htm
old-project: wic
ms.assetid: a46c968e-9ff0-479e-8f98-0d2fbbc5d6b0
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IWICBitmap interface [Windows Imaging Component],SetPalette method, IWICBitmap.SetPalette, IWICBitmap::SetPalette, SetPalette, SetPalette method [Windows Imaging Component], SetPalette method [Windows Imaging Component],IWICBitmap interface, _wic_codec_iwicbitmap_setpalette, wic._wic_codec_iwicbitmap_setpalette, wincodec/IWICBitmap::SetPalette
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WICTiffCompressionOption
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICBitmap.SetPalette
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmap::SetPalette


## -description


Provides access for palette modifications.


## -parameters




### -param pIPalette [in]

Type: <b><a href="https://msdn.microsoft.com/cb0e4f92-4aff-48c7-af62-5f7154539289">IWICPalette</a>*</b>

The palette to use for conversion.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



