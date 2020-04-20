---
UID: NN:wincodec.IWICBitmapDecoderInfo
title: IWICBitmapDecoderInfo (wincodec.h)
description: Exposes methods that provide information about a decoder.helpviewer_keywords: ["IWICBitmapDecoderInfo","IWICBitmapDecoderInfo interface [Windows Imaging Component]","IWICBitmapDecoderInfo interface [Windows Imaging Component]","described","_wic_codec_iwicbitmapdecoderinfo","wic._wic_codec_iwicbitmapdecoderinfo","wincodec/IWICBitmapDecoderInfo"]
old-location: wic\_wic_codec_iwicbitmapdecoderinfo.htm
tech.root: wic
ms.assetid: 7edc6d1a-7eda-45ef-bf1d-c5835b37a90f
ms.date: 12/05/2018
ms.keywords: IWICBitmapDecoderInfo, IWICBitmapDecoderInfo interface [Windows Imaging Component], IWICBitmapDecoderInfo interface [Windows Imaging Component],described, _wic_codec_iwicbitmapdecoderinfo, wic._wic_codec_iwicbitmapdecoderinfo, wincodec/IWICBitmapDecoderInfo
f1_keywords:
- wincodec/IWICBitmapDecoderInfo
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
- IWICBitmapDecoderInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICBitmapDecoderInfo interface


## -description


Exposes methods that provide information about a decoder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICBitmapDecoderInfo</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapcodecinfo">IWICBitmapCodecInfo</a>. <b>IWICBitmapDecoderInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICBitmapDecoderInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoderinfo-createinstance">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder">IWICBitmapDecoder</a> instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoderinfo-getpatterns">GetPatterns</a>
</td>
<td align="left" width="63%">
Retrieves the file pattern signatures supported by the decoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoderinfo-matchespattern">MatchesPattern</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the codec recognizes the pattern within a specified stream.

</td>
</tr>
</table> 

