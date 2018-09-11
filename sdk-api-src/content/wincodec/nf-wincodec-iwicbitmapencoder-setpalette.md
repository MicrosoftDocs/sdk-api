---
UID: NF:wincodec.IWICBitmapEncoder.SetPalette
title: IWICBitmapEncoder::SetPalette
author: windows-sdk-content
description: Sets the global palette for the image.
old-location: wic\_wic_codec_iwicbitmapencoder_setpalette.htm
tech.root: wic
ms.assetid: 9310f407-d310-402b-bd90-ebc7e8d99361
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWICBitmapEncoder interface [Windows Imaging Component],SetPalette method, IWICBitmapEncoder.SetPalette, IWICBitmapEncoder::SetPalette, SetPalette, SetPalette method [Windows Imaging Component], SetPalette method [Windows Imaging Component],IWICBitmapEncoder interface, _wic_codec_iwicbitmapencoder_setpalette, wic._wic_codec_iwicbitmapencoder_setpalette, wincodec/IWICBitmapEncoder::SetPalette
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
 - IWICBitmapEncoder.SetPalette
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICBitmapEncoder::SetPalette


## -description


Sets the global palette for the image.


## -parameters




### -param pIPalette [in]

Type: <b><a href="https://msdn.microsoft.com/cb0e4f92-4aff-48c7-af62-5f7154539289">IWICPalette</a>*</b>

The <a href="https://msdn.microsoft.com/cb0e4f92-4aff-48c7-af62-5f7154539289">IWICPalette</a> to use as the global palette.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise.
            

Returns WINCODEC_ERR_UNSUPPORTEDOPERATION if the feature is not supported by the encoder.




## -remarks



Only GIF images support an optional global palette, and you must set the global palette before adding any frames to the image. You only need to set the palette for indexed pixel formats.




