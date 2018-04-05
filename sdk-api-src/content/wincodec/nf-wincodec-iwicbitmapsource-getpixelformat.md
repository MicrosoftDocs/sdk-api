---
UID: NF:wincodec.IWICBitmapSource.GetPixelFormat
title: IWICBitmapSource::GetPixelFormat method
author: windows-driver-content
description: Retrieves the pixel format of the bitmap source..
old-location: wic\_wic_codec_iwicbitmapsource_getpixelformat.htm
old-project: wic
ms.assetid: 6fd30a38-a447-4e4e-93ea-e31c5ba1271e
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: GetPixelFormat method [Windows Imaging Component], GetPixelFormat method [Windows Imaging Component], IWICBitmapSource interface, GetPixelFormat,IWICBitmapSource.GetPixelFormat, IWICBitmapSource, IWICBitmapSource interface [Windows Imaging Component], GetPixelFormat method, IWICBitmapSource::GetPixelFormat, _wic_codec_iwicbitmapsource_getpixelformat, wic._wic_codec_iwicbitmapsource_getpixelformat, wincodec/IWICBitmapSource::GetPixelFormat
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
-	IWICBitmapSource.GetPixelFormat
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapSource::GetPixelFormat method


## -description


Retrieves the pixel format of the bitmap source.. 


## -parameters




### -param pPixelFormat [out]

Type: <b>WICPixelFormatGUID*</b>

Receives the pixel format GUID the bitmap is stored in. For a list of available pixel formats, see the <a href="https://msdn.microsoft.com/348b6d15-e339-4dce-99f3-4d639ee9bf7d">Native Pixel Formats</a> topic.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




            The pixel format returned by this method is not necessarily the pixel format the image is stored as.
            The codec may perform a format conversion from the storage pixel format to an output pixel format.
         



