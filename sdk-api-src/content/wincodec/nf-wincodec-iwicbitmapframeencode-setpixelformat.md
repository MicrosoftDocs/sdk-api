---
UID: NF:wincodec.IWICBitmapFrameEncode.SetPixelFormat
title: IWICBitmapFrameEncode::SetPixelFormat (wincodec.h)
description: Requests that the encoder use the specified pixel format.
helpviewer_keywords: ["IWICBitmapFrameEncode interface [Windows Imaging Component]","SetPixelFormat method","IWICBitmapFrameEncode.SetPixelFormat","IWICBitmapFrameEncode::SetPixelFormat","SetPixelFormat","SetPixelFormat method [Windows Imaging Component]","SetPixelFormat method [Windows Imaging Component]","IWICBitmapFrameEncode interface","_wic_codec_iwicbitmapframeencode_setpixelformat","wic._wic_codec_iwicbitmapframeencode_setpixelformat","wincodec/IWICBitmapFrameEncode::SetPixelFormat"]
old-location: wic\_wic_codec_iwicbitmapframeencode_setpixelformat.htm
tech.root: wic
ms.assetid: 9327b5dd-18a3-40c6-8bb4-245fcc7fb582
ms.date: 12/05/2018
ms.keywords: IWICBitmapFrameEncode interface [Windows Imaging Component],SetPixelFormat method, IWICBitmapFrameEncode.SetPixelFormat, IWICBitmapFrameEncode::SetPixelFormat, SetPixelFormat, SetPixelFormat method [Windows Imaging Component], SetPixelFormat method [Windows Imaging Component],IWICBitmapFrameEncode interface, _wic_codec_iwicbitmapframeencode_setpixelformat, wic._wic_codec_iwicbitmapframeencode_setpixelformat, wincodec/IWICBitmapFrameEncode::SetPixelFormat
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
 - IWICBitmapFrameEncode::SetPixelFormat
 - wincodec/IWICBitmapFrameEncode::SetPixelFormat
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
 - IWICBitmapFrameEncode.SetPixelFormat
---

# IWICBitmapFrameEncode::SetPixelFormat


## -description

Requests that the encoder use the specified pixel format.

## -parameters

### -param pPixelFormat [in, out]

Type: <b>WICPixelFormatGUID*</b>

On input, the requested pixel format GUID. On output, the closest pixel format GUID supported by the encoder; this may be different than the requested format. For a list of pixel format GUIDs, see <a href="/windows/desktop/wic/-wic-codec-native-pixel-formats">Native Pixel Formats</a>.

## -returns

Type: <b>HRESULT</b>

Possible return values include the following.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINCODEC_ERR_WRONGSTATE</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-initialize">IWICBitmapFrameEncode::Initialize</a> method was not called.

</td>
</tr>
</table>

## -remarks

The encoder might not support the requested pixel format. If not, <b>SetPixelFormat</b> returns the closest match in the memory block that <i>pPixelFormat</i> points to. If the returned pixel format doesn't match the requested format, you must use an <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter">IWICFormatConverter</a> object to convert the pixel data.

## -see-also

<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframeencode">IWICBitmapFrameEncode</a>



<a href="/windows/desktop/wic/-wic-codec-native-pixel-formats">Native Pixel Formats</a>