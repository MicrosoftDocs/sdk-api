---
UID: NN:wincodec.IWICBitmapCodecInfo
title: IWICBitmapCodecInfo
author: windows-sdk-content
description: Exposes methods that provide information about a particular codec.
old-location: wic\_wic_codec_iwicbitmapcodecinfo.htm
tech.root: wic
ms.assetid: 502a94bf-3ec4-44d2-b0de-9994f2f9861f
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWICBitmapCodecInfo, IWICBitmapCodecInfo interface [Windows Imaging Component], IWICBitmapCodecInfo interface [Windows Imaging Component],described, _wic_codec_iwicbitmapcodecinfo, wic._wic_codec_iwicbitmapcodecinfo, wincodec/IWICBitmapCodecInfo
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
 - IWICBitmapCodecInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICBitmapCodecInfo interface


## -description


Exposes methods that provide information about a particular codec.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICBitmapCodecInfo</b> interface inherits from <a href="https://msdn.microsoft.com/a31267ed-60cd-4de9-9fed-26bb390b29e6">IWICComponentInfo</a>. <b>IWICBitmapCodecInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICBitmapCodecInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17635459-e067-4fdb-a801-4ad6cc622215">DoesSupportAnimation</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the codec supports animation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/662e213e-1ed2-445c-a7be-ff8a137fba2e">DoesSupportChromakey</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the codec supports chromakeys.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90a1f4cf-2641-4033-a369-ad6bf6fe5f43">DoesSupportLossless</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the codec supports lossless formats.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b20bceb4-71aa-4ef6-865a-0afb4850e316">DoesSupportMultiframe</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the codec supports multi frame images.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d115306-615a-403b-95f8-3e2850928928">GetColorManagementVersion</a>
</td>
<td align="left" width="63%">
Retrieves the color manangement version number the codec supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/164952ae-95ea-43b1-872c-088b2c1c65c8">GetContainerFormat</a>
</td>
<td align="left" width="63%">
Retrieves the container GUID associated with the codec.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a69e8195-5dc1-4a25-ab3c-9ea0cb3de074">GetDeviceManufacturer</a>
</td>
<td align="left" width="63%">
Retrieves the name of the device manufacture associated with the codec.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ccc5aab6-8817-4c18-8e52-a1372b015541">GetDeviceModels</a>
</td>
<td align="left" width="63%">
Retrieves a comma delimited list of device models associated with the codec.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b171c48-3fad-44ea-a9a5-8318e4cc3eba">GetFileExtensions</a>
</td>
<td align="left" width="63%">
Retrieves a comma delimited list of the file name extensions associated with the codec.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fbca8068-a57d-402b-85e1-0dd284824efa">GetMimeTypes</a>
</td>
<td align="left" width="63%">
Retrieves a comma delimited sequence of mime types associated with the codec.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2da56e46-bbbd-42d4-ba49-9dee01f6bba0">GetPixelFormats</a>
</td>
<td align="left" width="63%">
Retrieves the pixel formats the codec supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43704d5c-d2c2-4817-b61b-a752d32105aa">MatchesMimeType</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the given mime type matches the mime type of the codec.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/7edc6d1a-7eda-45ef-bf1d-c5835b37a90f">IWICBitmapDecoderInfo</a>



<a href="https://msdn.microsoft.com/152b0dd2-1e5e-47fc-b6eb-a4c042e65047">IWICBitmapEncoderInfo</a>



<a href="https://msdn.microsoft.com/a31267ed-60cd-4de9-9fed-26bb390b29e6">IWICComponentInfo</a>



<b>Reference</b>
 

 

