---
UID: NF:wincodec.IWICDevelopRaw.GetExposureCompensation
title: IWICDevelopRaw::GetExposureCompensation
author: windows-sdk-content
description: Gets the exposure compensation stop value of the raw image.
old-location: wic\_wic_codec_iwicdevelopraw_getexposurecompensation.htm
tech.root: wic
ms.assetid: cdd71702-4696-4533-bd6f-ba9324b6b05b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetExposureCompensation, GetExposureCompensation method [Windows Imaging Component], GetExposureCompensation method [Windows Imaging Component],IWICDevelopRaw interface, IWICDevelopRaw interface [Windows Imaging Component],GetExposureCompensation method, IWICDevelopRaw.GetExposureCompensation, IWICDevelopRaw::GetExposureCompensation, _wic_codec_iwicdevelopraw_getexposurecompensation, wic._wic_codec_iwicdevelopraw_getexposurecompensation, wincodec/IWICDevelopRaw::GetExposureCompensation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICDevelopRaw.GetExposureCompensation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wincodec.h
: 
- IWICDevelopRaw.GetExposureCompensation
: 
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



