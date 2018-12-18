---
UID: NF:wincodec.IWICImagingFactory.CreateBitmapFromHBITMAP
title: IWICImagingFactory::CreateBitmapFromHBITMAP
author: windows-sdk-content
description: Creates an IWICBitmap from a bitmap handle.
old-location: wic\_wic_codec_iwicimagingfactory_createbitmapfromhbitmap.htm
tech.root: wic
ms.assetid: 8483f352-c31b-4afe-a011-ebef3430c576
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateBitmapFromHBITMAP, CreateBitmapFromHBITMAP method [Windows Imaging Component], CreateBitmapFromHBITMAP method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateBitmapFromHBITMAP method, IWICImagingFactory.CreateBitmapFromHBITMAP, IWICImagingFactory::CreateBitmapFromHBITMAP, _wic_codec_iwicimagingfactory_createbitmapfromhbitmap, wic._wic_codec_iwicimagingfactory_createbitmapfromhbitmap, wincodec/IWICImagingFactory::CreateBitmapFromHBITMAP
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
 - IWICImagingFactory.CreateBitmapFromHBITMAP
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICImagingFactory::CreateBitmapFromHBITMAP


## -description


Creates an <a href="https://msdn.microsoft.com/15dcc80d-ef58-453d-a57a-348ffc7ddc6b">IWICBitmap</a> from a bitmap handle.


## -parameters




### -param hBitmap [in]

Type: <b>HBITMAP</b>

A bitmap handle to create the bitmap from.


### -param hPalette [in]

Type: <b>HPALETTE</b>

A palette handle used to create the bitmap.


### -param options [in]

Type: <b><a href="https://msdn.microsoft.com/caa10c35-9af4-4310-b031-3347cf795087">WICBitmapAlphaChannelOption</a></b>

The alpha channel options to create the bitmap.


### -param ppIBitmap [out]

Type: <b><a href="https://msdn.microsoft.com/15dcc80d-ef58-453d-a57a-348ffc7ddc6b">IWICBitmap</a>**</b>

A pointer that receives a pointer to the new bitmap.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For a non-palletized bitmap, set NULL for the <i>hPalette</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">GDI+ Bitmap class</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536295(v=VS.85).aspx">GDI+ Bitmap.GetHBITMAP method</a>



<a href="https://msdn.microsoft.com/30d155b1-a46c-46c4-9f8f-fb56dc6bf0a9">IWICImagingFactory</a>



<a href="https://msdn.microsoft.com/caa10c35-9af4-4310-b031-3347cf795087">WICBitmapAlphaChannelOption</a>
 

 

