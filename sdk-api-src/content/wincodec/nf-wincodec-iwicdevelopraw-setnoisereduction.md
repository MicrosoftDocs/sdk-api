---
UID: NF:wincodec.IWICDevelopRaw.SetNoiseReduction
title: IWICDevelopRaw::SetNoiseReduction (wincodec.h)
author: windows-sdk-content
description: Sets the noise reduction value of the raw image.
old-location: wic\_wic_codec_iwicdevelopraw_setnoisereduction.htm
tech.root: wic
ms.assetid: d0c78274-0a1f-4a98-a449-ae902795a71b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICDevelopRaw interface [Windows Imaging Component],SetNoiseReduction method, IWICDevelopRaw.SetNoiseReduction, IWICDevelopRaw::SetNoiseReduction, SetNoiseReduction, SetNoiseReduction method [Windows Imaging Component], SetNoiseReduction method [Windows Imaging Component],IWICDevelopRaw interface, _wic_codec_iwicdevelopraw_setnoisereduction, wic._wic_codec_iwicdevelopraw_setnoisereduction, wincodec/IWICDevelopRaw::SetNoiseReduction
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
 - IWICDevelopRaw.SetNoiseReduction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICDevelopRaw::SetNoiseReduction


## -description


Sets the noise reduction value of the raw image.


## -parameters




### -param NoiseReduction [in]

Type: <b>double</b>

The noise reduction value of the raw image.  The default value is the "as-shot" setting if it exists or 0.0. The value range for noise reduction is 0.0 through 1.0. The 0.0 lower limit represents no noise reduction applied to the image, while the 1.0 upper limit represents highest noise reduction amount that can be applied.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The codec implementer must determine what the upper range value represents and must determine how to map the value to their image processing routines.



