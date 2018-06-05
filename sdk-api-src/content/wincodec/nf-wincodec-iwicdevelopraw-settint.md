---
UID: NF:wincodec.IWICDevelopRaw.SetTint
title: IWICDevelopRaw::SetTint
author: windows-sdk-content
description: Sets the tint value of the raw image.
old-location: wic\_wic_codec_iwicdevelopraw_settint.htm
old-project: wic
ms.assetid: a5c6a15b-19d3-4b6f-a00e-842ec8614ce5
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWICDevelopRaw interface [Windows Imaging Component],SetTint method, IWICDevelopRaw.SetTint, IWICDevelopRaw::SetTint, SetTint, SetTint method [Windows Imaging Component], SetTint method [Windows Imaging Component],IWICDevelopRaw interface, _wic_codec_iwicdevelopraw_settint, wic._wic_codec_iwicdevelopraw_settint, wincodec/IWICDevelopRaw::SetTint
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICDevelopRaw.SetTint
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICDevelopRaw::SetTint


## -description


Sets the tint value of the raw image.


## -parameters




### -param Tint [in]

Type: <b>double</b>

The tint value of the raw image. The default value is the "as-shot" setting if it exists or 0.0. The value range for sharpness is -1.0 through +1.0. The -1.0 lower limit represents a full green bias to the image, while the 1.0 upper limit represents a full magenta bias.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The codec implementer must determine what the outer range values represent and must determine how to map the values to their image processing routines.



