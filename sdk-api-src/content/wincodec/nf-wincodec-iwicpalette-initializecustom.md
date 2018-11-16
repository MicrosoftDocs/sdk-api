---
UID: NF:wincodec.IWICPalette.InitializeCustom
title: IWICPalette::InitializeCustom
author: windows-sdk-content
description: Initializes a palette to the custom color entries provided.
old-location: wic\_wic_codec_iwicpalette_initializecustom.htm
tech.root: wic
ms.assetid: eef17030-13eb-4d59-ac47-a49ffe2c80c8
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWICPalette interface [Windows Imaging Component],InitializeCustom method, IWICPalette.InitializeCustom, IWICPalette::InitializeCustom, InitializeCustom, InitializeCustom method [Windows Imaging Component], InitializeCustom method [Windows Imaging Component],IWICPalette interface, _wic_codec_iwicpalette_initializecustom, wic._wic_codec_iwicpalette_initializecustom, wincodec/IWICPalette::InitializeCustom
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICPalette.InitializeCustom
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wincodec.h
: 
- IWICPalette.InitializeCustom
: 
---

# IWICPalette::InitializeCustom


## -description


Initializes a palette to the custom color entries provided.


## -parameters




### -param pColors [in]

Type: <b>WICColor*</b>

Pointer to the color array.


### -param cCount [in]

Type: <b>UINT</b>

The number of colors in <i>pColors</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If a transparent color is required, provide it as part of the custom entries. To add a transparent value to the palette, its alpha value must be 0 (0x00RRGGBB).


The entry count is limited to 256.



