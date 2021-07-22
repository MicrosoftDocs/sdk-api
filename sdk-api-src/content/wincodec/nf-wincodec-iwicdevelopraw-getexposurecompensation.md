---
UID: NF:wincodec.IWICDevelopRaw.GetExposureCompensation
title: IWICDevelopRaw::GetExposureCompensation (wincodec.h)
description: Gets the exposure compensation stop value of the raw image.
helpviewer_keywords: ["GetExposureCompensation","GetExposureCompensation method [Windows Imaging Component]","GetExposureCompensation method [Windows Imaging Component]","IWICDevelopRaw interface","IWICDevelopRaw interface [Windows Imaging Component]","GetExposureCompensation method","IWICDevelopRaw.GetExposureCompensation","IWICDevelopRaw::GetExposureCompensation","_wic_codec_iwicdevelopraw_getexposurecompensation","wic._wic_codec_iwicdevelopraw_getexposurecompensation","wincodec/IWICDevelopRaw::GetExposureCompensation"]
old-location: wic\_wic_codec_iwicdevelopraw_getexposurecompensation.htm
tech.root: wic
ms.assetid: cdd71702-4696-4533-bd6f-ba9324b6b05b
ms.date: 12/05/2018
ms.keywords: GetExposureCompensation, GetExposureCompensation method [Windows Imaging Component], GetExposureCompensation method [Windows Imaging Component],IWICDevelopRaw interface, IWICDevelopRaw interface [Windows Imaging Component],GetExposureCompensation method, IWICDevelopRaw.GetExposureCompensation, IWICDevelopRaw::GetExposureCompensation, _wic_codec_iwicdevelopraw_getexposurecompensation, wic._wic_codec_iwicdevelopraw_getexposurecompensation, wincodec/IWICDevelopRaw::GetExposureCompensation
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
 - IWICDevelopRaw::GetExposureCompensation
 - wincodec/IWICDevelopRaw::GetExposureCompensation
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
 - IWICDevelopRaw.GetExposureCompensation
---

# IWICDevelopRaw::GetExposureCompensation


## -description

Gets the exposure compensation stop value of the raw image.

## -parameters

### -param pEV [out]

Type: <b>double*</b>

A pointer that receives the exposure compensation stop value. The default is the "as-shot" setting.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

