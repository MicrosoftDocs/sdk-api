---
UID: NF:wincodec.IWICBitmapLock.GetPixelFormat
title: IWICBitmapLock::GetPixelFormat
author: windows-sdk-content
description: Gets the pixel format of for the locked area of pixels. This can be used to compute the number of bytes-per-pixel in the locked area.
old-location: wic\_wic_codec_iwicbitmaplock_getpixelformat.htm
old-project: wic
ms.assetid: 2dfc6b0a-eb0f-416f-8123-17e5b93da612
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetPixelFormat, GetPixelFormat method [Windows Imaging Component], GetPixelFormat method [Windows Imaging Component],IWICBitmapLock interface, IWICBitmapLock interface [Windows Imaging Component],GetPixelFormat method, IWICBitmapLock.GetPixelFormat, IWICBitmapLock::GetPixelFormat, _wic_codec_iwicbitmaplock_getpixelformat, wic._wic_codec_iwicbitmaplock_getpixelformat, wincodec/IWICBitmapLock::GetPixelFormat
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
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICBitmapLock.GetPixelFormat
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapLock::GetPixelFormat


## -description


Gets the pixel format of for the locked area of pixels. This can be used to compute the number of bytes-per-pixel in the locked area.


## -parameters




### -param pPixelFormat [out]

Type: <b>WICPixelFormatGUID*</b>

A pointer that receives the pixel format GUID of the locked area.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



