---
UID: NN:wincodec.IWICPixelFormatInfo
title: IWICPixelFormatInfo (wincodec.h)
description: Exposes methods that provide information about a pixel format.
helpviewer_keywords: ["IWICPixelFormatInfo","IWICPixelFormatInfo interface [Windows Imaging Component]","IWICPixelFormatInfo interface [Windows Imaging Component]","described","_wic_codec_iwicpixelformatinfo","wic._wic_codec_iwicpixelformatinfo","wincodec/IWICPixelFormatInfo"]
old-location: wic\_wic_codec_iwicpixelformatinfo.htm
tech.root: wic
ms.assetid: d5853b27-4329-40d8-bfd0-b4b0f39ba6d5
ms.date: 12/05/2018
ms.keywords: IWICPixelFormatInfo, IWICPixelFormatInfo interface [Windows Imaging Component], IWICPixelFormatInfo interface [Windows Imaging Component],described, _wic_codec_iwicpixelformatinfo, wic._wic_codec_iwicpixelformatinfo, wincodec/IWICPixelFormatInfo
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
 - IWICPixelFormatInfo
 - wincodec/IWICPixelFormatInfo
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
 - IWICPixelFormatInfo
---

# IWICPixelFormatInfo interface


## -description

Exposes methods that provide information about a pixel format.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICPixelFormatInfo</b> interface inherits from <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccomponentinfo">IWICComponentInfo</a>. <b>IWICPixelFormatInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICPixelFormatInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicpixelformatinfo-getbitsperpixel">GetBitsPerPixel</a>
</td>
<td align="left" width="63%">
Gets the BPP of the pixel format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicpixelformatinfo-getchannelcount">GetChannelCount</a>
</td>
<td align="left" width="63%">
Gets the number of channels the pixel format contains.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicpixelformatinfo-getchannelmask">GetChannelMask</a>
</td>
<td align="left" width="63%">
Gets the pixel format's channel mask.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicpixelformatinfo-getcolorcontext">GetColorContext</a>
</td>
<td align="left" width="63%">
Gets the pixel format's <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicpixelformatinfo-getformatguid">GetFormatGUID</a>
</td>
<td align="left" width="63%">
Gets the pixel format GUID.

</td>
</tr>
</table>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccomponentinfo">IWICComponentInfo</a>



<a href="/windows/desktop/wic/-wic-codec-native-pixel-formats">Native Pixel Formats</a>



<a href="/windows/desktop/wic/-wic-about-windows-imaging-codec">Windows Imaging Component Overview</a>