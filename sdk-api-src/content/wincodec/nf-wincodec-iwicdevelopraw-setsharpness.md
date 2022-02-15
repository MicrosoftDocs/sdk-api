---
UID: NF:wincodec.IWICDevelopRaw.SetSharpness
title: IWICDevelopRaw::SetSharpness (wincodec.h)
description: Sets the sharpness value of the raw image.
helpviewer_keywords: ["IWICDevelopRaw interface [Windows Imaging Component]","SetSharpness method","IWICDevelopRaw.SetSharpness","IWICDevelopRaw::SetSharpness","SetSharpness","SetSharpness method [Windows Imaging Component]","SetSharpness method [Windows Imaging Component]","IWICDevelopRaw interface","_wic_codec_iwicdevelopraw_setsharpness","wic._wic_codec_iwicdevelopraw_setsharpness","wincodec/IWICDevelopRaw::SetSharpness"]
old-location: wic\_wic_codec_iwicdevelopraw_setsharpness.htm
tech.root: wic
ms.assetid: 0c989362-0c76-4028-ac27-c49e3ec1c6fd
ms.date: 12/05/2018
ms.keywords: IWICDevelopRaw interface [Windows Imaging Component],SetSharpness method, IWICDevelopRaw.SetSharpness, IWICDevelopRaw::SetSharpness, SetSharpness, SetSharpness method [Windows Imaging Component], SetSharpness method [Windows Imaging Component],IWICDevelopRaw interface, _wic_codec_iwicdevelopraw_setsharpness, wic._wic_codec_iwicdevelopraw_setsharpness, wincodec/IWICDevelopRaw::SetSharpness
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
 - IWICDevelopRaw::SetSharpness
 - wincodec/IWICDevelopRaw::SetSharpness
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
 - IWICDevelopRaw.SetSharpness
---

# IWICDevelopRaw::SetSharpness


## -description

Sets the sharpness value of the raw image.

## -parameters

### -param Sharpness [in]

Type: <b>double</b>

The sharpness value of the raw image. The default value is the "as-shot" setting. The value range for sharpness is 0.0 through 1.0. The 0.0 lower limit represents no sharpening applied to the image, while the 1.0 upper limit represents the highest amount of sharpness that can be applied.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The codec implementer must determine what the upper range value represents and must determine how to map the value to their image processing routines.

