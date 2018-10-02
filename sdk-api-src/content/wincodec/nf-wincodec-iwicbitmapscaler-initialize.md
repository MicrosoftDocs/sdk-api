---
UID: NF:wincodec.IWICBitmapScaler.Initialize
title: IWICBitmapScaler::Initialize
author: windows-sdk-content
description: Initializes the bitmap scaler with the provided parameters.
old-location: wic\_wic_codec_iwicbitmapscaler_initialize.htm
tech.root: wic
ms.assetid: e783389e-4702-4774-a501-b86ec4bc6cbe
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWICBitmapScaler interface [Windows Imaging Component],Initialize method, IWICBitmapScaler.Initialize, IWICBitmapScaler::Initialize, Initialize, Initialize method [Windows Imaging Component], Initialize method [Windows Imaging Component],IWICBitmapScaler interface, _wic_codec_iwicbitmapscaler_initialize, wic._wic_codec_iwicbitmapscaler_initialize, wincodec/IWICBitmapScaler::Initialize
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWICBitmapScaler.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICBitmapScaler::Initialize


## -description


Initializes the bitmap scaler with the provided parameters.


## -parameters




### -param pISource [in]

Type: <b><a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a>*</b>

The input bitmap source.


### -param uiWidth [in]

Type: <b>UINT</b>

The destination width.


### -param uiHeight [in]

Type: <b>UINT</b>

The desination height.


### -param mode [in]

Type: <b><a href="https://msdn.microsoft.com/7c707ab7-7cd5-418f-921c-e9114da92f2a">WICBitmapInterpolationMode</a></b>

The <a href="https://msdn.microsoft.com/7c707ab7-7cd5-418f-921c-e9114da92f2a">WICBitmapInterpolationMode</a> to use when scaling.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




<a href="https://msdn.microsoft.com/cc14be9d-d750-40db-a95f-309b392cefe8">IWICBitmapScaler</a> can't be initialized multiple times. For example, when scaling every frame in a multi-frame image, a new <b>IWICBitmapScaler</b> must be created and initialized for each frame.


#### Examples

For an example using an <a href="https://msdn.microsoft.com/cc14be9d-d750-40db-a95f-309b392cefe8">IWICBitmapScaler</a>, see the <a href="https://msdn.microsoft.com/d2c65c9b-6f52-46f7-935d-0c582ca83867">How to Scale a Bitmap Source</a> topic.

<div class="code"></div>


