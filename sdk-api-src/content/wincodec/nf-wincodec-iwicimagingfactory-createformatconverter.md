---
UID: NF:wincodec.IWICImagingFactory.CreateFormatConverter
title: IWICImagingFactory::CreateFormatConverter (wincodec.h)
description: Creates a new instance of the IWICFormatConverter class.
old-location: wic\_wic_codec_iwicimagingfactory_createformatconverter.htm
tech.root: wic
ms.assetid: 50ceabdf-574e-4083-86a4-dddd4da06bbf
ms.date: 12/05/2018
ms.keywords: CreateFormatConverter, CreateFormatConverter method [Windows Imaging Component], CreateFormatConverter method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateFormatConverter method, IWICImagingFactory.CreateFormatConverter, IWICImagingFactory::CreateFormatConverter, _wic_codec_iwicimagingfactory_createformatconverter, wic._wic_codec_iwicimagingfactory_createformatconverter, wincodec/IWICImagingFactory::CreateFormatConverter
ms.topic: method
f1_keywords:
- wincodec/IWICImagingFactory.CreateFormatConverter
dev_langs:
- c++
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
- IWICImagingFactory.CreateFormatConverter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICImagingFactory::CreateFormatConverter


## -description


Creates a new instance of the <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter">IWICFormatConverter</a> class.


## -parameters




### -param ppIFormatConverter [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter">IWICFormatConverter</a>**</b>

A pointer that receives a pointer to a new <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter">IWICFormatConverter</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



