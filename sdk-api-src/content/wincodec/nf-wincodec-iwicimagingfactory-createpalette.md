---
UID: NF:wincodec.IWICImagingFactory.CreatePalette
title: IWICImagingFactory::CreatePalette
author: windows-driver-content
description: Creates a new instance of the IWICPalette class.
old-location: wic\_wic_codec_iwicimagingfactory_createpalette.htm
old-project: wic
ms.assetid: 135440ee-ea70-40da-9ee1-618a8e10170a
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: CreatePalette, CreatePalette method [Windows Imaging Component], CreatePalette method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreatePalette method, IWICImagingFactory.CreatePalette, IWICImagingFactory::CreatePalette, _wic_codec_iwicimagingfactory_createpalette, wic._wic_codec_iwicimagingfactory_createpalette, wincodec/IWICImagingFactory::CreatePalette
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
-	IWICImagingFactory.CreatePalette
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICImagingFactory::CreatePalette


## -description


Creates a new instance of the <a href="https://msdn.microsoft.com/cb0e4f92-4aff-48c7-af62-5f7154539289">IWICPalette</a> class.


## -parameters




### -param ppIPalette [out]

Type: <b><a href="https://msdn.microsoft.com/cb0e4f92-4aff-48c7-af62-5f7154539289">IWICPalette</a>**</b>

A pointer that receives a pointer to a new <a href="https://msdn.microsoft.com/cb0e4f92-4aff-48c7-af62-5f7154539289">IWICPalette</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



