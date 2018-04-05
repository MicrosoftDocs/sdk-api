---
UID: NN:wincodec.IWICPixelFormatInfo
title: IWICPixelFormatInfo
author: windows-driver-content
description: Exposes methods that provide information about a pixel format.
old-location: wic\_wic_codec_iwicpixelformatinfo.htm
old-project: wic
ms.assetid: d5853b27-4329-40d8-bfd0-b4b0f39ba6d5
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: IWICPixelFormatInfo, IWICPixelFormatInfo interface [Windows Imaging Component], IWICPixelFormatInfo interface [Windows Imaging Component], described, _wic_codec_iwicpixelformatinfo, wic._wic_codec_iwicpixelformatinfo, wincodec/IWICPixelFormatInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.lib
-	Windowscodecs.dll
api_name:
-	IWICPixelFormatInfo
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICPixelFormatInfo interface


## -description


Exposes methods that provide information about a pixel format.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICPixelFormatInfo</b> interface inherits from <a href="https://msdn.microsoft.com/a31267ed-60cd-4de9-9fed-26bb390b29e6">IWICComponentInfo</a>. <b>IWICPixelFormatInfo</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/484fb014-5999-46b9-8e32-3fd5296e483f">GetBitsPerPixel</a>
</td>
<td align="left" width="63%">
Gets the BPP of the pixel format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/884262b8-dddf-4b8b-87aa-52d9e7952c91">GetChannelCount</a>
</td>
<td align="left" width="63%">
Gets the number of channels the pixel format contains.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da812e26-b0cc-49eb-a273-73b9bb579ba3">GetChannelMask</a>
</td>
<td align="left" width="63%">
Gets the pixel format's channel mask.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c35fc474-cbf5-4705-b0f1-a2e24a062a7a">GetColorContext</a>
</td>
<td align="left" width="63%">
Gets the pixel format's <a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/184ad8e5-51f2-47eb-b3c4-010626fa7c34">GetFormatGUID</a>
</td>
<td align="left" width="63%">
Gets the pixel format GUID.

</td>
</tr>
</table> 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/a31267ed-60cd-4de9-9fed-26bb390b29e6">IWICComponentInfo</a>



<a href="https://msdn.microsoft.com/348b6d15-e339-4dce-99f3-4d639ee9bf7d">Native Pixel Formats</a>



<a href="https://msdn.microsoft.com/a05b496a-bd4c-4065-8060-df0f8930cde7">Windows Imaging Component Overview</a>
 

 

