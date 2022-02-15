---
UID: NF:wincodec.IWICDevelopRaw.GetSharpness
title: IWICDevelopRaw::GetSharpness (wincodec.h)
description: Gets the sharpness value of the raw image.
helpviewer_keywords: ["GetSharpness","GetSharpness method [Windows Imaging Component]","GetSharpness method [Windows Imaging Component]","IWICDevelopRaw interface","IWICDevelopRaw interface [Windows Imaging Component]","GetSharpness method","IWICDevelopRaw.GetSharpness","IWICDevelopRaw::GetSharpness","_wic_codec_iwicdevelopraw_getsharpness","wic._wic_codec_iwicdevelopraw_getsharpness","wincodec/IWICDevelopRaw::GetSharpness"]
old-location: wic\_wic_codec_iwicdevelopraw_getsharpness.htm
tech.root: wic
ms.assetid: a3cb0749-5ec6-4c29-824f-ae44f554d494
ms.date: 12/05/2018
ms.keywords: GetSharpness, GetSharpness method [Windows Imaging Component], GetSharpness method [Windows Imaging Component],IWICDevelopRaw interface, IWICDevelopRaw interface [Windows Imaging Component],GetSharpness method, IWICDevelopRaw.GetSharpness, IWICDevelopRaw::GetSharpness, _wic_codec_iwicdevelopraw_getsharpness, wic._wic_codec_iwicdevelopraw_getsharpness, wincodec/IWICDevelopRaw::GetSharpness
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
 - IWICDevelopRaw::GetSharpness
 - wincodec/IWICDevelopRaw::GetSharpness
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
 - IWICDevelopRaw.GetSharpness
---

# IWICDevelopRaw::GetSharpness


## -description

Gets the sharpness value of the raw image.

## -parameters

### -param pSharpness [out]

Type: <b>double*</b>

A pointer that receives the sharpness value of the raw image. The default value is the "as-shot" setting. The value range for sharpness is 0.0 through 1.0. The 0.0 lower limit represents no sharpening applied to the image, while the 1.0 upper limit represents the highest amount of sharpness that can be applied.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

