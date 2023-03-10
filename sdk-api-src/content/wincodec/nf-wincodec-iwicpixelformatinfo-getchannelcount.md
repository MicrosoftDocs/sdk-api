---
UID: NF:wincodec.IWICPixelFormatInfo.GetChannelCount
title: IWICPixelFormatInfo::GetChannelCount (wincodec.h)
description: Gets the number of channels the pixel format contains.
helpviewer_keywords: ["GetChannelCount","GetChannelCount method [Windows Imaging Component]","GetChannelCount method [Windows Imaging Component]","IWICPixelFormatInfo interface","IWICPixelFormatInfo interface [Windows Imaging Component]","GetChannelCount method","IWICPixelFormatInfo.GetChannelCount","IWICPixelFormatInfo::GetChannelCount","_wic_codec_iwicpixelformatinfo_getchannelcount","wic._wic_codec_iwicpixelformatinfo_getchannelcount","wincodec/IWICPixelFormatInfo::GetChannelCount"]
old-location: wic\_wic_codec_iwicpixelformatinfo_getchannelcount.htm
tech.root: wic
ms.assetid: 884262b8-dddf-4b8b-87aa-52d9e7952c91
ms.date: 12/05/2018
ms.keywords: GetChannelCount, GetChannelCount method [Windows Imaging Component], GetChannelCount method [Windows Imaging Component],IWICPixelFormatInfo interface, IWICPixelFormatInfo interface [Windows Imaging Component],GetChannelCount method, IWICPixelFormatInfo.GetChannelCount, IWICPixelFormatInfo::GetChannelCount, _wic_codec_iwicpixelformatinfo_getchannelcount, wic._wic_codec_iwicpixelformatinfo_getchannelcount, wincodec/IWICPixelFormatInfo::GetChannelCount
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICPixelFormatInfo::GetChannelCount
 - wincodec/IWICPixelFormatInfo::GetChannelCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.lib
 - Windowscodecs.dll
api_name:
 - IWICPixelFormatInfo.GetChannelCount
---

# IWICPixelFormatInfo::GetChannelCount


## -description

Gets the number of channels the pixel format contains.

## -parameters

### -param puiChannelCount [out]

Type: <b>UINT*</b>

Pointer that receives the channel count.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

