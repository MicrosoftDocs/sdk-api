---
UID: NF:wincodec.IWICPixelFormatInfo.GetChannelMask
title: IWICPixelFormatInfo::GetChannelMask (wincodec.h)
description: Gets the pixel format's channel mask.
helpviewer_keywords: ["GetChannelMask","GetChannelMask method [Windows Imaging Component]","GetChannelMask method [Windows Imaging Component]","IWICPixelFormatInfo interface","IWICPixelFormatInfo interface [Windows Imaging Component]","GetChannelMask method","IWICPixelFormatInfo.GetChannelMask","IWICPixelFormatInfo::GetChannelMask","_wic_codec_iwicpixelformatinfo_getchannelmask","wic._wic_codec_iwicpixelformatinfo_getchannelmask","wincodec/IWICPixelFormatInfo::GetChannelMask"]
old-location: wic\_wic_codec_iwicpixelformatinfo_getchannelmask.htm
tech.root: wic
ms.assetid: da812e26-b0cc-49eb-a273-73b9bb579ba3
ms.date: 12/05/2018
ms.keywords: GetChannelMask, GetChannelMask method [Windows Imaging Component], GetChannelMask method [Windows Imaging Component],IWICPixelFormatInfo interface, IWICPixelFormatInfo interface [Windows Imaging Component],GetChannelMask method, IWICPixelFormatInfo.GetChannelMask, IWICPixelFormatInfo::GetChannelMask, _wic_codec_iwicpixelformatinfo_getchannelmask, wic._wic_codec_iwicpixelformatinfo_getchannelmask, wincodec/IWICPixelFormatInfo::GetChannelMask
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
 - IWICPixelFormatInfo::GetChannelMask
 - wincodec/IWICPixelFormatInfo::GetChannelMask
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
 - IWICPixelFormatInfo.GetChannelMask
---

# IWICPixelFormatInfo::GetChannelMask


## -description

Gets the pixel format's channel mask.

## -parameters

### -param uiChannelIndex [in]

Type: <b>UINT</b>

The index to the channel mask to retrieve.

### -param cbMaskBuffer [in]

Type: <b>UINT</b>

The size of the <i>pbMaskBuffer</i> buffer.

### -param pbMaskBuffer [in, out]

Type: <b>BYTE*</b>

Pointer to the mask buffer.

### -param pcbActual [out]

Type: <b>UINT*</b>

The actual buffer size needed to obtain the channel mask.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If 0 and NULL are passed in for <i>cbMaskBuffer</i> and <i>pbMaskBuffer</i>, respectively, the required buffer size will be returned through <i>pcbActual</i>.

