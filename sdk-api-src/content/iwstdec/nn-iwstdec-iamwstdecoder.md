---
UID: NN:iwstdec.IAMWstDecoder
title: IAMWstDecoder (iwstdec.h)
author: windows-sdk-content
description: The IAMWstDecoder interface sets and retrieves information about World Standard Teletext (WST). The WST Decoder filter implements this interface.
old-location: dshow\iamwstdecoder.htm
tech.root: DirectShow
ms.assetid: f2f5a459-14de-4be1-909c-3c23e4cfd737
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMWstDecoder, IAMWstDecoder interface [DirectShow], IAMWstDecoder interface [DirectShow],described, IAMWstDecoderInterface, dshow.iamwstdecoder, iwstdec/IAMWstDecoder
ms.topic: interface
req.header: iwstdec.h
req.include-header: 
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://msdn.microsoft.com/en-us/library/Dd376042(v=VS.85).aspx">GetAnswerMode</a>
</td>
<td align="left" width="63%">
Retrieves whether hidden text is exposed or not.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376043(v=VS.85).aspx">GetBackgroundColor</a>
</td>
<td align="left" width="63%">
Retrieves the current physical color used in color keying the background for overlay mixing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376044(v=VS.85).aspx">GetCurrentPage</a>
</td>
<td align="left" width="63%">
Retrieves the current WST page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376045(v=VS.85).aspx">GetCurrentService</a>
</td>
<td align="left" width="63%">
Retrieves the current WST service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376046(v=VS.85).aspx">GetDecoderLevel</a>
</td>
<td align="left" width="63%">
Retrieves the WST decoder level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376047(v=VS.85).aspx">GetDrawBackgroundMode</a>
</td>
<td align="left" width="63%">
Determines whether the caption text background is opaque or transparent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376048(v=VS.85).aspx">GetHoldPage</a>
</td>
<td align="left" width="63%">
Determines whether the current WST page is held by the WST decoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376049(v=VS.85).aspx">GetOutputFormat</a>
</td>
<td align="left" width="63%">
Retrieves the current output video format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376050(v=VS.85).aspx">GetRedrawAlways</a>
</td>
<td align="left" width="63%">
Retrieves whether the whole output bitmap should be redrawn for each sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376051(v=VS.85).aspx">GetServiceState</a>
</td>
<td align="left" width="63%">
Retrieves whether closed captioning is on or off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376052(v=VS.85).aspx">SetAnswerMode</a>
</td>
<td align="left" width="63%">
Assigns whether hidden text is exposed or not.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376053(v=VS.85).aspx">SetBackgroundColor</a>
</td>
<td align="left" width="63%">
Assigns the current physical color used in color keying the background for overlay mixing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376054(v=VS.85).aspx">SetCurrentPage</a>
</td>
<td align="left" width="63%">
Assigns the current WST page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376055(v=VS.85).aspx">SetDrawBackgroundMode</a>
</td>
<td align="left" width="63%">
Assigns the caption text background to be opaque or transparent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376056(v=VS.85).aspx">SetHoldPage</a>
</td>
<td align="left" width="63%">
Instructs the WST decoder to hold the current page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376057(v=VS.85).aspx">SetOutputFormat</a>
</td>
<td align="left" width="63%">
Assigns an output video format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376058(v=VS.85).aspx">SetRedrawAlways</a>
</td>
<td align="left" width="63%">
Sets whether the whole output bitmap should be redrawn for each sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd376059(v=VS.85).aspx">SetServiceState</a>
</td>
<td align="left" width="63%">
Sets closed captioning on or off.

</td>
</tr>
</table> 

