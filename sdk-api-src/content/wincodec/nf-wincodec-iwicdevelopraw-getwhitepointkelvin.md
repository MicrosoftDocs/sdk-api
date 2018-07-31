---
UID: NF:wincodec.IWICDevelopRaw.GetWhitePointKelvin
title: IWICDevelopRaw::GetWhitePointKelvin
author: windows-sdk-content
description: Gets the white point Kelvin temperature of the raw image.
old-location: wic\_wic_codec_iwicdevelopraw_getwhitepointkelvin.htm
old-project: wic
ms.assetid: 9f649de0-6b53-4c67-b75d-73a44cc07c56
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetWhitePointKelvin, GetWhitePointKelvin method [Windows Imaging Component], GetWhitePointKelvin method [Windows Imaging Component],IWICDevelopRaw interface, IWICDevelopRaw interface [Windows Imaging Component],GetWhitePointKelvin method, IWICDevelopRaw.GetWhitePointKelvin, IWICDevelopRaw::GetWhitePointKelvin, _wic_codec_iwicdevelopraw_getwhitepointkelvin, wic._wic_codec_iwicdevelopraw_getwhitepointkelvin, wincodec/IWICDevelopRaw::GetWhitePointKelvin
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WICTiffCompressionOption
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICDevelopRaw.GetWhitePointKelvin
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



