---
UID: NF:wincodec.IWICImagingFactory.CreateBitmapFromHICON
title: IWICImagingFactory::CreateBitmapFromHICON
author: windows-sdk-content
description: Creates an IWICBitmap from an icon handle.
old-location: wic\_wic_codec_iwicimagingfactory_createbitmapfromhicon.htm
old-project: wic
ms.assetid: a67695a1-30ac-4e28-a9a9-582601139e17
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateBitmapFromHICON, CreateBitmapFromHICON method [Windows Imaging Component], CreateBitmapFromHICON method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateBitmapFromHICON method, IWICImagingFactory.CreateBitmapFromHICON, IWICImagingFactory::CreateBitmapFromHICON, _wic_codec_iwicimagingfactory_createbitmapfromhicon, wic._wic_codec_iwicimagingfactory_createbitmapfromhicon, wincodec/IWICImagingFactory::CreateBitmapFromHICON
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
 - Windowscodecs.dll
api_name:
 - IWICImagingFactory.CreateBitmapFromHICON
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICImagingFactory::CreateBitmapFromHICON


## -description


Creates an <a href="https://msdn.microsoft.com/15dcc80d-ef58-453d-a57a-348ffc7ddc6b">IWICBitmap</a> from an icon handle.


## -parameters




### -param hIcon [in]

Type: <b>HICON</b>

The icon handle to create the new bitmap from.


### -param ppIBitmap [out]

Type: <b><a href="https://msdn.microsoft.com/15dcc80d-ef58-453d-a57a-348ffc7ddc6b">IWICBitmap</a>**</b>

A pointer that receives a pointer to the new bitmap.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



