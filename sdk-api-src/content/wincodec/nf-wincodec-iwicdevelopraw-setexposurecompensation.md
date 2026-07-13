---
UID: NF:wincodec.IWICDevelopRaw.SetExposureCompensation
title: IWICDevelopRaw::SetExposureCompensation (wincodec.h)
description: Sets the exposure compensation stop value.
helpviewer_keywords: ["IWICDevelopRaw interface [Windows Imaging Component]","SetExposureCompensation method","IWICDevelopRaw.SetExposureCompensation","IWICDevelopRaw::SetExposureCompensation","SetExposureCompensation","SetExposureCompensation method [Windows Imaging Component]","SetExposureCompensation method [Windows Imaging Component]","IWICDevelopRaw interface","_wic_codec_iwicdevelopraw_setexposurecompensation","wic._wic_codec_iwicdevelopraw_setexposurecompensation","wincodec/IWICDevelopRaw::SetExposureCompensation"]
old-location: wic\_wic_codec_iwicdevelopraw_setexposurecompensation.htm
tech.root: wic
ms.assetid: 57ee5b96-2e49-415c-b1a8-41436a761b23
ms.date: 12/05/2018
ms.keywords: IWICDevelopRaw interface [Windows Imaging Component],SetExposureCompensation method, IWICDevelopRaw.SetExposureCompensation, IWICDevelopRaw::SetExposureCompensation, SetExposureCompensation, SetExposureCompensation method [Windows Imaging Component], SetExposureCompensation method [Windows Imaging Component],IWICDevelopRaw interface, _wic_codec_iwicdevelopraw_setexposurecompensation, wic._wic_codec_iwicdevelopraw_setexposurecompensation, wincodec/IWICDevelopRaw::SetExposureCompensation
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
 - IWICDevelopRaw::SetExposureCompensation
 - wincodec/IWICDevelopRaw::SetExposureCompensation
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
 - IWICDevelopRaw.SetExposureCompensation
---

# IWICDevelopRaw::SetExposureCompensation


## -description

Sets the exposure compensation stop value.

## -parameters

### -param ev [in]

Type: <b>double</b>

The exposure compensation value. The value range for exposure compensation is -5.0 through +5.0, which equates to 10 full stops.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

It is recommended that a codec report that this method is supported even if the results at the outer range limits are not of perfect quality.

