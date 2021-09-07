---
UID: NF:wincodec.IWICBitmapLock.GetPixelFormat
title: IWICBitmapLock::GetPixelFormat (wincodec.h)
description: Gets the pixel format of for the locked area of pixels. This can be used to compute the number of bytes-per-pixel in the locked area.
helpviewer_keywords: ["GetPixelFormat","GetPixelFormat method [Windows Imaging Component]","GetPixelFormat method [Windows Imaging Component]","IWICBitmapLock interface","IWICBitmapLock interface [Windows Imaging Component]","GetPixelFormat method","IWICBitmapLock.GetPixelFormat","IWICBitmapLock::GetPixelFormat","_wic_codec_iwicbitmaplock_getpixelformat","wic._wic_codec_iwicbitmaplock_getpixelformat","wincodec/IWICBitmapLock::GetPixelFormat"]
old-location: wic\_wic_codec_iwicbitmaplock_getpixelformat.htm
tech.root: wic
ms.assetid: 2dfc6b0a-eb0f-416f-8123-17e5b93da612
ms.date: 12/05/2018
ms.keywords: GetPixelFormat, GetPixelFormat method [Windows Imaging Component], GetPixelFormat method [Windows Imaging Component],IWICBitmapLock interface, IWICBitmapLock interface [Windows Imaging Component],GetPixelFormat method, IWICBitmapLock.GetPixelFormat, IWICBitmapLock::GetPixelFormat, _wic_codec_iwicbitmaplock_getpixelformat, wic._wic_codec_iwicbitmaplock_getpixelformat, wincodec/IWICBitmapLock::GetPixelFormat
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
 - IWICBitmapLock::GetPixelFormat
 - wincodec/IWICBitmapLock::GetPixelFormat
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
 - IWICBitmapLock.GetPixelFormat
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

