---
UID: NF:wincodec.IWICBitmapFlipRotator.Initialize
title: IWICBitmapFlipRotator::Initialize
author: windows-sdk-content
description: Initializes the bitmap flip rotator with the provided parameters.
old-location: wic\_wic_codec_iwicbitmapfliprotator_initialize.htm
old-project: wic
ms.assetid: 8c70d25d-b591-4ef4-91b5-b8350da99df1
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWICBitmapFlipRotator interface [Windows Imaging Component],Initialize method, IWICBitmapFlipRotator.Initialize, IWICBitmapFlipRotator::Initialize, Initialize, Initialize method [Windows Imaging Component], Initialize method [Windows Imaging Component],IWICBitmapFlipRotator interface, _wic_codec_iwicbitmapfliprotator_initialize, wic._wic_codec_iwicbitmapfliprotator_initialize, wincodec/IWICBitmapFlipRotator::Initialize
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICBitmapFlipRotator.Initialize
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapFlipRotator::Initialize


## -description


Initializes the bitmap flip rotator with the provided parameters.


## -parameters




### -param pISource [in]

Type: <b><a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a>*</b>

The input bitmap source.


### -param options [in]

Type: <b><a href="https://msdn.microsoft.com/e123bb4d-bc75-4f3f-98f1-bea9b008498b">WICBitmapTransformOptions</a></b>

The <a href="https://msdn.microsoft.com/e123bb4d-bc75-4f3f-98f1-bea9b008498b">WICBitmapTransformOptions</a> to flip or rotate the image.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



