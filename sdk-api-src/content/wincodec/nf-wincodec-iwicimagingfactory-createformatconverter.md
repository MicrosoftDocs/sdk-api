---
UID: NF:wincodec.IWICImagingFactory.CreateFormatConverter
title: IWICImagingFactory::CreateFormatConverter
author: windows-sdk-content
description: Creates a new instance of the IWICFormatConverter class.
old-location: wic\_wic_codec_iwicimagingfactory_createformatconverter.htm
old-project: wic
ms.assetid: 50ceabdf-574e-4083-86a4-dddd4da06bbf
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateFormatConverter, CreateFormatConverter method [Windows Imaging Component], CreateFormatConverter method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateFormatConverter method, IWICImagingFactory.CreateFormatConverter, IWICImagingFactory::CreateFormatConverter, _wic_codec_iwicimagingfactory_createformatconverter, wic._wic_codec_iwicimagingfactory_createformatconverter, wincodec/IWICImagingFactory::CreateFormatConverter
ms.prod: windows
ms.technology: windows-sdk
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
 - IWICImagingFactory.CreateFormatConverter
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICImagingFactory::CreateFormatConverter


## -description


Creates a new instance of the <a href="https://msdn.microsoft.com/d558aaa7-5962-424c-9e83-363fba09ad50">IWICFormatConverter</a> class.


## -parameters




### -param ppIFormatConverter [out]

Type: <b><a href="https://msdn.microsoft.com/d558aaa7-5962-424c-9e83-363fba09ad50">IWICFormatConverter</a>**</b>

A pointer that receives a pointer to a new <a href="https://msdn.microsoft.com/d558aaa7-5962-424c-9e83-363fba09ad50">IWICFormatConverter</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



