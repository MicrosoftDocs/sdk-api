---
UID: NF:wincodec.IWICDevelopRaw.GetNoiseReduction
title: IWICDevelopRaw::GetNoiseReduction (wincodec.h)
description: Gets the noise reduction value of the raw image.
helpviewer_keywords: ["GetNoiseReduction","GetNoiseReduction method [Windows Imaging Component]","GetNoiseReduction method [Windows Imaging Component]","IWICDevelopRaw interface","IWICDevelopRaw interface [Windows Imaging Component]","GetNoiseReduction method","IWICDevelopRaw.GetNoiseReduction","IWICDevelopRaw::GetNoiseReduction","_wic_codec_iwicdevelopraw_getnoisereduction","wic._wic_codec_iwicdevelopraw_getnoisereduction","wincodec/IWICDevelopRaw::GetNoiseReduction"]
old-location: wic\_wic_codec_iwicdevelopraw_getnoisereduction.htm
tech.root: wic
ms.assetid: 38dee560-16c1-4a91-8a8d-ed42dcdbb9ff
ms.date: 12/05/2018
ms.keywords: GetNoiseReduction, GetNoiseReduction method [Windows Imaging Component], GetNoiseReduction method [Windows Imaging Component],IWICDevelopRaw interface, IWICDevelopRaw interface [Windows Imaging Component],GetNoiseReduction method, IWICDevelopRaw.GetNoiseReduction, IWICDevelopRaw::GetNoiseReduction, _wic_codec_iwicdevelopraw_getnoisereduction, wic._wic_codec_iwicdevelopraw_getnoisereduction, wincodec/IWICDevelopRaw::GetNoiseReduction
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
 - IWICDevelopRaw::GetNoiseReduction
 - wincodec/IWICDevelopRaw::GetNoiseReduction
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
 - IWICDevelopRaw.GetNoiseReduction
---

# IWICDevelopRaw::GetNoiseReduction


## -description

Gets the noise reduction value of the raw image.

## -parameters

### -param pNoiseReduction [out]

Type: <b>double*</b>

A pointer that receives the noise reduction value of the raw image.  The default value is the "as-shot" setting if it exists or 0.0. The value range for noise reduction is 0.0 through 1.0. The 0.0 lower limit represents no noise reduction applied to the image, while the 1.0 upper limit represents full highest noise reduction amount that can be applied.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

