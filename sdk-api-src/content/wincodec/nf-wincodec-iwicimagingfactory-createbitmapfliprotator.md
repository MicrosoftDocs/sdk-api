---
UID: NF:wincodec.IWICImagingFactory.CreateBitmapFlipRotator
title: IWICImagingFactory::CreateBitmapFlipRotator
author: windows-sdk-content
description: Creates a new instance of an IWICBitmapFlipRotator object.
old-location: wic\_wic_codec_iwicimagingfactory_createbitmapfliprotator.htm
old-project: wic
ms.assetid: ec044a38-b39d-4421-8e56-a8be0586cc49
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: CreateBitmapFlipRotator, CreateBitmapFlipRotator method [Windows Imaging Component], CreateBitmapFlipRotator method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateBitmapFlipRotator method, IWICImagingFactory.CreateBitmapFlipRotator, IWICImagingFactory::CreateBitmapFlipRotator, _wic_codec_iwicimagingfactory_createbitmapfliprotator, wic._wic_codec_iwicimagingfactory_createbitmapfliprotator, wincodec/IWICImagingFactory::CreateBitmapFlipRotator
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
 - IWICImagingFactory.CreateBitmapFlipRotator
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICImagingFactory::CreateBitmapFlipRotator


## -description


Creates a new instance of an <a href="https://msdn.microsoft.com/1fcb19ba-34bd-48c0-9964-0c973c31cacc">IWICBitmapFlipRotator</a> object.


## -parameters




### -param ppIBitmapFlipRotator [out]

Type: <b><a href="https://msdn.microsoft.com/1fcb19ba-34bd-48c0-9964-0c973c31cacc">IWICBitmapFlipRotator</a>**</b>

A pointer that receives a pointer to a new <a href="https://msdn.microsoft.com/1fcb19ba-34bd-48c0-9964-0c973c31cacc">IWICBitmapFlipRotator</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



