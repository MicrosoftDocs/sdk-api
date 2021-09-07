---
UID: NF:wincodec.IWICBitmapCodecInfo.GetFileExtensions
title: IWICBitmapCodecInfo::GetFileExtensions (wincodec.h)
description: Retrieves a comma delimited list of the file name extensions associated with the codec.
helpviewer_keywords: ["GetFileExtensions","GetFileExtensions method [Windows Imaging Component]","GetFileExtensions method [Windows Imaging Component]","IWICBitmapCodecInfo interface","IWICBitmapCodecInfo interface [Windows Imaging Component]","GetFileExtensions method","IWICBitmapCodecInfo.GetFileExtensions","IWICBitmapCodecInfo::GetFileExtensions","_wic_codec_iwicbitmapcodecinfo_getfileextensions","wic._wic_codec_iwicbitmapcodecinfo_getfileextensions","wincodec/IWICBitmapCodecInfo::GetFileExtensions"]
old-location: wic\_wic_codec_iwicbitmapcodecinfo_getfileextensions.htm
tech.root: wic
ms.assetid: 7b171c48-3fad-44ea-a9a5-8318e4cc3eba
ms.date: 12/05/2018
ms.keywords: GetFileExtensions, GetFileExtensions method [Windows Imaging Component], GetFileExtensions method [Windows Imaging Component],IWICBitmapCodecInfo interface, IWICBitmapCodecInfo interface [Windows Imaging Component],GetFileExtensions method, IWICBitmapCodecInfo.GetFileExtensions, IWICBitmapCodecInfo::GetFileExtensions, _wic_codec_iwicbitmapcodecinfo_getfileextensions, wic._wic_codec_iwicbitmapcodecinfo_getfileextensions, wincodec/IWICBitmapCodecInfo::GetFileExtensions
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
 - IWICBitmapCodecInfo::GetFileExtensions
 - wincodec/IWICBitmapCodecInfo::GetFileExtensions
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
 - IWICBitmapCodecInfo.GetFileExtensions
---

# IWICBitmapCodecInfo::GetFileExtensions


## -description

Retrieves a comma delimited list of the file name extensions associated with the codec.

## -parameters

### -param cchFileExtensions [in]

Type: <b>UINT</b>

The size of the file name extension buffer. Use <code>0</code> on first call to determine needed buffer size.

### -param wzFileExtensions [in, out]

Type: <b>WCHAR*</b>

Receives a comma delimited list  of file name extensions associated with the codec. Use <code>NULL</code> on first call to determine needed buffer size.

### -param pcchActual [in, out]

Type: <b>UINT*</b>

The actual buffer size needed to retrieve all file name extensions associated with the codec.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The default extension for an image encoder is the first item in the list of returned extensions.

The usage pattern for this method is a two call process.
               The first call retrieves the buffer size needed to retrieve the full color management version number by calling it with <i>cchFileExtensions</i> set to <code>0</code> and <i>wzFileExtensions</i> set to <code>NULL</code>.
               This call sets <i>pcchActual</i> to the buffer size needed.
               Once the needed buffer size is determined, a second <b>GetFileExtensions</b> call with <i>cchFileExtensions</i> set to the buffer size and <i>wzFileExtensions</i> set to a buffer of the appropriate size will retrieve the pixel formats.

