---
UID: NF:wincodec.IWICPixelFormatInfo2.SupportsTransparency
title: IWICPixelFormatInfo2::SupportsTransparency
author: windows-sdk-content
description: Returns whether the format supports transparent pixels.
old-location: wic\_wic_codec_iwicpixelformatinfo2_supportstransparency.htm
tech.root: wic
ms.assetid: 953cc1f0-28ee-4717-ac95-73ab39126b27
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWICPixelFormatInfo2 interface [Windows Imaging Component],SupportsTransparency method, IWICPixelFormatInfo2.SupportsTransparency, IWICPixelFormatInfo2::SupportsTransparency, SupportsTransparency, SupportsTransparency method [Windows Imaging Component], SupportsTransparency method [Windows Imaging Component],IWICPixelFormatInfo2 interface, _wic_codec_iwicpixelformatinfo2_supportstransparency, wic._wic_codec_iwicpixelformatinfo2_supportstransparency, wincodec/IWICPixelFormatInfo2::SupportsTransparency
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
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
 - IWICPixelFormatInfo2.SupportsTransparency
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICPixelFormatInfo2::SupportsTransparency


## -description


Returns whether the format supports transparent pixels.


## -parameters




### -param pfSupportsTransparency [out]

Type: <b>BOOL*</b>

Returns <b>TRUE</b> if the pixel format supports transparency; otherwise, <b>FALSE</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An indexed pixel format will not return <b>TRUE</b> even though it may have some transparency support.





## -see-also




<a href="https://msdn.microsoft.com/6c36fb08-f0c7-4654-bd8e-ef8ef737bc41">IWICPixelFormatInfo2</a>
 

 

