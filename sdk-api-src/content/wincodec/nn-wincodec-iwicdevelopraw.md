---
UID: NN:wincodec.IWICDevelopRaw
title: IWICDevelopRaw
author: windows-driver-content
description: Exposes methods that provide access to the capabilites of a raw codec format.
old-location: wic\_wic_codec_iwicdevelopraw.htm
old-project: wic
ms.assetid: d449f3f7-fd43-44b0-ab7f-2ae307a74191
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: IWICDevelopRaw, IWICDevelopRaw interface [Windows Imaging Component], IWICDevelopRaw interface [Windows Imaging Component],described, _wic_codec_iwicdevelopraw, wic._wic_codec_iwicdevelopraw, wincodec/IWICDevelopRaw
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
-	Windowscodecs.dll
api_name:
-	IWICDevelopRaw
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICDevelopRaw interface


## -description


Exposes methods that provide access to the capabilites of a raw codec format.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICDevelopRaw</b> interface inherits from <a href="https://msdn.microsoft.com/1498b800-6449-440f-bed7-85891637e559">IWICBitmapFrameDecode</a>. <b>IWICDevelopRaw</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/65454979-f282-42da-80b6-e50955634093">GetContrast</a>
</td>
<td align="left" width="63%">
Gets the contrast value of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06facc60-0d88-472d-827a-70e4006e947e">GetCurrentParameterSet</a>
</td>
<td align="left" width="63%">
Gets the current set of parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cdd71702-4696-4533-bd6f-ba9324b6b05b">GetExposureCompensation</a>
</td>
<td align="left" width="63%">
Gets the exposure compensation stop value of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d76fc2dc-9bcc-4d7b-93fd-82a9647e7b6f">GetGamma</a>
</td>
<td align="left" width="63%">
Gets the current gamma setting of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c718c957-3523-4281-aa7e-761977a6b4c5">GetKelvinRangeInfo</a>
</td>
<td align="left" width="63%">
Gets the information about the current Kelvin range of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2fa5f0c8-fee2-4338-992a-5c927883a731">GetNamedWhitePoint</a>
</td>
<td align="left" width="63%">
Gets the named white point of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38dee560-16c1-4a91-8a8d-ed42dcdbb9ff">GetNoiseReduction</a>
</td>
<td align="left" width="63%">
Gets the noise reduction value of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8cf4508-6a2c-4d02-b98f-0455a3dc966c">GetRenderMode</a>
</td>
<td align="left" width="63%">
Gets the current <a href="https://msdn.microsoft.com/dc020c78-a018-42ee-a500-65a743b96107">WICRawRenderMode</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/671bca6d-bbe5-4f07-9735-12d796013d9e">GetRotation</a>
</td>
<td align="left" width="63%">
Gets the current rotation angle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/621868d6-3444-48f9-a069-f52ebacd7bbb">GetSaturation</a>
</td>
<td align="left" width="63%">
Gets the saturation value of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3cb0749-5ec6-4c29-824f-ae44f554d494">GetSharpness</a>
</td>
<td align="left" width="63%">
Gets the sharpness value of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12b7ecbe-efa9-47f4-b3b5-5ae1e1a66c3b">GetTint</a>
</td>
<td align="left" width="63%">
Gets the tint value of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/651f9efb-145a-400b-8d7c-255aee67c385">GetToneCurve</a>
</td>
<td align="left" width="63%">
Gets the tone curve of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f649de0-6b53-4c67-b75d-73a44cc07c56">GetWhitePointKelvin</a>
</td>
<td align="left" width="63%">
Gets the white point Kelvin temperature of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e163ba80-6ed2-4f03-b74f-07c96b478ac0">GetWhitePointRGB</a>
</td>
<td align="left" width="63%">
Gets the white point RGB values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3882d90-5772-4b10-8fcc-8d16f5004a05">LoadParameterSet</a>
</td>
<td align="left" width="63%">
Sets the desired <a href="https://msdn.microsoft.com/0c39b769-9523-42ce-942f-761e6d39ec5b">WICRawParameterSet</a> option.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a16ada3c-34ae-47ce-9660-90e50d78802a">QueryRawCapabilitiesInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about which capabilities are supported for a raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5013d351-e96d-44c7-88d7-65a55e474b01">SetContrast</a>
</td>
<td align="left" width="63%">
Sets the contrast value of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5e82941-b52d-4f5b-8134-c3463464f1ac">SetDestinationColorContext</a>
</td>
<td align="left" width="63%">
Sets the destination color context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57ee5b96-2e49-415c-b1a8-41436a761b23">SetExposureCompensation</a>
</td>
<td align="left" width="63%">
Sets the exposure compensation stop value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14d3b34c-1628-4e49-b07c-141f2933c86e">SetGamma</a>
</td>
<td align="left" width="63%">
Sets the desired gamma value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb83233d-7967-4160-bebf-2b06378f77ab">SetNamedWhitePoint</a>
</td>
<td align="left" width="63%">
Sets the named white point of the raw file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0c78274-0a1f-4a98-a449-ae902795a71b">SetNoiseReduction</a>
</td>
<td align="left" width="63%">
Sets the noise reduction value of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f6c44dee-8dbd-49c2-9773-899b3f01b968">SetNotificationCallback</a>
</td>
<td align="left" width="63%">
Sets the notification callback method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3150abb3-795d-416d-b3eb-0001796f510d">SetRenderMode</a>
</td>
<td align="left" width="63%">
Sets the current <a href="https://msdn.microsoft.com/dc020c78-a018-42ee-a500-65a743b96107">WICRawRenderMode</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1eba6004-d22e-4168-9207-358c072c3a17">SetRotation</a>
</td>
<td align="left" width="63%">
Sets the desired rotation angle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93e9eb1c-8428-4c4d-913a-d6162430e509">SetSaturation</a>
</td>
<td align="left" width="63%">
Sets the saturation value of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c989362-0c76-4028-ac27-c49e3ec1c6fd">SetSharpness</a>
</td>
<td align="left" width="63%">
Sets the sharpness value of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5c6a15b-19d3-4b6f-a00e-842ec8614ce5">SetTint</a>
</td>
<td align="left" width="63%">
Sets the tint value of the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cfb0b67d-7eb1-4bbb-90be-33ca82b9460f">SetToneCurve</a>
</td>
<td align="left" width="63%">
Sets the tone curve for the raw image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a5235ed-b0c8-4090-9380-892e3e994d10">SetWhitePointKelvin</a>
</td>
<td align="left" width="63%">
Sets the white point Kelvin value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7059959f-dcd6-46a6-a95c-1dd9610f865c">SetWhitePointRGB</a>
</td>
<td align="left" width="63%">
Sets the white point RGB values.

</td>
</tr>
</table> 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/58f03dc2-cc31-4d76-b75a-f332da1f900f">How to Write a WIC-Enabled CODEC</a>



<a href="https://msdn.microsoft.com/1498b800-6449-440f-bed7-85891637e559">IWICBitmapFrameDecode</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/2be5cfeb-2dd3-4486-b639-35ee28a7dd7b">WIC GUIDs and CLSIDs</a>



<a href="https://msdn.microsoft.com/a05b496a-bd4c-4065-8060-df0f8930cde7">Windows Imaging Component Overview</a>
 

 

