---
UID: NN:wincodec.IWICBitmap
title: IWICBitmap (wincodec.h)
author: windows-sdk-content
description: Defines methods that add the concept of writeability and static in-memory representations of bitmaps to IWICBitmapSource.
old-location: wic\_wic_codec_iwicbitmap.htm
tech.root: wic
ms.assetid: 15dcc80d-ef58-453d-a57a-348ffc7ddc6b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICBitmap, IWICBitmap interface [Windows Imaging Component], IWICBitmap interface [Windows Imaging Component],described, _wic_codec_iwicbitmap, wic._wic_codec_iwicbitmap, wincodec/IWICBitmap
ms.topic: interface
f1_keywords: 
 - "wincodec/IWICBitmap"
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
 - IWICBitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICBitmap interface


## -description


Defines methods that add the concept of writeability and static in-memory representations of bitmaps to <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICBitmap</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>. <b>IWICBitmap</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICBitmap</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmap-lock">Lock</a>
</td>
<td align="left" width="63%">
Provides access to a rectangular area of the bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmap-setpalette">SetPalette</a>
</td>
<td align="left" width="63%">
Provides access for palette modifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmap-setresolution">SetResolution</a>
</td>
<td align="left" width="63%">
Changes the physical resolution of the image.

</td>
</tr>
</table> 


## -remarks



<b>IWICBitmap</b> inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a> and therefore also inherits the <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels">CopyPixels</a> method.
            When pixels need to be moved to a new memory location, <b>CopyPixels</b> is often the most efficient.
         

Because of to the internal memory representation implied by the <b>IWICBitmap</b>, in-place modification and processing using the <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmap-lock">Lock</a> is more efficient than <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels">CopyPixels</a>, usually reducing to a simple pointer access directly into the memory owned by the bitmap rather than a as a copy. 
            This is contrasted to procedural bitmaps which implement only <b>CopyPixels</b> because there is no internal memory representation and one would need to be created on demand to satisfy a call to <b>Lock</b>. 
         



