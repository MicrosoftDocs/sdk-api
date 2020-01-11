---
UID: NN:wincodec.IWICBitmapFrameEncode
title: IWICBitmapFrameEncode (wincodec.h)
description: Represents an encoder's individual image frames.
old-location: wic\_wic_codec_iwicbitmapframeencode.htm
tech.root: wic
ms.assetid: a8de774b-3783-46be-9a21-c9fec2f10ffd
ms.date: 12/05/2018
ms.keywords: IWICBitmapFrameEncode, IWICBitmapFrameEncode interface [Windows Imaging Component], IWICBitmapFrameEncode interface [Windows Imaging Component],described, _wic_codec_iwicbitmapframeencode, wic._wic_codec_iwicbitmapframeencode, wincodec/IWICBitmapFrameEncode
f1_keywords:
- wincodec/IWICBitmapFrameEncode
dev_langs:
- c++
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
- IWICBitmapFrameEncode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICBitmapFrameEncode interface


## -description


Represents an encoder's individual image frames.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICBitmapFrameEncode</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICBitmapFrameEncode</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICBitmapFrameEncode</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-commit">Commit</a>
</td>
<td align="left" width="63%">
Commits the frame to the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter">GetMetadataQueryWriter</a>
</td>
<td align="left" width="63%">
Gets the metadata query writer for the encoder frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the frame encoder using the given properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts">SetColorContexts</a>
</td>
<td align="left" width="63%">
Sets a given number <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a> profiles to the frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-setpalette">SetPalette</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicpalette">IWICPalette</a> for indexed pixel formats.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat">SetPixelFormat</a>
</td>
<td align="left" width="63%">
Requests that the encoder use the specified pixel format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-setresolution">SetResolution</a>
</td>
<td align="left" width="63%">
Sets the physical resolution of the output image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-setsize">SetSize</a>
</td>
<td align="left" width="63%">
Sets the output image dimensions for the frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail">SetThumbnail</a>
</td>
<td align="left" width="63%">
Sets the frame thumbnail if supported by the codec.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-writepixels">WritePixels</a>
</td>
<td align="left" width="63%">
Encodes the frame scanlines.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-writesource">WriteSource</a>
</td>
<td align="left" width="63%">
Encodes a bitmap source.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/ms771770(v=vs.100)">AITCodec Sample CODEC</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-howtowriteacodec">How to Write a WIC-Enabled CODEC</a>



<b>Other Resources</b>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-guids-clsids">WIC GUIDs and CLSIDs</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-about-windows-imaging-codec">Windows Imaging Component Overview</a>
 

 

