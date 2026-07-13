---
UID: NF:wincodec.IWICBitmapCodecInfo.GetMimeTypes
title: IWICBitmapCodecInfo::GetMimeTypes (wincodec.h)
description: Retrieves a comma delimited sequence of mime types associated with the codec.
helpviewer_keywords: ["GetMimeTypes","GetMimeTypes method [Windows Imaging Component]","GetMimeTypes method [Windows Imaging Component]","IWICBitmapCodecInfo interface","IWICBitmapCodecInfo interface [Windows Imaging Component]","GetMimeTypes method","IWICBitmapCodecInfo.GetMimeTypes","IWICBitmapCodecInfo::GetMimeTypes","_wic_codec_iwicbitmapcodecinfo_getmimetypes","wic._wic_codec_iwicbitmapcodecinfo_getmimetypes","wincodec/IWICBitmapCodecInfo::GetMimeTypes"]
old-location: wic\_wic_codec_iwicbitmapcodecinfo_getmimetypes.htm
tech.root: wic
ms.assetid: fbca8068-a57d-402b-85e1-0dd284824efa
ms.date: 12/05/2018
ms.keywords: GetMimeTypes, GetMimeTypes method [Windows Imaging Component], GetMimeTypes method [Windows Imaging Component],IWICBitmapCodecInfo interface, IWICBitmapCodecInfo interface [Windows Imaging Component],GetMimeTypes method, IWICBitmapCodecInfo.GetMimeTypes, IWICBitmapCodecInfo::GetMimeTypes, _wic_codec_iwicbitmapcodecinfo_getmimetypes, wic._wic_codec_iwicbitmapcodecinfo_getmimetypes, wincodec/IWICBitmapCodecInfo::GetMimeTypes
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
 - IWICBitmapCodecInfo::GetMimeTypes
 - wincodec/IWICBitmapCodecInfo::GetMimeTypes
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
 - IWICBitmapCodecInfo.GetMimeTypes
---

# IWICBitmapCodecInfo::GetMimeTypes


## -description

Retrieves a comma delimited sequence of mime types associated with the codec.

## -parameters

### -param cchMimeTypes [in]

Type: <b>UINT</b>

The size of the mime types buffer.  Use <code>0</code> on first call to determine needed buffer size.

### -param wzMimeTypes [out]

Type: <b>WCHAR*</b>

Receives the mime types associated with the codec. Use <code>NULL</code> on first call to determine needed buffer size.

### -param pcchActual [out]

Type: <b>UINT*</b>

The actual buffer size needed to retrieve all mime types associated with the codec.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The usage pattern for this method is a two call process.
            The first call retrieves the buffer size needed to retrieve the full color management version number by calling it with <i>cchMimeTypes</i> set to <code>0</code> and <i>wzMimeTypes</i> set to <code>NULL</code>.
            This call sets <i>pcchActual</i> to the buffer size needed.
            Once the needed buffer size is determined, a second <b>GetMimeTypes</b> call with <i>cchMimeTypes</i> set to the buffer size and <i>wzMimeTypes</i> set to a buffer of the appropriate size will retrieve the pixel formats.

