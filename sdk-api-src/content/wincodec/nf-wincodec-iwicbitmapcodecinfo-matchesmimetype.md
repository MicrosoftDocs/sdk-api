---
UID: NF:wincodec.IWICBitmapCodecInfo.MatchesMimeType
title: IWICBitmapCodecInfo::MatchesMimeType (wincodec.h)
description: Retrieves a value indicating whether the given mime type matches the mime type of the codec.
helpviewer_keywords: ["IWICBitmapCodecInfo interface [Windows Imaging Component]","MatchesMimeType method","IWICBitmapCodecInfo.MatchesMimeType","IWICBitmapCodecInfo::MatchesMimeType","MatchesMimeType","MatchesMimeType method [Windows Imaging Component]","MatchesMimeType method [Windows Imaging Component]","IWICBitmapCodecInfo interface","_wic_codec_iwicbitmapcodecinfo_matchesmimetype","wic._wic_codec_iwicbitmapcodecinfo_matchesmimetype","wincodec/IWICBitmapCodecInfo::MatchesMimeType"]
old-location: wic\_wic_codec_iwicbitmapcodecinfo_matchesmimetype.htm
tech.root: wic
ms.assetid: 43704d5c-d2c2-4817-b61b-a752d32105aa
ms.date: 12/05/2018
ms.keywords: IWICBitmapCodecInfo interface [Windows Imaging Component],MatchesMimeType method, IWICBitmapCodecInfo.MatchesMimeType, IWICBitmapCodecInfo::MatchesMimeType, MatchesMimeType, MatchesMimeType method [Windows Imaging Component], MatchesMimeType method [Windows Imaging Component],IWICBitmapCodecInfo interface, _wic_codec_iwicbitmapcodecinfo_matchesmimetype, wic._wic_codec_iwicbitmapcodecinfo_matchesmimetype, wincodec/IWICBitmapCodecInfo::MatchesMimeType
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
 - IWICBitmapCodecInfo::MatchesMimeType
 - wincodec/IWICBitmapCodecInfo::MatchesMimeType
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
 - IWICBitmapCodecInfo.MatchesMimeType
---

# IWICBitmapCodecInfo::MatchesMimeType


## -description

Retrieves a value indicating whether the given mime type matches the mime type of the codec.

## -parameters

### -param wzMimeType [in]

Type: <b>LPCWSTR</b>

The mime type to compare.

### -param pfMatches [out]

Type: <b>BOOL*</b>

Receives <b>TRUE</b> if the mime types match; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The codec does not implement this method.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  The Windows provided codecs do not implement this method and return E_NOTIMPL.</div>
<div> </div>

