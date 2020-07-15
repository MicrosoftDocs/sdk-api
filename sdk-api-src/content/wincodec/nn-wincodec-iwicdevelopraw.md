---
UID: NN:wincodec.IWICDevelopRaw
title: IWICDevelopRaw (wincodec.h)
description: Exposes methods that provide access to the capabilites of a raw codec format.
helpviewer_keywords: ["IWICDevelopRaw","IWICDevelopRaw interface [Windows Imaging Component]","IWICDevelopRaw interface [Windows Imaging Component]","described","_wic_codec_iwicdevelopraw","wic._wic_codec_iwicdevelopraw","wincodec/IWICDevelopRaw"]
old-location: wic\_wic_codec_iwicdevelopraw.htm
tech.root: wic
ms.assetid: d449f3f7-fd43-44b0-ab7f-2ae307a74191
ms.date: 12/05/2018
ms.keywords: IWICDevelopRaw, IWICDevelopRaw interface [Windows Imaging Component], IWICDevelopRaw interface [Windows Imaging Component],described, _wic_codec_iwicdevelopraw, wic._wic_codec_iwicdevelopraw, wincodec/IWICDevelopRaw
f1_keywords:
- wincodec/IWICDevelopRaw
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
- IWICDevelopRaw
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICDevelopRaw interface


## -description


Exposes methods that provide access to the capabilites of a raw codec format.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICDevelopRaw</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode">IWICBitmapFrameDecode</a>. <b>IWICDevelopRaw</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICDevelopRaw</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-getcontrast">GetContrast</a>
</td>
<td align="left" width="63%">
Gets the contrast value of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset">GetCurrentParameterSet</a>
</td>
<td align="left" width="63%">
Gets the current set of parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-getexposurecompensation">GetExposureCompensation</a>
</td>
<td align="left" width="63%">
Gets the exposure compensation stop value of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-getgamma">GetGamma</a>
</td>
<td align="left" width="63%">
Gets the current gamma setting of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-getkelvinrangeinfo">GetKelvinRangeInfo</a>
</td>
<td align="left" width="63%">
Gets the information about the current Kelvin range of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-getnamedwhitepoint">GetNamedWhitePoint</a>
</td>
<td align="left" width="63%">
Gets the named white point of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-getnoisereduction">GetNoiseReduction</a>
</td>
<td align="left" width="63%">
Gets the noise reduction value of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-getrendermode">GetRenderMode</a>
</td>
<td align="left" width="63%">
Gets the current <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/ne-wincodec-wicrawrendermode">WICRawRenderMode</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-getrotation">GetRotation</a>
</td>
<td align="left" width="63%">
Gets the current rotation angle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-getsaturation">GetSaturation</a>
</td>
<td align="left" width="63%">
Gets the saturation value of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-getsharpness">GetSharpness</a>
</td>
<td align="left" width="63%">
Gets the sharpness value of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-gettint">GetTint</a>
</td>
<td align="left" width="63%">
Gets the tint value of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-gettonecurve">GetToneCurve</a>
</td>
<td align="left" width="63%">
Gets the tone curve of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-getwhitepointkelvin">GetWhitePointKelvin</a>
</td>
<td align="left" width="63%">
Gets the white point Kelvin temperature of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-getwhitepointrgb">GetWhitePointRGB</a>
</td>
<td align="left" width="63%">
Gets the white point RGB values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-loadparameterset">LoadParameterSet</a>
</td>
<td align="left" width="63%">
Sets the desired <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/ne-wincodec-wicrawparameterset">WICRawParameterSet</a> option.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-queryrawcapabilitiesinfo">QueryRawCapabilitiesInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about which capabilities are supported for a raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-setcontrast">SetContrast</a>
</td>
<td align="left" width="63%">
Sets the contrast value of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-setdestinationcolorcontext">SetDestinationColorContext</a>
</td>
<td align="left" width="63%">
Sets the destination color context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-setexposurecompensation">SetExposureCompensation</a>
</td>
<td align="left" width="63%">
Sets the exposure compensation stop value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-setgamma">SetGamma</a>
</td>
<td align="left" width="63%">
Sets the desired gamma value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-setnamedwhitepoint">SetNamedWhitePoint</a>
</td>
<td align="left" width="63%">
Sets the named white point of the raw file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-setnoisereduction">SetNoiseReduction</a>
</td>
<td align="left" width="63%">
Sets the noise reduction value of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-setnotificationcallback">SetNotificationCallback</a>
</td>
<td align="left" width="63%">
Sets the notification callback method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-setrendermode">SetRenderMode</a>
</td>
<td align="left" width="63%">
Sets the current <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/ne-wincodec-wicrawrendermode">WICRawRenderMode</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-setrotation">SetRotation</a>
</td>
<td align="left" width="63%">
Sets the desired rotation angle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-setsaturation">SetSaturation</a>
</td>
<td align="left" width="63%">
Sets the saturation value of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-setsharpness">SetSharpness</a>
</td>
<td align="left" width="63%">
Sets the sharpness value of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-settint">SetTint</a>
</td>
<td align="left" width="63%">
Sets the tint value of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-settonecurve">SetToneCurve</a>
</td>
<td align="left" width="63%">
Sets the tone curve for the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-setwhitepointkelvin">SetWhitePointKelvin</a>
</td>
<td align="left" width="63%">
Sets the white point Kelvin value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-setwhitepointrgb">SetWhitePointRGB</a>
</td>
<td align="left" width="63%">
Sets the white point RGB values.

</td>
</tr>
</table> 


## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-howtowriteacodec">How to Write a WIC-Enabled CODEC</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode">IWICBitmapFrameDecode</a>



<b>Other Resources</b>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-guids-clsids">WIC GUIDs and CLSIDs</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-about-windows-imaging-codec">Windows Imaging Component Overview</a>
 

 

