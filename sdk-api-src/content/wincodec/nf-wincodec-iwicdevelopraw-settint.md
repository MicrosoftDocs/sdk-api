---
UID: NF:wincodec.IWICDevelopRaw.SetTint
title: IWICDevelopRaw::SetTint (wincodec.h)
description: Sets the tint value of the raw image.
helpviewer_keywords: ["IWICDevelopRaw interface [Windows Imaging Component]","SetTint method","IWICDevelopRaw.SetTint","IWICDevelopRaw::SetTint","SetTint","SetTint method [Windows Imaging Component]","SetTint method [Windows Imaging Component]","IWICDevelopRaw interface","_wic_codec_iwicdevelopraw_settint","wic._wic_codec_iwicdevelopraw_settint","wincodec/IWICDevelopRaw::SetTint"]
old-location: wic\_wic_codec_iwicdevelopraw_settint.htm
tech.root: wic
ms.assetid: a5c6a15b-19d3-4b6f-a00e-842ec8614ce5
ms.date: 12/05/2018
ms.keywords: IWICDevelopRaw interface [Windows Imaging Component],SetTint method, IWICDevelopRaw.SetTint, IWICDevelopRaw::SetTint, SetTint, SetTint method [Windows Imaging Component], SetTint method [Windows Imaging Component],IWICDevelopRaw interface, _wic_codec_iwicdevelopraw_settint, wic._wic_codec_iwicdevelopraw_settint, wincodec/IWICDevelopRaw::SetTint
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
 - IWICDevelopRaw::SetTint
 - wincodec/IWICDevelopRaw::SetTint
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
 - IWICDevelopRaw.SetTint
---

# IWICDevelopRaw::SetTint


## -description

Sets the tint value of the raw image.

## -parameters

### -param Tint [in]

Type: <b>double</b>

The tint value of the raw image. The default value is the "as-shot" setting if it exists or 0.0. The value range for sharpness is -1.0 through +1.0. The -1.0 lower limit represents a full green bias to the image, while the 1.0 upper limit represents a full magenta bias.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The codec implementer must determine what the outer range values represent and must determine how to map the values to their image processing routines.

