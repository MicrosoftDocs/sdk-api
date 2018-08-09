---
UID: NF:wincodec.IWICDevelopRaw.GetTint
title: IWICDevelopRaw::GetTint
author: windows-sdk-content
description: Gets the tint value of the raw image.
old-location: wic\_wic_codec_iwicdevelopraw_gettint.htm
old-project: wic
ms.assetid: 12b7ecbe-efa9-47f4-b3b5-5ae1e1a66c3b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetTint, GetTint method [Windows Imaging Component], GetTint method [Windows Imaging Component],IWICDevelopRaw interface, IWICDevelopRaw interface [Windows Imaging Component],GetTint method, IWICDevelopRaw.GetTint, IWICDevelopRaw::GetTint, _wic_codec_iwicdevelopraw_gettint, wic._wic_codec_iwicdevelopraw_gettint, wincodec/IWICDevelopRaw::GetTint
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
 - IWICDevelopRaw.GetTint
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICDevelopRaw::GetTint


## -description


Gets the tint value of the raw image.


## -parameters




### -param pTint [out]

Type: <b>double*</b>

A pointer that receives the tint value of the raw image. The default value is the "as-shot" setting if it exists or 0.0. The value range for sharpness is -1.0 through +1.0. The -1.0 lower limit represents a full green bias to the image, while the 1.0 upper limit represents a full magenta bias.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



