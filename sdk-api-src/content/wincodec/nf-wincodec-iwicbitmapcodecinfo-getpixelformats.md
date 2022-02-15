---
UID: NF:wincodec.IWICBitmapCodecInfo.GetPixelFormats
title: IWICBitmapCodecInfo::GetPixelFormats (wincodec.h)
description: Retrieves the pixel formats the codec supports.
helpviewer_keywords: ["GetPixelFormats","GetPixelFormats method [Windows Imaging Component]","GetPixelFormats method [Windows Imaging Component]","IWICBitmapCodecInfo interface","IWICBitmapCodecInfo interface [Windows Imaging Component]","GetPixelFormats method","IWICBitmapCodecInfo.GetPixelFormats","IWICBitmapCodecInfo::GetPixelFormats","_wic_codec_iwicbitmapcodecinfo_getpixelformats","wic._wic_codec_iwicbitmapcodecinfo_getpixelformats","wincodec/IWICBitmapCodecInfo::GetPixelFormats"]
old-location: wic\_wic_codec_iwicbitmapcodecinfo_getpixelformats.htm
tech.root: wic
ms.assetid: 2da56e46-bbbd-42d4-ba49-9dee01f6bba0
ms.date: 12/05/2018
ms.keywords: GetPixelFormats, GetPixelFormats method [Windows Imaging Component], GetPixelFormats method [Windows Imaging Component],IWICBitmapCodecInfo interface, IWICBitmapCodecInfo interface [Windows Imaging Component],GetPixelFormats method, IWICBitmapCodecInfo.GetPixelFormats, IWICBitmapCodecInfo::GetPixelFormats, _wic_codec_iwicbitmapcodecinfo_getpixelformats, wic._wic_codec_iwicbitmapcodecinfo_getpixelformats, wincodec/IWICBitmapCodecInfo::GetPixelFormats
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICBitmapCodecInfo::GetPixelFormats
 - wincodec/IWICBitmapCodecInfo::GetPixelFormats
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICBitmapCodecInfo.GetPixelFormats
---

# IWICBitmapCodecInfo::GetPixelFormats


## -description

Retrieves the pixel formats the codec supports.

## -parameters

### -param cFormats [in]

Type: <b>UINT</b>

The size of the <i>pguidPixelFormats</i> array. Use <code>0</code> on first call to determine the needed array size.

### -param pguidPixelFormats [in, out]

Type: <b>GUID*</b>

Receives the supported pixel formats. Use <code>NULL</code> on first call to determine needed array size.

### -param pcActual [out]

Type: <b>UINT*</b>

The array size needed to retrieve all supported pixel formats.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The usage pattern for this method is a two call process.
            The first call retrieves the array size needed to retrieve all the supported pixel formats by calling it with <i>cFormats</i> set to <code>0</code> and <i>pguidPixelFormats</i> set to <code>NULL</code>.
            This call sets <i>pcActual</i> to the array size needed.
            Once the needed array size is determined, a second <b>GetPixelFormats</b> call with <i>pguidPixelFormats</i> set to an array of the appropriate size will retrieve the pixel formats.

