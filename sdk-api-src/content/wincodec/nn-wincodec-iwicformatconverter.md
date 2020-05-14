---
UID: NN:wincodec.IWICFormatConverter
title: IWICFormatConverter (wincodec.h)
description: Represents an IWICBitmapSource that converts the image data from one pixel format to another, handling dithering and halftoning to indexed formats, palette translation and alpha thresholding.helpviewer_keywords: ["IWICFormatConverter","IWICFormatConverter interface [Windows Imaging Component]","IWICFormatConverter interface [Windows Imaging Component]","described","_wic_codec_iwicformatconverter","wic._wic_codec_iwicformatconverter","wincodec/IWICFormatConverter"]
old-location: wic\_wic_codec_iwicformatconverter.htm
tech.root: wic
ms.assetid: d558aaa7-5962-424c-9e83-363fba09ad50
ms.date: 12/05/2018
ms.keywords: IWICFormatConverter, IWICFormatConverter interface [Windows Imaging Component], IWICFormatConverter interface [Windows Imaging Component],described, _wic_codec_iwicformatconverter, wic._wic_codec_iwicformatconverter, wincodec/IWICFormatConverter
f1_keywords:
- wincodec/IWICFormatConverter
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
- IWICFormatConverter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICFormatConverter interface


## -description


Represents an <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a> that converts the image data from one pixel format to another, handling dithering and halftoning to indexed formats, palette translation and alpha thresholding.
         


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICFormatConverter</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>. <b>IWICFormatConverter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICFormatConverter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicformatconverter-canconvert">CanConvert</a>
</td>
<td align="left" width="63%">
Determines if the source pixel format can be converted to the destination pixel format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicformatconverter-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the format converter.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/dotnet/netframework-3.0/ms771770(v=vs.85)">AITCodec Sample CODEC</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-howtowriteacodec">How to Write a WIC-Enabled CODEC</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>



<b>Other Resources</b>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-guids-clsids">WIC GUIDs and CLSIDs</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-about-windows-imaging-codec">Windows Imaging Component Overview</a>
 

 

