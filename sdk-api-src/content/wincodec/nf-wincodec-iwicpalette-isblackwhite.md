---
UID: NF:wincodec.IWICPalette.IsBlackWhite
title: IWICPalette::IsBlackWhite
author: windows-driver-content
description: Retrieves a value that describes whether the palette is black and white.
old-location: wic\_wic_codec_iwicpalette_isblackwhite.htm
old-project: wic
ms.assetid: a22603b9-5c23-4016-9f28-1cf420ac11fa
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: IWICPalette interface [Windows Imaging Component],IsBlackWhite method, IWICPalette.IsBlackWhite, IWICPalette::IsBlackWhite, IsBlackWhite, IsBlackWhite method [Windows Imaging Component], IsBlackWhite method [Windows Imaging Component],IWICPalette interface, _wic_codec_iwicpalette_isblackwhite, wic._wic_codec_iwicpalette_isblackwhite, wincodec/IWICPalette::IsBlackWhite
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICPalette.IsBlackWhite
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A palette is considered to be black and white only if it contains exactly two entries, one full black (0xFF000000) and one full white (0xFFFFFFF).




