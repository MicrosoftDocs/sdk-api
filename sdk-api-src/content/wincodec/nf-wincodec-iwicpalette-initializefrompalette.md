---
UID: NF:wincodec.IWICPalette.InitializeFromPalette
title: IWICPalette::InitializeFromPalette
author: windows-driver-content
description: Initialize the palette based on a given palette.
old-location: wic\_wic_codec_iwicpalette_initializefrompalette.htm
old-project: wic
ms.assetid: c1e27b1a-5103-4111-8356-f35d53a07f4b
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IWICPalette interface [Windows Imaging Component],InitializeFromPalette method, IWICPalette.InitializeFromPalette, IWICPalette::InitializeFromPalette, InitializeFromPalette, InitializeFromPalette method [Windows Imaging Component], InitializeFromPalette method [Windows Imaging Component],IWICPalette interface, _wic_codec_iwicpalette_initializefrompalette, wic._wic_codec_iwicpalette_initializefrompalette, wincodec/IWICPalette::InitializeFromPalette
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
-	IWICPalette.InitializeFromPalette
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICPalette::InitializeFromPalette


## -description


Initialize the palette based on a given palette.


## -parameters




### -param pIPalette






#### - pIMILPalette [in]

Type: <b><a href="https://msdn.microsoft.com/cb0e4f92-4aff-48c7-af62-5f7154539289">IWICPalette</a>*</b>

Pointer to the source palette.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



