---
UID: NF:wincodec.IWICDevelopRaw.SetContrast
title: IWICDevelopRaw::SetContrast (wincodec.h)
description: Sets the contrast value of the raw image.
helpviewer_keywords: ["IWICDevelopRaw interface [Windows Imaging Component]","SetContrast method","IWICDevelopRaw.SetContrast","IWICDevelopRaw::SetContrast","SetContrast","SetContrast method [Windows Imaging Component]","SetContrast method [Windows Imaging Component]","IWICDevelopRaw interface","_wic_codec_iwicdevelopraw_setcontrast","wic._wic_codec_iwicdevelopraw_setcontrast","wincodec/IWICDevelopRaw::SetContrast"]
old-location: wic\_wic_codec_iwicdevelopraw_setcontrast.htm
tech.root: wic
ms.assetid: 5013d351-e96d-44c7-88d7-65a55e474b01
ms.date: 12/05/2018
ms.keywords: IWICDevelopRaw interface [Windows Imaging Component],SetContrast method, IWICDevelopRaw.SetContrast, IWICDevelopRaw::SetContrast, SetContrast, SetContrast method [Windows Imaging Component], SetContrast method [Windows Imaging Component],IWICDevelopRaw interface, _wic_codec_iwicdevelopraw_setcontrast, wic._wic_codec_iwicdevelopraw_setcontrast, wincodec/IWICDevelopRaw::SetContrast
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
 - IWICDevelopRaw::SetContrast
 - wincodec/IWICDevelopRaw::SetContrast
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
 - IWICDevelopRaw.SetContrast
---

# IWICDevelopRaw::SetContrast


## -description

Sets the contrast value of the raw image.

## -parameters

### -param Contrast [in]

Type: <b>double</b>

The contrast value of the raw image.  The default value is the "as-shot" setting. The value range for contrast is 0.0 through 1.0. The 0.0 lower limit represents no contrast applied to the image, while the 1.0 upper limit represents the highest amount of contrast that can be applied.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The codec implementer must determine what the upper range value represents and must determine how to map the value to their image processing routines.

