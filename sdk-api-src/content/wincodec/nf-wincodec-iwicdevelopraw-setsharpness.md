---
UID: NF:wincodec.IWICDevelopRaw.SetSharpness
title: IWICDevelopRaw::SetSharpness
author: windows-sdk-content
description: Sets the sharpness value of the raw image.
old-location: wic\_wic_codec_iwicdevelopraw_setsharpness.htm
old-project: wic
ms.assetid: 0c989362-0c76-4028-ac27-c49e3ec1c6fd
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWICDevelopRaw interface [Windows Imaging Component],SetSharpness method, IWICDevelopRaw.SetSharpness, IWICDevelopRaw::SetSharpness, SetSharpness, SetSharpness method [Windows Imaging Component], SetSharpness method [Windows Imaging Component],IWICDevelopRaw interface, _wic_codec_iwicdevelopraw_setsharpness, wic._wic_codec_iwicdevelopraw_setsharpness, wincodec/IWICDevelopRaw::SetSharpness
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
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
 - IWICDevelopRaw.SetSharpness
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICDevelopRaw::SetSharpness


## -description


Sets the sharpness value of the raw image.


## -parameters




### -param Sharpness [in]

Type: <b>double</b>

The sharpness value of the raw image. The default value is the "as-shot" setting. The value range for sharpness is 0.0 through 1.0. The 0.0 lower limit represents no sharpening applied to the image, while the 1.0 upper limit represents the highest amount of sharpness that can be applied.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The codec implementer must determine what the upper range value represents and must determine how to map the value to their image processing routines.



