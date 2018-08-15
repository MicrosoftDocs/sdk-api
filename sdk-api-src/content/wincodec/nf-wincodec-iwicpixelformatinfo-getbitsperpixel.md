---
UID: NF:wincodec.IWICPixelFormatInfo.GetBitsPerPixel
title: IWICPixelFormatInfo::GetBitsPerPixel
author: windows-sdk-content
description: Gets the bits per pixel (BPP) of the pixel format.
old-location: wic\_wic_codec_iwicpixelformatinfo_getbitsperpixel.htm
old-project: wic
ms.assetid: 484fb014-5999-46b9-8e32-3fd5296e483f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetBitsPerPixel, GetBitsPerPixel method [Windows Imaging Component], GetBitsPerPixel method [Windows Imaging Component],IWICPixelFormatInfo interface, IWICPixelFormatInfo interface [Windows Imaging Component],GetBitsPerPixel method, IWICPixelFormatInfo.GetBitsPerPixel, IWICPixelFormatInfo::GetBitsPerPixel, _wic_codec_iwicpixelformatinfo_getbitsperpixel, wic._wic_codec_iwicpixelformatinfo_getbitsperpixel, wincodec/IWICPixelFormatInfo::GetBitsPerPixel
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WICTiffCompressionOption
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.lib
 - Windowscodecs.dll
api_name:
 - IWICPixelFormatInfo.GetBitsPerPixel
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICPixelFormatInfo::GetBitsPerPixel


## -description


Gets the bits per pixel (BPP) of the pixel format.


## -parameters




### -param puiBitsPerPixel [out]

Type: <b>UINT*</b>

Pointer that receives the BPP of the pixel format.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



