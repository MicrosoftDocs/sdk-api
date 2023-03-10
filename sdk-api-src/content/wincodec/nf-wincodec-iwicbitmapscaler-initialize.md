---
UID: NF:wincodec.IWICBitmapScaler.Initialize
title: IWICBitmapScaler::Initialize (wincodec.h)
description: Initializes the bitmap scaler with the provided parameters.
helpviewer_keywords: ["IWICBitmapScaler interface [Windows Imaging Component]","Initialize method","IWICBitmapScaler.Initialize","IWICBitmapScaler::Initialize","Initialize","Initialize method [Windows Imaging Component]","Initialize method [Windows Imaging Component]","IWICBitmapScaler interface","_wic_codec_iwicbitmapscaler_initialize","wic._wic_codec_iwicbitmapscaler_initialize","wincodec/IWICBitmapScaler::Initialize"]
old-location: wic\_wic_codec_iwicbitmapscaler_initialize.htm
tech.root: wic
ms.assetid: e783389e-4702-4774-a501-b86ec4bc6cbe
ms.date: 12/05/2018
ms.keywords: IWICBitmapScaler interface [Windows Imaging Component],Initialize method, IWICBitmapScaler.Initialize, IWICBitmapScaler::Initialize, Initialize, Initialize method [Windows Imaging Component], Initialize method [Windows Imaging Component],IWICBitmapScaler interface, _wic_codec_iwicbitmapscaler_initialize, wic._wic_codec_iwicbitmapscaler_initialize, wincodec/IWICBitmapScaler::Initialize
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
 - IWICBitmapScaler::Initialize
 - wincodec/IWICBitmapScaler::Initialize
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
 - IWICBitmapScaler.Initialize
---

# IWICBitmapScaler::Initialize


## -description

Initializes the bitmap scaler with the provided parameters.

## -parameters

### -param pISource [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>*</b>

The input bitmap source.

### -param uiWidth [in]

Type: <b>UINT</b>

The destination width.

### -param uiHeight [in]

Type: <b>UINT</b>

The destination height.

### -param mode [in]

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmapinterpolationmode">WICBitmapInterpolationMode</a></b>

The <a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmapinterpolationmode">WICBitmapInterpolationMode</a> to use when scaling.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapscaler">IWICBitmapScaler</a> can't be initialized multiple times. For example, when scaling every frame in a multi-frame image, a new <b>IWICBitmapScaler</b> must be created and initialized for each frame.


#### Examples

For an example using an <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapscaler">IWICBitmapScaler</a>, see the <a href="/windows/desktop/wic/-wic-bitmapsources-howto-scale">How to Scale a Bitmap Source</a> topic.

<div class="code"></div>