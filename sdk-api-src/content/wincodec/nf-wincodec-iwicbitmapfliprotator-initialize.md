---
UID: NF:wincodec.IWICBitmapFlipRotator.Initialize
title: IWICBitmapFlipRotator::Initialize (wincodec.h)
description: Initializes the bitmap flip rotator with the provided parameters.
helpviewer_keywords: ["IWICBitmapFlipRotator interface [Windows Imaging Component]","Initialize method","IWICBitmapFlipRotator.Initialize","IWICBitmapFlipRotator::Initialize","Initialize","Initialize method [Windows Imaging Component]","Initialize method [Windows Imaging Component]","IWICBitmapFlipRotator interface","_wic_codec_iwicbitmapfliprotator_initialize","wic._wic_codec_iwicbitmapfliprotator_initialize","wincodec/IWICBitmapFlipRotator::Initialize"]
old-location: wic\_wic_codec_iwicbitmapfliprotator_initialize.htm
tech.root: wic
ms.assetid: 8c70d25d-b591-4ef4-91b5-b8350da99df1
ms.date: 12/05/2018
ms.keywords: IWICBitmapFlipRotator interface [Windows Imaging Component],Initialize method, IWICBitmapFlipRotator.Initialize, IWICBitmapFlipRotator::Initialize, Initialize, Initialize method [Windows Imaging Component], Initialize method [Windows Imaging Component],IWICBitmapFlipRotator interface, _wic_codec_iwicbitmapfliprotator_initialize, wic._wic_codec_iwicbitmapfliprotator_initialize, wincodec/IWICBitmapFlipRotator::Initialize
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
 - IWICBitmapFlipRotator::Initialize
 - wincodec/IWICBitmapFlipRotator::Initialize
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
 - IWICBitmapFlipRotator.Initialize
---

# IWICBitmapFlipRotator::Initialize


## -description

Initializes the bitmap flip rotator with the provided parameters.

## -parameters

### -param pISource [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>*</b>

The input bitmap source.

### -param options [in]

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmaptransformoptions">WICBitmapTransformOptions</a></b>

The <a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmaptransformoptions">WICBitmapTransformOptions</a> to flip or rotate the image.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.