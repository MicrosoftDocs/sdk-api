---
UID: NF:wincodec.IWICBitmapFrameEncode.SetThumbnail
title: IWICBitmapFrameEncode::SetThumbnail (wincodec.h)
description: Sets the frame thumbnail if supported by the codec.
helpviewer_keywords: ["IWICBitmapFrameEncode interface [Windows Imaging Component]","SetThumbnail method","IWICBitmapFrameEncode.SetThumbnail","IWICBitmapFrameEncode::SetThumbnail","SetThumbnail","SetThumbnail method [Windows Imaging Component]","SetThumbnail method [Windows Imaging Component]","IWICBitmapFrameEncode interface","_wic_codec_iwicbitmapframeencode_setthumbnail","wic._wic_codec_iwicbitmapframeencode_setthumbnail","wincodec/IWICBitmapFrameEncode::SetThumbnail"]
old-location: wic\_wic_codec_iwicbitmapframeencode_setthumbnail.htm
tech.root: wic
ms.assetid: da6924cf-87c0-4774-a02e-5d54be65ef28
ms.date: 12/05/2018
ms.keywords: IWICBitmapFrameEncode interface [Windows Imaging Component],SetThumbnail method, IWICBitmapFrameEncode.SetThumbnail, IWICBitmapFrameEncode::SetThumbnail, SetThumbnail, SetThumbnail method [Windows Imaging Component], SetThumbnail method [Windows Imaging Component],IWICBitmapFrameEncode interface, _wic_codec_iwicbitmapframeencode_setthumbnail, wic._wic_codec_iwicbitmapframeencode_setthumbnail, wincodec/IWICBitmapFrameEncode::SetThumbnail
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
 - IWICBitmapFrameEncode::SetThumbnail
 - wincodec/IWICBitmapFrameEncode::SetThumbnail
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
 - IWICBitmapFrameEncode.SetThumbnail
---

# IWICBitmapFrameEncode::SetThumbnail


## -description

Sets the frame thumbnail if supported by the codec.

## -parameters

### -param pIThumbnail [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>*</b>

The bitmap source to use as the thumbnail.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise.
            

Returns WINCODEC_ERR_UNSUPPORTEDOPERATION if the feature is not supported by the encoder.

## -remarks

We recommend that you call
			   <b>SetThumbnail</b> before calling <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-writepixels">WritePixels</a> or <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-writesource">WriteSource</a>.
				The thumbnail won't be added to the encoded file if <b>SetThumbnail</b> is called after a call to <b>WritePixels</b> or <b>WriteSource</b>.
			

<ul>
<li><b>BMP, PNG</b>Setting thumbnails is unsupported. This function will return <b>WINCODEC_ERR_UNSUPPORTEDOPERATION</b>.

</li>
<li><b>JPEG</b>Setting the thumbnail is supported. The source image will be re-encoded as either an 8bpp or 24bpp JPEG and will be written to the JPEG’s APP1 metadata block.


</li>
<li><b>TIFF</b> Setting the thumbnail is supported. The source image will be re-encoded as a TIFF and will be written to the frame’s SubIFD block.

</li>
<li><b>JPEG-XR</b>Setting the thumbnail is supported. The source image will be re-encoded as an additional 8bpp or 24bpp frame.


</li>
</ul>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/wic/-wic-creating-encoder">Encoding Overview</a>



<a href="/windows/desktop/wic/-wic-howtowriteacodec">How to Write a WIC-Enabled CODEC</a>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframeencode">IWICBitmapFrameEncode</a>