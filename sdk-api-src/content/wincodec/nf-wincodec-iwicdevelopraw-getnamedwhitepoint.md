---
UID: NF:wincodec.IWICDevelopRaw.GetNamedWhitePoint
title: IWICDevelopRaw::GetNamedWhitePoint
author: windows-sdk-content
description: Gets the named white point of the raw image.
old-location: wic\_wic_codec_iwicdevelopraw_getnamedwhitepoint.htm
old-project: wic
ms.assetid: 2fa5f0c8-fee2-4338-992a-5c927883a731
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: GetNamedWhitePoint, GetNamedWhitePoint method [Windows Imaging Component], GetNamedWhitePoint method [Windows Imaging Component],IWICDevelopRaw interface, IWICDevelopRaw interface [Windows Imaging Component],GetNamedWhitePoint method, IWICDevelopRaw.GetNamedWhitePoint, IWICDevelopRaw::GetNamedWhitePoint, _wic_codec_iwicdevelopraw_getnamedwhitepoint, wic._wic_codec_iwicdevelopraw_getnamedwhitepoint, wincodec/IWICDevelopRaw::GetNamedWhitePoint
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
 - IWICDevelopRaw.GetNamedWhitePoint
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICDevelopRaw::GetNamedWhitePoint


## -description


Gets the named white point of the raw image.


## -parameters




### -param pWhitePoint [out]

Type: <b><a href="https://msdn.microsoft.com/e256a6d6-a035-47c3-a82c-d9aec284de17">WICNamedWhitePoint</a>*</b>

A pointer that receives the bitwise combination of the enumeration values.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the named white points are not supported by the raw image or the raw file contains named white points that are not supported by this API, the codec implementer should still mark this capability as supported.

If the named white points are not supported by the raw image, a best effort should be made to adjust the image to the named white point even when it isn't a pre-defined white point of the raw file.

If the raw file containes named white points not supported by this API, the codec implementer should support the named white points in <a href="https://msdn.microsoft.com/e256a6d6-a035-47c3-a82c-d9aec284de17">WICNamedWhitePoint</a>.



