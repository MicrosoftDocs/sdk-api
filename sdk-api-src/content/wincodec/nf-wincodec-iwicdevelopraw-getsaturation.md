---
UID: NF:wincodec.IWICDevelopRaw.GetSaturation
title: IWICDevelopRaw::GetSaturation (wincodec.h)
description: Gets the saturation value of the raw image.
helpviewer_keywords: ["GetSaturation","GetSaturation method [Windows Imaging Component]","GetSaturation method [Windows Imaging Component]","IWICDevelopRaw interface","IWICDevelopRaw interface [Windows Imaging Component]","GetSaturation method","IWICDevelopRaw.GetSaturation","IWICDevelopRaw::GetSaturation","_wic_codec_iwicdevelopraw_getsaturation","wic._wic_codec_iwicdevelopraw_getsaturation","wincodec/IWICDevelopRaw::GetSaturation"]
old-location: wic\_wic_codec_iwicdevelopraw_getsaturation.htm
tech.root: wic
ms.assetid: 621868d6-3444-48f9-a069-f52ebacd7bbb
ms.date: 12/05/2018
ms.keywords: GetSaturation, GetSaturation method [Windows Imaging Component], GetSaturation method [Windows Imaging Component],IWICDevelopRaw interface, IWICDevelopRaw interface [Windows Imaging Component],GetSaturation method, IWICDevelopRaw.GetSaturation, IWICDevelopRaw::GetSaturation, _wic_codec_iwicdevelopraw_getsaturation, wic._wic_codec_iwicdevelopraw_getsaturation, wincodec/IWICDevelopRaw::GetSaturation
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
 - IWICDevelopRaw::GetSaturation
 - wincodec/IWICDevelopRaw::GetSaturation
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
 - IWICDevelopRaw.GetSaturation
---

# IWICDevelopRaw::GetSaturation


## -description

Gets the saturation value of the raw image.

## -parameters

### -param pSaturation [out]

Type: <b>double*</b>

A pointer that receives the saturation value of the raw image. The default value is the "as-shot" setting. The value range for saturation is 0.0 through 1.0. A value of 0.0 represents an image with a fully de-saturated image, while a value of 1.0 represents the highest amount of saturation that can be applied.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

