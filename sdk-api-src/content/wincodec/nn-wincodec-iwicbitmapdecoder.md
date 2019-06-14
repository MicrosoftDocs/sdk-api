---
UID: NN:wincodec.IWICBitmapDecoder
title: IWICBitmapDecoder (wincodec.h)
author: windows-sdk-content
description: Exposes methods that represent a decoder.
old-location: wic\_wic_codec_iwicbitmapdecoder.htm
tech.root: wic
ms.assetid: 91dafd5e-e4fb-4691-a3d0-ca8b6ff0aaf7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICBitmapDecoder, IWICBitmapDecoder interface [Windows Imaging Component], IWICBitmapDecoder interface [Windows Imaging Component],described, _wic_codec_iwicbitmapdecoder, wic._wic_codec_iwicbitmapdecoder, wincodec/IWICBitmapDecoder
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICBitmapDecoder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICBitmapDecoder interface


## -description


Exposes methods that represent a decoder.

The interface provides access to the decoder's properties such as global thumbnails (if supported), frames, and palette. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICBitmapDecoder</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICBitmapDecoder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICBitmapDecoder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-copypalette">CopyPalette</a>
</td>
<td align="left" width="63%">
Copies the decoder's <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicpalette">IWICPalette</a> .

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts">GetColorContexts</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a> objects of the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat">GetContainerFormat</a>
</td>
<td align="left" width="63%">
Retrieves the image's container format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo">GetDecoderInfo</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoderinfo">IWICBitmapDecoderInfo</a> for the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getframe">GetFrame</a>
</td>
<td align="left" width="63%">
Retrieves the specified frame of the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getframecount">GetFrameCount</a>
</td>
<td align="left" width="63%">
Retrieves the total number of frames in the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader">GetMetadataQueryReader</a>
</td>
<td align="left" width="63%">
Retrieves the metadata query reader from the decoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getpreview">GetPreview</a>
</td>
<td align="left" width="63%">
Retrieves a preview image, if supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail">GetThumbnail</a>
</td>
<td align="left" width="63%">
Retrieves a bitmap thumbnail of the image, if one exists

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the decoder with the provided stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-querycapability">QueryCapability</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of the decoder based on the specified stream.

</td>
</tr>
</table> 


## -remarks



There are a number of concrete implemenations of this interface representing each of the standard decoders provided by the platform including bitmap (BMP), Portable Network Graphics (PNG), icon (ICO), Joint Photographic Experts Group (JPEG), Graphics Interchange Format (GIF), Tagged Image File Format (TIFF), and Microsoft Windows Digital Photo (WDP). The following table includes the class identifier (CLSID) for each native decoder.
            

<table class="clsStd">
<tr>
<th>CLSID Name</th>
<th>CLSID</th>
</tr>
<tr>
<td>CLSID_WICBmpDecoder</td>
<td>0x6b462062, 0x7cbf, 0x400d, 0x9f, 0xdb, 0x81, 0x3d, 0xd1, 0xf, 0x27, 0x78</td>
</tr>
<tr>
<td>CLSID_WICGifDecoder</td>
<td>0x381dda3c, 0x9ce9, 0x4834, 0xa2, 0x3e, 0x1f, 0x98, 0xf8, 0xfc, 0x52, 0xbe</td>
</tr>
<tr>
<td>CLSID_WICHeifDecoder</td>
<td>0xe9a4a80a, 0x44fe, 0x4de4, 0x89, 0x71, 0x71, 0x50, 0xb1, 0x0a, 0x51, 0x99</td>
</tr>
<tr>
<td>CLSID_WICIcoDecoder</td>
<td>0xc61bfcdf, 0x2e0f, 0x4aad, 0xa8, 0xd7, 0xe0, 0x6b, 0xaf, 0xeb, 0xcd, 0xfe</td>
</tr>
<tr>
<td>CLSID_WICJpegDecoder</td>
<td>0x9456a480, 0xe88b, 0x43ea, 0x9e, 0x73, 0xb, 0x2d, 0x9b, 0x71, 0xb1, 0xca</td>
</tr>
<tr>
<td>CLSID_WICPngDecoder</td>
<td>0x389ea17b, 0x5078, 0x4cde, 0xb6, 0xef, 0x25, 0xc1, 0x51, 0x75, 0xc7, 0x51</td>
</tr>
<tr>
<td>CLSID_WICTiffDecoder</td>
<td>0xb54e85d9, 0xfe23, 0x499f, 0x8b, 0x88, 0x6a, 0xce, 0xa7, 0x13, 0x75, 0x2b</td>
</tr>
<tr>
<td>CLSID_WICWebpDecoder</td>
<td>0x7693e886, 0x51c9, 0x4070, 0x84, 0x19, 0x9f, 0x70, 0X73, 0X8e, 0Xc8, 0Xfa</td>
</tr>
<tr>
<td>CLSID_WICWmpDecoder</td>
<td>0xa26cec36, 0x234c, 0x4950, 0xae, 0x16, 0xe3, 0x4a, 0xac, 0xe7, 0x1d, 0x0d</td>
</tr>
</table>
 

This interface may be sub-classed to provide support for third party codecs as part of the extensibility model. See the <a href="https://docs.microsoft.com/previous-versions/ms771770(v=vs.100)">AITCodec Sample CODEC</a>.

Codecs written as TIFF container formats that are not register will decode as a TIFF image. Client applications should check for a zero frame count to determine if the codec is valid.

CLSID_WICHeifDecoder operates on HEIF (High Efficiency Image Format) images.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/dotnet/netframework-3.0/ms771770(v=vs.85)">AITCodec Sample CODEC</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-howtowriteacodec">How to Write a WIC-Enabled CODEC</a>



<b>Other Resources</b>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-guids-clsids">WIC GUIDs and CLSIDs</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-about-windows-imaging-codec">Windows Imaging Component Overview</a>
 

 

