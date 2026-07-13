---
UID: NF:wincodec.IWICDevelopRaw.GetKelvinRangeInfo
title: IWICDevelopRaw::GetKelvinRangeInfo (wincodec.h)
description: Gets the information about the current Kelvin range of the raw image.
helpviewer_keywords: ["GetKelvinRangeInfo","GetKelvinRangeInfo method [Windows Imaging Component]","GetKelvinRangeInfo method [Windows Imaging Component]","IWICDevelopRaw interface","IWICDevelopRaw interface [Windows Imaging Component]","GetKelvinRangeInfo method","IWICDevelopRaw.GetKelvinRangeInfo","IWICDevelopRaw::GetKelvinRangeInfo","_wic_codec_iwicdevelopraw_getkelvinrangeinfo","wic._wic_codec_iwicdevelopraw_getkelvinrangeinfo","wincodec/IWICDevelopRaw::GetKelvinRangeInfo"]
old-location: wic\_wic_codec_iwicdevelopraw_getkelvinrangeinfo.htm
tech.root: wic
ms.assetid: c718c957-3523-4281-aa7e-761977a6b4c5
ms.date: 12/05/2018
ms.keywords: GetKelvinRangeInfo, GetKelvinRangeInfo method [Windows Imaging Component], GetKelvinRangeInfo method [Windows Imaging Component],IWICDevelopRaw interface, IWICDevelopRaw interface [Windows Imaging Component],GetKelvinRangeInfo method, IWICDevelopRaw.GetKelvinRangeInfo, IWICDevelopRaw::GetKelvinRangeInfo, _wic_codec_iwicdevelopraw_getkelvinrangeinfo, wic._wic_codec_iwicdevelopraw_getkelvinrangeinfo, wincodec/IWICDevelopRaw::GetKelvinRangeInfo
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
 - IWICDevelopRaw::GetKelvinRangeInfo
 - wincodec/IWICDevelopRaw::GetKelvinRangeInfo
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
 - IWICDevelopRaw.GetKelvinRangeInfo
---

# IWICDevelopRaw::GetKelvinRangeInfo


## -description

Gets the information about the current Kelvin range of the raw image.

## -parameters

### -param pMinKelvinTemp [out]

Type: <b>UINT*</b>

A pointer that receives the minimum Kelvin temperature.

### -param pMaxKelvinTemp [out]

Type: <b>UINT*</b>

A pointer that receives the maximum Kelvin temperature.

### -param pKelvinTempStepValue [out]

Type: <b>UINT*</b>

A pointer that receives the Kelvin step value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

