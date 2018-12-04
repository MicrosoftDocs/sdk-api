---
UID: NN:wincodec.IWICBitmapDecoderInfo
title: IWICBitmapDecoderInfo
author: windows-sdk-content
description: Exposes methods that provide information about a decoder.
old-location: wic\_wic_codec_iwicbitmapdecoderinfo.htm
tech.root: wic
ms.assetid: 7edc6d1a-7eda-45ef-bf1d-c5835b37a90f
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IWICBitmapDecoderInfo, IWICBitmapDecoderInfo interface [Windows Imaging Component], IWICBitmapDecoderInfo interface [Windows Imaging Component],described, _wic_codec_iwicbitmapdecoderinfo, wic._wic_codec_iwicbitmapdecoderinfo, wincodec/IWICBitmapDecoderInfo
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWICBitmapDecoderInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICBitmapDecoderInfo interface


## -description


Exposes methods that provide information about a decoder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICBitmapDecoderInfo</b> interface inherits from <a href="https://msdn.microsoft.com/502a94bf-3ec4-44d2-b0de-9994f2f9861f">IWICBitmapCodecInfo</a>. <b>IWICBitmapDecoderInfo</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/2bda1c2a-47b9-4e15-b0c1-52e3f85a6523">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/91dafd5e-e4fb-4691-a3d0-ca8b6ff0aaf7">IWICBitmapDecoder</a> instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6143a431-cea6-4ced-adf5-2aa4d90d622f">GetPatterns</a>
</td>
<td align="left" width="63%">
Retrieves the file pattern signatures supported by the decoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/159459a4-f14e-4441-94a6-d55b3bacb868">MatchesPattern</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the codec recognizes the pattern within a specified stream.

</td>
</tr>
</table> 

