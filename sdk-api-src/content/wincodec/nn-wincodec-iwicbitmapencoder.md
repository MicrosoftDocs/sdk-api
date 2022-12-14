---
UID: NN:wincodec.IWICBitmapEncoder
title: IWICBitmapEncoder (wincodec.h)
description: Defines methods for setting an encoder's properties such as thumbnails, frames, and palettes.
helpviewer_keywords: ["IWICBitmapEncoder","IWICBitmapEncoder interface [Windows Imaging Component]","IWICBitmapEncoder interface [Windows Imaging Component]","described","_wic_codec_iwicbitmapencoder","wic._wic_codec_iwicbitmapencoder","wincodec/IWICBitmapEncoder"]
old-location: wic\_wic_codec_iwicbitmapencoder.htm
tech.root: wic
ms.assetid: fe87c9ae-dedf-4ec2-ac11-0ea5fc6aa3ad
ms.date: 12/05/2018
ms.keywords: IWICBitmapEncoder, IWICBitmapEncoder interface [Windows Imaging Component], IWICBitmapEncoder interface [Windows Imaging Component],described, _wic_codec_iwicbitmapencoder, wic._wic_codec_iwicbitmapencoder, wincodec/IWICBitmapEncoder
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICBitmapEncoder
 - wincodec/IWICBitmapEncoder
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wincodec.h
api_name:
 - IWICBitmapEncoder
---

# IWICBitmapEncoder interface


## -description

Defines methods for setting an encoder's properties such as thumbnails, frames, and palettes.

## -inheritance

The <b>IWICBitmapEncoder</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICBitmapEncoder</b> also has these types of members:

## -remarks

There are a number of concrete implementations of this interface representing each of the standard encoders provided by the platform including bitmap (BMP), Portable Network Graphics (PNG), Joint Photographic Experts Group (JPEG), Graphics Interchange Format (GIF), Tagged Image File Format (TIFF), and Microsoft Windows Digital Photo (WDP). The following table includes the class identifier (CLSID) for each native encoder.
            

<table class="clsStd">
<tr>
<th>CLSID Name</th>
<th>CLSID</th>
</tr>
<tr>
<td>CLSID_WICBmpEncoder</td>
<td>0x69be8bb4, 0xd66d, 0x47c8, 0x86, 0x5a, 0xed, 0x15, 0x89, 0x43, 0x37, 0x82</td>
</tr>
<tr>
<td>CLSID_WICGifEncoder</td>
<td>0x114f5598, 0xb22, 0x40a0, 0x86, 0xa1, 0xc8, 0x3e, 0xa4, 0x95, 0xad, 0xbd</td>
</tr>
<tr>
<td>CLSID_WICHeifEncoder</td>
<td>0x0dbecec1, 0x9eb3, 0x4860, 0x9c, 0x6f, 0xdd, 0xbe, 0x86, 0x63, 0x45, 0x75</td>
</tr>
<tr>
<td>CLSID_WICJpegEncoder</td>
<td>0x1a34f5c1, 0x4a5a, 0x46dc, 0xb6, 0x44, 0x1f, 0x45, 0x67, 0xe7, 0xa6, 0x76</td>
</tr>
<tr>
<td>CLSID_WICPngEncoder</td>
<td>0x27949969, 0x876a, 0x41d7, 0x94, 0x47, 0x56, 0x8f, 0x6a, 0x35, 0xa4, 0xdc</td>
</tr>
<tr>
<td>CLSID_WICTiffEncoder</td>
<td>0x0131be10, 0x2001, 0x4c5f, 0xa9, 0xb0, 0xcc, 0x88, 0xfa, 0xb6, 0x4c, 0xe8</td>
</tr>
<tr>
<td>CLSID_WICWmpEncoder</td>
<td>0xac4ce3cb, 0xe1c1, 0x44cd, 0x82, 0x15, 0x5a, 0x16, 0x65, 0x50, 0x9e, 0xc2</td>
</tr>
</table>
 

Additionally this interface may be sub-classed to provide support for third party codecs as part of the extensibility model. See the <a href="/previous-versions/ms771770(v=vs.100)">AITCodec Sample CODEC</a>.

CLSID_WICHeifDecoder operates on HEIF (High Efficiency Image Format) images.

## -see-also

<a href="/previous-versions/ms771770(v=vs.100)">AITCodec Sample CODEC</a>



<b>Conceptual</b>



<a href="/windows/desktop/wic/-wic-howtowriteacodec">How to Write a WIC-Enabled CODEC</a>



<b>Other Resources</b>



<a href="/windows/desktop/wic/-wic-guids-clsids">WIC GUIDs and CLSIDs</a>



<a href="/windows/desktop/wic/-wic-about-windows-imaging-codec">Windows Imaging Component Overview</a>
