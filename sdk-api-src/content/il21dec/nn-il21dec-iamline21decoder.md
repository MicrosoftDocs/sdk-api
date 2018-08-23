---
UID: NN:il21dec.IAMLine21Decoder
title: IAMLine21Decoder
author: windows-sdk-content
description: The IAMLine21Decoder interface sets and retrieves information about closed captions.The Line 21 Decoder filter exposes this interface.
old-location: dshow\iamline21decoder.htm
old-project: DirectShow
ms.assetid: b6fbb5c3-28af-4db6-8dc4-82271b69bf71
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IAMLine21Decoder, IAMLine21Decoder interface [DirectShow], IAMLine21Decoder interface [DirectShow],described, IAMLine21DecoderInterface, dshow.iamline21decoder, il21dec/IAMLine21Decoder
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: il21dec.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AM_LINE21_DRAWBGMODE, *PAM_LINE21_DRAWBGMODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMLine21Decoder
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IAMLine21Decoder interface


## -description



The <code>IAMLine21Decoder</code> interface sets and retrieves information about closed captions.

The <a href="https://msdn.microsoft.com/48fa5484-1f8c-4133-b2e1-888cb1834402">Line 21 Decoder</a> filter exposes this interface. Applications can use this interface to enable or disable closed captions, select the closed captioning service, and set other closed captioning properties.

Closed-captioned information is transmitted on line 21 of field 1 in the vertical blanking interval (VBI) of television signals. Video cassette recorders record this information on video tape, and you can use the Line21 Decoder and other DirectShow filters to capture the line 21 data and save it on disk in a media file format such as Audio-Video Interleaved (AVI). The closed-captioned information appears as a separate stream within the media file.

Closed-captioned text is used in television programming and DVD movies. DVD movies contain line 21 data as part of the user data section of each Group of Pictures (GOP) in the video stream. Television receiver cards with Windows Driver Model (WDM) drivers provide line 21 data.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMLine21Decoder</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMLine21Decoder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMLine21Decoder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba75dc5b-207e-4425-a8fe-8da16fc89921">GetBackgroundColor</a>
</td>
<td align="left" width="63%">
Retrieves the background color used by the Line 21 Decoder filter for overlay.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bfd1c33d-27e0-4923-9c80-5d1bedb4fd25">GetCurrentService</a>
</td>
<td align="left" width="63%">
Retrieves the current closed captioning service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f0fc2c3-cc98-4646-ada0-57d74c6b5dd9">GetDecoderLevel</a>
</td>
<td align="left" width="63%">
Retrieves the closed-captioned decoder level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/817a47d6-39c4-4186-81d0-ad822814f0ee">GetDrawBackgroundMode</a>
</td>
<td align="left" width="63%">
Indicates whether the filter draws the captions on a transparent background or an opaque background.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d1ded3c-fdeb-4e02-92ee-d0986711c335">GetOutputFormat</a>
</td>
<td align="left" width="63%">
Retrieves the Line 21 Decoder filter's output format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ab65d23-816d-4c6f-a0bc-b3334babdc23">GetRedrawAlways</a>
</td>
<td align="left" width="63%">
Indicates whether the filter redraws the entire output bitmap for each sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c88d2328-0338-4c0b-b719-8501bcbb8a69">GetServiceState</a>
</td>
<td align="left" width="63%">
Indicates whether closed captioning is on or off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a69bb0d0-5afb-420f-a97c-071dc472e1d2">SetBackgroundColor</a>
</td>
<td align="left" width="63%">
Sets the background color that the filter uses for overlay.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f1945c3-644d-4e72-b2b7-a7e068b59d96">SetCurrentService</a>
</td>
<td align="left" width="63%">
Sets the closed captioning service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56301cc2-8f27-4530-bb6e-9909eb5bb390">SetDrawBackgroundMode</a>
</td>
<td align="left" width="63%">
Specifies whether the filter draws the captions on a transparent background or an opaque background.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72d63092-8ac6-42c5-a0da-6c64f3a127c5">SetOutputFormat</a>
</td>
<td align="left" width="63%">
Sets the filter's output format. (Not implemented)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20f2e95a-8362-457d-b562-f7263e698551">SetRedrawAlways</a>
</td>
<td align="left" width="63%">
Specifies whether the filter redraws the entire output bitmap for each sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/009e7d14-5946-42f0-8832-7fd8c565a877">SetServiceState</a>
</td>
<td align="left" width="63%">
Enables or disables closed captions.

</td>
</tr>
</table> 

