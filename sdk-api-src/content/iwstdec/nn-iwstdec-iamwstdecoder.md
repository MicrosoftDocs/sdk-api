---
UID: NN:iwstdec.IAMWstDecoder
title: IAMWstDecoder
author: windows-sdk-content
description: The IAMWstDecoder interface sets and retrieves information about World Standard Teletext (WST). The WST Decoder filter implements this interface.
old-location: dshow\iamwstdecoder.htm
old-project: DirectShow
ms.assetid: f2f5a459-14de-4be1-909c-3c23e4cfd737
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IAMWstDecoder, IAMWstDecoder interface [DirectShow], IAMWstDecoder interface [DirectShow],described, IAMWstDecoderInterface, dshow.iamwstdecoder, iwstdec/IAMWstDecoder
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: iwstdec.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: AM_WST_STYLE, *PAM_WST_STYLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMWstDecoder
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IAMWstDecoder interface


## -description



The <code>IAMWstDecoder</code> interface sets and retrieves information about World Standard Teletext (WST). The <a href="https://msdn.microsoft.com/2d33ae3f-565d-4e69-8fb0-117ff582a4d0">WST Decoder</a> filter implements this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMWstDecoder</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMWstDecoder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMWstDecoder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6251c9fa-1149-47ac-b776-7d10d153dde5">GetAnswerMode</a>
</td>
<td align="left" width="63%">
Retrieves whether hidden text is exposed or not.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1661f2cd-8e6c-4e55-b5fd-995ef2962cb7">GetBackgroundColor</a>
</td>
<td align="left" width="63%">
Retrieves the current physical color used in color keying the background for overlay mixing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4e52723-27ad-487a-a547-7ad7ade6f099">GetCurrentPage</a>
</td>
<td align="left" width="63%">
Retrieves the current WST page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d16b3501-efee-48e6-8d5d-d76f206d77ed">GetCurrentService</a>
</td>
<td align="left" width="63%">
Retrieves the current WST service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/629ee71d-7d79-4fa9-b169-3b5328659435">GetDecoderLevel</a>
</td>
<td align="left" width="63%">
Retrieves the WST decoder level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5bf3a83-5f74-4ef1-81b6-6c99e3832725">GetDrawBackgroundMode</a>
</td>
<td align="left" width="63%">
Determines whether the caption text background is opaque or transparent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db09b2a2-7f92-421a-8582-4ed648563119">GetHoldPage</a>
</td>
<td align="left" width="63%">
Determines whether the current WST page is held by the WST decoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63ef7dbe-138b-442a-bf54-1f409c969418">GetOutputFormat</a>
</td>
<td align="left" width="63%">
Retrieves the current output video format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4035bd0-9a86-4deb-b4eb-4aa5b4b4ff35">GetRedrawAlways</a>
</td>
<td align="left" width="63%">
Retrieves whether the whole output bitmap should be redrawn for each sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a927341-6ff4-41f5-918b-ea5b9e1ebe9a">GetServiceState</a>
</td>
<td align="left" width="63%">
Retrieves whether closed captioning is on or off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d26b22d2-2c88-4347-80fb-aca8abae50ab">SetAnswerMode</a>
</td>
<td align="left" width="63%">
Assigns whether hidden text is exposed or not.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d65726aa-a826-41d4-95f3-40c86d7b9347">SetBackgroundColor</a>
</td>
<td align="left" width="63%">
Assigns the current physical color used in color keying the background for overlay mixing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84f8854d-77a7-4ae3-9fec-c4d6fce7eead">SetCurrentPage</a>
</td>
<td align="left" width="63%">
Assigns the current WST page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d237d3dc-b3c9-44b2-9277-798c4830b361">SetDrawBackgroundMode</a>
</td>
<td align="left" width="63%">
Assigns the caption text background to be opaque or transparent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2fea6f52-bae3-4679-a89b-fe85f1232d34">SetHoldPage</a>
</td>
<td align="left" width="63%">
Instructs the WST decoder to hold the current page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92d19d2b-dce5-4dd6-ac96-a39fa48fa1aa">SetOutputFormat</a>
</td>
<td align="left" width="63%">
Assigns an output video format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4663a9c0-3d08-4f25-8742-458081536f98">SetRedrawAlways</a>
</td>
<td align="left" width="63%">
Sets whether the whole output bitmap should be redrawn for each sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c65d056e-0f39-4372-9060-37859798cade">SetServiceState</a>
</td>
<td align="left" width="63%">
Sets closed captioning on or off.

</td>
</tr>
</table> 

