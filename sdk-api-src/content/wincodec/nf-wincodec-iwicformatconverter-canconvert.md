---
UID: NF:wincodec.IWICFormatConverter.CanConvert
title: IWICFormatConverter::CanConvert
author: windows-sdk-content
description: Determines if the source pixel format can be converted to the destination pixel format.
old-location: wic\_wic_codec_iwicformatconverter_canconvert.htm
tech.root: wic
ms.assetid: bf813eaf-0899-4df2-bcc2-ba2db1e9af2f
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CanConvert, CanConvert method [Windows Imaging Component], CanConvert method [Windows Imaging Component],IWICFormatConverter interface, IWICFormatConverter interface [Windows Imaging Component],CanConvert method, IWICFormatConverter.CanConvert, IWICFormatConverter::CanConvert, _wic_codec_iwicformatconverter_canconvert, wic._wic_codec_iwicformatconverter_canconvert, wincodec/IWICFormatConverter::CanConvert
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWICFormatConverter.CanConvert
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICFormatConverter::CanConvert


## -description


Determines if the source pixel format can be converted to the destination pixel format.


## -parameters




### -param srcPixelFormat [in]

Type: <b>REFWICPixelFormatGUID</b>

The source pixel format.


### -param dstPixelFormat [in]

Type: <b>REFWICPixelFormatGUID</b>

The destionation pixel format.


### -param pfCanConvert [out]

Type: <b>BOOL*</b>

A pointer that receives a value indicating whether the source pixel format can be converted to the destination pixel format.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d558aaa7-5962-424c-9e83-363fba09ad50">IWICFormatConverter</a>



<a href="https://msdn.microsoft.com/348b6d15-e339-4dce-99f3-4d639ee9bf7d">Native Pixel Formats</a>
 

 

