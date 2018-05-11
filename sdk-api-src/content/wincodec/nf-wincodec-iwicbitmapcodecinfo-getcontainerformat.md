---
UID: NF:wincodec.IWICBitmapCodecInfo.GetContainerFormat
title: IWICBitmapCodecInfo::GetContainerFormat
author: windows-driver-content
description: Retrieves the container GUID associated with the codec.
old-location: wic\_wic_codec_iwicbitmapcodecinfo_getcontainerformat.htm
old-project: wic
ms.assetid: 164952ae-95ea-43b1-872c-088b2c1c65c8
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetContainerFormat, GetContainerFormat method [Windows Imaging Component], GetContainerFormat method [Windows Imaging Component],IWICBitmapCodecInfo interface, IWICBitmapCodecInfo interface [Windows Imaging Component],GetContainerFormat method, IWICBitmapCodecInfo.GetContainerFormat, IWICBitmapCodecInfo::GetContainerFormat, _wic_codec_iwicbitmapcodecinfo_getcontainerformat, wic._wic_codec_iwicbitmapcodecinfo_getcontainerformat, wincodec/IWICBitmapCodecInfo::GetContainerFormat
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICBitmapCodecInfo.GetContainerFormat
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapCodecInfo::GetContainerFormat


## -description


Retrieves the container GUID associated with the codec.


## -parameters




### -param pguidContainerFormat [out]

Type: <b>GUID*</b>

Receives the container GUID.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



