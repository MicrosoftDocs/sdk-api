---
UID: NF:wincodec.IWICImagingFactory.CreateBitmapScaler
title: IWICImagingFactory::CreateBitmapScaler
author: windows-sdk-content
description: Creates a new instance of an IWICBitmapScaler.
old-location: wic\_wic_codec_iwicimagingfactory_createbitmapscaler.htm
old-project: wic
ms.assetid: 4da6b185-4a94-4032-a1d6-e64b96a5da97
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: CreateBitmapScaler, CreateBitmapScaler method [Windows Imaging Component], CreateBitmapScaler method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateBitmapScaler method, IWICImagingFactory.CreateBitmapScaler, IWICImagingFactory::CreateBitmapScaler, _wic_codec_iwicimagingfactory_createbitmapscaler, wic._wic_codec_iwicimagingfactory_createbitmapscaler, wincodec/IWICImagingFactory::CreateBitmapScaler
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
 - IWICImagingFactory.CreateBitmapScaler
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICImagingFactory::CreateBitmapScaler


## -description


Creates a new instance of an <a href="https://msdn.microsoft.com/cc14be9d-d750-40db-a95f-309b392cefe8">IWICBitmapScaler</a>.


## -parameters




### -param ppIBitmapScaler [out]

Type: <b><a href="https://msdn.microsoft.com/cc14be9d-d750-40db-a95f-309b392cefe8">IWICBitmapScaler</a>**</b>

A pointer that receives a pointer to a new <a href="https://msdn.microsoft.com/cc14be9d-d750-40db-a95f-309b392cefe8">IWICBitmapScaler</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



