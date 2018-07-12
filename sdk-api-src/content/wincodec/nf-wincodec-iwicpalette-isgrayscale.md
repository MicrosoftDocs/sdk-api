---
UID: NF:wincodec.IWICPalette.IsGrayscale
title: IWICPalette::IsGrayscale
author: windows-sdk-content
description: Retrieves a value that describes whether a palette is grayscale.
old-location: wic\_wic_codec_iwicpalette_isgrayscale.htm
old-project: wic
ms.assetid: a559fa20-a967-4f8f-b978-f36365d3f00a
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IWICPalette interface [Windows Imaging Component],IsGrayscale method, IWICPalette.IsGrayscale, IWICPalette::IsGrayscale, IsGrayscale, IsGrayscale method [Windows Imaging Component], IsGrayscale method [Windows Imaging Component],IWICPalette interface, _wic_codec_iwicpalette_isgrayscale, wic._wic_codec_iwicpalette_isgrayscale, wincodec/IWICPalette::IsGrayscale
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
 - IWICPalette.IsGrayscale
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A palette is considered grayscale only if, for every entry, the alpha value is 0xFF and the red, green and blue values match.




