---
UID: NF:wincodec.IWICDevelopRaw.GetContrast
title: IWICDevelopRaw::GetContrast
author: windows-sdk-content
description: Gets the contrast value of the raw image.
old-location: wic\_wic_codec_iwicdevelopraw_getcontrast.htm
tech.root: wic
ms.assetid: 65454979-f282-42da-80b6-e50955634093
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetContrast, GetContrast method [Windows Imaging Component], GetContrast method [Windows Imaging Component],IWICDevelopRaw interface, IWICDevelopRaw interface [Windows Imaging Component],GetContrast method, IWICDevelopRaw.GetContrast, IWICDevelopRaw::GetContrast, _wic_codec_iwicdevelopraw_getcontrast, wic._wic_codec_iwicdevelopraw_getcontrast, wincodec/IWICDevelopRaw::GetContrast
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
 - IWICDevelopRaw.GetContrast
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICDevelopRaw::GetContrast


## -description


Gets the contrast value of the raw image.


## -parameters




### -param pContrast [out]

Type: <b>double*</b>

A pointer that receives the contrast value of the raw image. The default value is the "as-shot" setting. The value range for contrast is 0.0 through 1.0. The 0.0 lower limit represents no contrast applied to the image, while the 1.0 upper limit represents the highest amount of contrast that can be applied.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



