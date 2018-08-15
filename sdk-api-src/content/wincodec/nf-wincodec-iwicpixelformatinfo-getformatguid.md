---
UID: NF:wincodec.IWICPixelFormatInfo.GetFormatGUID
title: IWICPixelFormatInfo::GetFormatGUID
author: windows-sdk-content
description: Gets the pixel format GUID.
old-location: wic\_wic_codec_iwicpixelformatinfo_getformatguid.htm
old-project: wic
ms.assetid: 184ad8e5-51f2-47eb-b3c4-010626fa7c34
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetFormatGUID, GetFormatGUID method [Windows Imaging Component], GetFormatGUID method [Windows Imaging Component],IWICPixelFormatInfo interface, IWICPixelFormatInfo interface [Windows Imaging Component],GetFormatGUID method, IWICPixelFormatInfo.GetFormatGUID, IWICPixelFormatInfo::GetFormatGUID, _wic_codec_iwicpixelformatinfo_getformatguid, wic._wic_codec_iwicpixelformatinfo_getformatguid, wincodec/IWICPixelFormatInfo::GetFormatGUID
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.redist: 
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
 - Windowscodecs.lib
 - Windowscodecs.dll
api_name:
 - IWICPixelFormatInfo.GetFormatGUID
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICPixelFormatInfo::GetFormatGUID


## -description


Gets the pixel format GUID.


## -parameters




### -param pFormat [out]

Type: <b>GUID*</b>

Pointer that receives the pixel format GUID.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



