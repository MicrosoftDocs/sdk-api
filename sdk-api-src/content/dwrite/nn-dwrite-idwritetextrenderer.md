---
UID: NN:dwrite.IDWriteTextRenderer
title: IDWriteTextRenderer
author: windows-sdk-content
description: Represents a set of application-defined callbacks that perform rendering of text, inline objects, and decorations such as underlines.
old-location: directwrite\IDWriteTextRenderer.htm
tech.root: DirectWrite
ms.assetid: a2ac70c8-e33b-46f1-b53b-1ab07555f109
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IDWriteTextRenderer, IDWriteTextRenderer interface [Direct Write], IDWriteTextRenderer interface [Direct Write],described, directwrite.IDWriteTextRenderer, dwrite/IDWriteTextRenderer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteTextRenderer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextRenderer interface


## -description


 Represents a set of application-defined callbacks that perform rendering of text, inline objects, and decorations such as underlines.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteTextRenderer</b> interface inherits from <a href="https://msdn.microsoft.com/b1b1eeb7-934f-42f4-ac01-50973a94996e">IDWritePixelSnapping</a>. <b>IDWriteTextRenderer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteTextRenderer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95a0044c-dffd-4c6a-a6eb-2f87b02ef89a">DrawGlyphRun</a>
</td>
<td align="left" width="63%">
 IDWriteTextLayout::<a href="https://msdn.microsoft.com/cbaa3341-e43a-4d3f-89c7-dda758a63e7d">Draw</a> calls this function to instruct the client to
     render a run of glyphs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea1c4cd0-d9b5-46af-b53e-a2d8fc442acf">DrawInlineObject</a>
</td>
<td align="left" width="63%">
 IDWriteTextLayout::<a href="https://msdn.microsoft.com/cbaa3341-e43a-4d3f-89c7-dda758a63e7d">Draw</a> calls this application callback when it needs to
     draw an inline object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7888c99-ff7c-4e14-b0a6-4726c9228226">DrawStrikethrough</a>
</td>
<td align="left" width="63%">
 IDWriteTextLayout::<a href="https://msdn.microsoft.com/cbaa3341-e43a-4d3f-89c7-dda758a63e7d">Draw</a> calls this function to instruct the client to draw
     a strikethrough.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23395b2a-f53c-4697-87f1-15c65224b1f3">DrawUnderline</a>
</td>
<td align="left" width="63%">
 IDWriteTextLayout::<a href="https://msdn.microsoft.com/cbaa3341-e43a-4d3f-89c7-dda758a63e7d">Draw</a> calls this function to instruct the client to draw
     an underline.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b1b1eeb7-934f-42f4-ac01-50973a94996e">IDWritePixelSnapping</a>
 

 

