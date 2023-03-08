---
UID: NF:wincodec.IWICDevelopRaw.GetWhitePointKelvin
title: IWICDevelopRaw::GetWhitePointKelvin (wincodec.h)
description: Gets the white point Kelvin temperature of the raw image.
helpviewer_keywords: ["GetWhitePointKelvin","GetWhitePointKelvin method [Windows Imaging Component]","GetWhitePointKelvin method [Windows Imaging Component]","IWICDevelopRaw interface","IWICDevelopRaw interface [Windows Imaging Component]","GetWhitePointKelvin method","IWICDevelopRaw.GetWhitePointKelvin","IWICDevelopRaw::GetWhitePointKelvin","_wic_codec_iwicdevelopraw_getwhitepointkelvin","wic._wic_codec_iwicdevelopraw_getwhitepointkelvin","wincodec/IWICDevelopRaw::GetWhitePointKelvin"]
old-location: wic\_wic_codec_iwicdevelopraw_getwhitepointkelvin.htm
tech.root: wic
ms.assetid: 9f649de0-6b53-4c67-b75d-73a44cc07c56
ms.date: 12/05/2018
ms.keywords: GetWhitePointKelvin, GetWhitePointKelvin method [Windows Imaging Component], GetWhitePointKelvin method [Windows Imaging Component],IWICDevelopRaw interface, IWICDevelopRaw interface [Windows Imaging Component],GetWhitePointKelvin method, IWICDevelopRaw.GetWhitePointKelvin, IWICDevelopRaw::GetWhitePointKelvin, _wic_codec_iwicdevelopraw_getwhitepointkelvin, wic._wic_codec_iwicdevelopraw_getwhitepointkelvin, wincodec/IWICDevelopRaw::GetWhitePointKelvin
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
 - IWICDevelopRaw::GetWhitePointKelvin
 - wincodec/IWICDevelopRaw::GetWhitePointKelvin
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
 - IWICDevelopRaw.GetWhitePointKelvin
---

# IWICDevelopRaw::GetWhitePointKelvin


## -description

Gets the white point Kelvin temperature of the raw image.

## -parameters

### -param pWhitePointKelvin [out]

Type: <b>UINT*</b>

A pointer that receives the white point Kelvin temperature of the raw image. The default is the "as-shot" setting value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

