---
UID: NF:wincodec.IWICPalette.InitializeFromPalette
title: IWICPalette::InitializeFromPalette (wincodec.h)
description: Initialize the palette based on a given palette.
helpviewer_keywords: ["IWICPalette interface [Windows Imaging Component]","InitializeFromPalette method","IWICPalette.InitializeFromPalette","IWICPalette::InitializeFromPalette","InitializeFromPalette","InitializeFromPalette method [Windows Imaging Component]","InitializeFromPalette method [Windows Imaging Component]","IWICPalette interface","_wic_codec_iwicpalette_initializefrompalette","wic._wic_codec_iwicpalette_initializefrompalette","wincodec/IWICPalette::InitializeFromPalette"]
old-location: wic\_wic_codec_iwicpalette_initializefrompalette.htm
tech.root: wic
ms.assetid: c1e27b1a-5103-4111-8356-f35d53a07f4b
ms.date: 12/05/2018
ms.keywords: IWICPalette interface [Windows Imaging Component],InitializeFromPalette method, IWICPalette.InitializeFromPalette, IWICPalette::InitializeFromPalette, InitializeFromPalette, InitializeFromPalette method [Windows Imaging Component], InitializeFromPalette method [Windows Imaging Component],IWICPalette interface, _wic_codec_iwicpalette_initializefrompalette, wic._wic_codec_iwicpalette_initializefrompalette, wincodec/IWICPalette::InitializeFromPalette
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
 - IWICPalette::InitializeFromPalette
 - wincodec/IWICPalette::InitializeFromPalette
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
 - IWICPalette.InitializeFromPalette
---

# IWICPalette::InitializeFromPalette


## -description

Initialize the palette based on a given palette.

## -parameters

### -param pIPalette [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicpalette">IWICPalette</a>*</b>

Pointer to the source palette.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.