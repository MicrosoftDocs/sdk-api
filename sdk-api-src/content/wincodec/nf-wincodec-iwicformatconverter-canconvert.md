---
UID: NF:wincodec.IWICFormatConverter.CanConvert
title: IWICFormatConverter::CanConvert (wincodec.h)
description: Determines if the source pixel format can be converted to the destination pixel format.
helpviewer_keywords: ["CanConvert","CanConvert method [Windows Imaging Component]","CanConvert method [Windows Imaging Component]","IWICFormatConverter interface","IWICFormatConverter interface [Windows Imaging Component]","CanConvert method","IWICFormatConverter.CanConvert","IWICFormatConverter::CanConvert","_wic_codec_iwicformatconverter_canconvert","wic._wic_codec_iwicformatconverter_canconvert","wincodec/IWICFormatConverter::CanConvert"]
old-location: wic\_wic_codec_iwicformatconverter_canconvert.htm
tech.root: wic
ms.assetid: bf813eaf-0899-4df2-bcc2-ba2db1e9af2f
ms.date: 12/05/2018
ms.keywords: CanConvert, CanConvert method [Windows Imaging Component], CanConvert method [Windows Imaging Component],IWICFormatConverter interface, IWICFormatConverter interface [Windows Imaging Component],CanConvert method, IWICFormatConverter.CanConvert, IWICFormatConverter::CanConvert, _wic_codec_iwicformatconverter_canconvert, wic._wic_codec_iwicformatconverter_canconvert, wincodec/IWICFormatConverter::CanConvert
f1_keywords:
- wincodec/IWICFormatConverter.CanConvert
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter">IWICFormatConverter</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-codec-native-pixel-formats">Native Pixel Formats</a>
 

 

