---
UID: NN:wincodec.IWICBitmapSource
title: IWICBitmapSource (wincodec.h)
description: Exposes methods that refers to a source from which pixels are retrieved, but cannot be written back to.
helpviewer_keywords: ["IWICBitmapSource","IWICBitmapSource interface [Windows Imaging Component]","IWICBitmapSource interface [Windows Imaging Component]","described","_wic_codec_iwicbitmapsource","wic._wic_codec_iwicbitmapsource","wincodec/IWICBitmapSource"]
old-location: wic\_wic_codec_iwicbitmapsource.htm
tech.root: wic
ms.assetid: abcc84af-6067-4856-8618-fb66aff4255a
ms.date: 12/05/2018
ms.keywords: IWICBitmapSource, IWICBitmapSource interface [Windows Imaging Component], IWICBitmapSource interface [Windows Imaging Component],described, _wic_codec_iwicbitmapsource, wic._wic_codec_iwicbitmapsource, wincodec/IWICBitmapSource
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
 - IWICBitmapSource
 - wincodec/IWICBitmapSource
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
 - IWICBitmapSource
---

# IWICBitmapSource interface


## -description

Exposes methods that refers to a source from which pixels are retrieved, but cannot be written back to.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICBitmapSource</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICBitmapSource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICBitmapSource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypalette">CopyPalette</a>
</td>
<td align="left" width="63%">
Retrieves the color table for indexed pixel formats.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels">CopyPixels</a>
</td>
<td align="left" width="63%">
Instructs the object to produce pixels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-getpixelformat">GetPixelFormat</a>
</td>
<td align="left" width="63%">
Retrieves the pixel format of the bitmap source.. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-getresolution">GetResolution</a>
</td>
<td align="left" width="63%">
Retrieves the sampling rate between pixels and physical world measurements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-getsize">GetSize</a>
</td>
<td align="left" width="63%">
Retrieves the pixel width and height of the bitmap.

</td>
</tr>
</table>

## -remarks

This interface provides a common way of accessing and linking together bitmaps, decoders, format converters, and scalers. Components that implement this interface can be connected together in a graph to pull imaging data through.

This interface defines only the notion of readability or being able to produce pixels. Modifying or writing to a bitmap is considered to be a specialization specific to bitmaps which have storage and is defined in the descendant interface <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmap">IWICBitmap</a>.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmap">IWICBitmap</a>

