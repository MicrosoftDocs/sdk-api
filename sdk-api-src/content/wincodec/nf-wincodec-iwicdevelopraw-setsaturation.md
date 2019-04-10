---
UID: NF:wincodec.IWICDevelopRaw.SetSaturation
title: IWICDevelopRaw::SetSaturation (wincodec.h)
author: windows-sdk-content
description: Sets the saturation value of the raw image.
old-location: wic\_wic_codec_iwicdevelopraw_setsaturation.htm
tech.root: wic
ms.assetid: 93e9eb1c-8428-4c4d-913a-d6162430e509
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICDevelopRaw interface [Windows Imaging Component],SetSaturation method, IWICDevelopRaw.SetSaturation, IWICDevelopRaw::SetSaturation, SetSaturation, SetSaturation method [Windows Imaging Component], SetSaturation method [Windows Imaging Component],IWICDevelopRaw interface, _wic_codec_iwicdevelopraw_setsaturation, wic._wic_codec_iwicdevelopraw_setsaturation, wincodec/IWICDevelopRaw::SetSaturation
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
 - IWICDevelopRaw.SetSaturation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICDevelopRaw::SetSaturation


## -description


Sets the saturation value of the raw image.


## -parameters




### -param Saturation [in]

Type: <b>double</b>

The saturation value of the raw image. The value range for saturation is 0.0 through 1.0. A value of 0.0 represents an image with a fully de-saturated image, while a value of 1.0 represents the highest amount of saturation that can be applied.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The codec implementer must determine what the upper range value represents and must determine how to map the value to their image processing routines.



