---
UID: NF:wincodec.IWICDevelopRaw.SetContrast
title: IWICDevelopRaw::SetContrast (wincodec.h)
author: windows-sdk-content
description: Sets the contrast value of the raw image.
old-location: wic\_wic_codec_iwicdevelopraw_setcontrast.htm
tech.root: wic
ms.assetid: 5013d351-e96d-44c7-88d7-65a55e474b01
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWICDevelopRaw interface [Windows Imaging Component],SetContrast method, IWICDevelopRaw.SetContrast, IWICDevelopRaw::SetContrast, SetContrast, SetContrast method [Windows Imaging Component], SetContrast method [Windows Imaging Component],IWICDevelopRaw interface, _wic_codec_iwicdevelopraw_setcontrast, wic._wic_codec_iwicdevelopraw_setcontrast, wincodec/IWICDevelopRaw::SetContrast
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
 - IWICDevelopRaw.SetContrast
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The codec implementer must determine what the upper range value represents and must determine how to map the value to their image processing routines.



