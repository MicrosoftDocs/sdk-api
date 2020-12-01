---
UID: NN:wincodec.IWICBitmapCodecInfo
title: IWICBitmapCodecInfo (wincodec.h)
description: Exposes methods that provide information about a particular codec.
helpviewer_keywords: ["IWICBitmapCodecInfo","IWICBitmapCodecInfo interface [Windows Imaging Component]","IWICBitmapCodecInfo interface [Windows Imaging Component]","described","_wic_codec_iwicbitmapcodecinfo","wic._wic_codec_iwicbitmapcodecinfo","wincodec/IWICBitmapCodecInfo"]
old-location: wic\_wic_codec_iwicbitmapcodecinfo.htm
tech.root: wic
ms.assetid: 502a94bf-3ec4-44d2-b0de-9994f2f9861f
ms.date: 12/05/2018
ms.keywords: IWICBitmapCodecInfo, IWICBitmapCodecInfo interface [Windows Imaging Component], IWICBitmapCodecInfo interface [Windows Imaging Component],described, _wic_codec_iwicbitmapcodecinfo, wic._wic_codec_iwicbitmapcodecinfo, wincodec/IWICBitmapCodecInfo
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
 - IWICBitmapCodecInfo
 - wincodec/IWICBitmapCodecInfo
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
 - IWICBitmapCodecInfo
---

# IWICBitmapCodecInfo interface


## -description

Exposes methods that provide information about a particular codec.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICBitmapCodecInfo</b> interface inherits from <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccomponentinfo">IWICComponentInfo</a>. <b>IWICBitmapCodecInfo</b> also has these types of members:
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
<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportanimation">DoesSupportAnimation</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the codec supports animation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportchromakey">DoesSupportChromakey</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the codec supports chromakeys.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportlossless">DoesSupportLossless</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the codec supports lossless formats.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportmultiframe">DoesSupportMultiframe</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the codec supports multi frame images.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapcodecinfo-getcolormanagementversion">GetColorManagementVersion</a>
</td>
<td align="left" width="63%">
Retrieves the color manangement version number the codec supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat">GetContainerFormat</a>
</td>
<td align="left" width="63%">
Retrieves the container GUID associated with the codec.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemanufacturer">GetDeviceManufacturer</a>
</td>
<td align="left" width="63%">
Retrieves the name of the device manufacture associated with the codec.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemodels">GetDeviceModels</a>
</td>
<td align="left" width="63%">
Retrieves a comma delimited list of device models associated with the codec.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapcodecinfo-getfileextensions">GetFileExtensions</a>
</td>
<td align="left" width="63%">
Retrieves a comma delimited list of the file name extensions associated with the codec.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapcodecinfo-getmimetypes">GetMimeTypes</a>
</td>
<td align="left" width="63%">
Retrieves a comma delimited sequence of mime types associated with the codec.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapcodecinfo-getpixelformats">GetPixelFormats</a>
</td>
<td align="left" width="63%">
Retrieves the pixel formats the codec supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapcodecinfo-matchesmimetype">MatchesMimeType</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the given mime type matches the mime type of the codec.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoderinfo">IWICBitmapDecoderInfo</a>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoderinfo">IWICBitmapEncoderInfo</a>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccomponentinfo">IWICComponentInfo</a>



<b>Reference</b>