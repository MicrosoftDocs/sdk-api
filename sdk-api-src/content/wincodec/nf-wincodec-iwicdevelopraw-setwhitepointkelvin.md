---
UID: NF:wincodec.IWICDevelopRaw.SetWhitePointKelvin
title: IWICDevelopRaw::SetWhitePointKelvin
author: windows-sdk-content
description: Sets the white point Kelvin value.
old-location: wic\_wic_codec_iwicdevelopraw_setwhitepointkelvin.htm
old-project: wic
ms.assetid: 3a5235ed-b0c8-4090-9380-892e3e994d10
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWICDevelopRaw interface [Windows Imaging Component],SetWhitePointKelvin method, IWICDevelopRaw.SetWhitePointKelvin, IWICDevelopRaw::SetWhitePointKelvin, SetWhitePointKelvin, SetWhitePointKelvin method [Windows Imaging Component], SetWhitePointKelvin method [Windows Imaging Component],IWICDevelopRaw interface, _wic_codec_iwicdevelopraw_setwhitepointkelvin, wic._wic_codec_iwicdevelopraw_setwhitepointkelvin, wincodec/IWICDevelopRaw::SetWhitePointKelvin
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
-	IWICDevelopRaw.SetWhitePointKelvin
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICDevelopRaw::SetWhitePointKelvin


## -description


Sets the white point Kelvin value.


## -parameters




### -param WhitePointKelvin [in]

Type: <b>UINT</b>

The white point Kelvin value. Acceptable Kelvin values are 1,500 through 30,000.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Codec implementers should faithfully adjust the color temperature within the range supported natively by the raw image. For values outside the native support range, the codec implementer should provide a best effort representation of the image at that color temperature.

Codec implementers should return <b>WINCODEC_ERR_VALUEOUTOFRANGE</b> if the value is out of defined acceptable range.

Codec implementers must ensure proper interoperability with other white point setting methods such as <a href="https://msdn.microsoft.com/7059959f-dcd6-46a6-a95c-1dd9610f865c">SetWhitePointRGB</a>. For example, if the caller sets the white point via <a href="https://msdn.microsoft.com/eb83233d-7967-4160-bebf-2b06378f77ab">SetNamedWhitePoint</a> then the codec implementer may want to disable reading back the correspoinding Kelvin temperature. In specific cases where the codec implementer wants to deny a given action because of previous calls, <b>WINCODEC_ERR_WRONGSTATE</b> should be returned.



