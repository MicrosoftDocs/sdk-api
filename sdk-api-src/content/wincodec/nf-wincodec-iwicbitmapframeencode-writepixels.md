---
UID: NF:wincodec.IWICBitmapFrameEncode.WritePixels
title: IWICBitmapFrameEncode::WritePixels (wincodec.h)
description: Copies scan-line data from a caller-supplied buffer to the IWICBitmapFrameEncode object.
helpviewer_keywords: ["IWICBitmapFrameEncode interface [Windows Imaging Component]","WritePixels method","IWICBitmapFrameEncode.WritePixels","IWICBitmapFrameEncode::WritePixels","WritePixels","WritePixels method [Windows Imaging Component]","WritePixels method [Windows Imaging Component]","IWICBitmapFrameEncode interface","_wic_codec_iwicbitmapframeencode_writepixels","wic._wic_codec_iwicbitmapframeencode_writepixels","wincodec/IWICBitmapFrameEncode::WritePixels"]
old-location: wic\_wic_codec_iwicbitmapframeencode_writepixels.htm
tech.root: wic
ms.assetid: 6b430fe0-5230-47dc-95c0-aeabd138cefe
ms.date: 12/05/2018
ms.keywords: IWICBitmapFrameEncode interface [Windows Imaging Component],WritePixels method, IWICBitmapFrameEncode.WritePixels, IWICBitmapFrameEncode::WritePixels, WritePixels, WritePixels method [Windows Imaging Component], WritePixels method [Windows Imaging Component],IWICBitmapFrameEncode interface, _wic_codec_iwicbitmapframeencode_writepixels, wic._wic_codec_iwicbitmapframeencode_writepixels, wincodec/IWICBitmapFrameEncode::WritePixels
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
 - IWICBitmapFrameEncode::WritePixels
 - wincodec/IWICBitmapFrameEncode::WritePixels
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
 - IWICBitmapFrameEncode.WritePixels
---

# IWICBitmapFrameEncode::WritePixels


## -description

Copies scan-line data from a caller-supplied buffer to the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframeencode">IWICBitmapFrameEncode</a> object.

## -parameters

### -param lineCount [in]

Type: <b>UINT</b>

The number of lines to encode.

### -param cbStride [in]

Type: <b>UINT</b>

The stride of the image pixels.

### -param cbBufferSize [in]

Type: <b>UINT</b>

The size of the pixel buffer.

### -param pbPixels [in]

Type: <b>BYTE*</b>

A pointer to the pixel buffer.

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
<dt><b>WINCODEC_ERR_CODECTOOMANYSCANLINES</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>lineCount</i> is larger than the number of scan lines in the image.

</td>
</tr>
</table>

## -remarks

Successive <b>WritePixels</b> calls are assumed to be sequential scan-line access in the output image.