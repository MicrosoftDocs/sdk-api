---
UID: NN:dwrite_2.IDWriteTextRenderer1
title: IDWriteTextRenderer1
author: windows-sdk-content
description: Represents a set of application-defined callbacks that perform rendering of text, inline objects, and decorations such as underlines.
old-location: directwrite\idwritetextrenderer1.htm
tech.root: DirectWrite
ms.assetid: A8C39C54-AF98-4A27-9BCF-9C132F4CD3B1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDWriteTextRenderer1, IDWriteTextRenderer1 interface [Direct Write], IDWriteTextRenderer1 interface [Direct Write],described, directwrite.idwritetextrenderer1, dwrite_2/IDWriteTextRenderer1
ms.topic: interface
req.header: dwrite_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - IDWriteTextRenderer1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextRenderer1 interface


## -description


 Represents a set of application-defined callbacks that perform rendering of text, inline objects, and decorations such as underlines. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteTextRenderer1</b> interface inherits from <a href="https://msdn.microsoft.com/a2ac70c8-e33b-46f1-b53b-1ab07555f109">IDWriteTextRenderer</a>. <b>IDWriteTextRenderer1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteTextRenderer1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5f24a23-fb81-90f3-85de-55d8599a18d3">DrawGlyphRun</a>
</td>
<td align="left" width="63%">
 IDWriteTextLayout::<a href="https://msdn.microsoft.com/cbaa3341-e43a-4d3f-89c7-dda758a63e7d">Draw</a> calls this function to instruct the client to
     render a run of glyphs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1115e215-d04e-28db-c196-7d693ca91044">DrawInlineObject</a>
</td>
<td align="left" width="63%">
 IDWriteTextLayout::<a href="https://msdn.microsoft.com/cbaa3341-e43a-4d3f-89c7-dda758a63e7d">Draw</a> calls this application callback when it needs to
     draw an inline object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8800a536-9477-89c5-c48d-3f4bdf1ca1a5">DrawStrikethrough</a>
</td>
<td align="left" width="63%">
 IDWriteTextLayout::<a href="https://msdn.microsoft.com/cbaa3341-e43a-4d3f-89c7-dda758a63e7d">Draw</a> calls this function to instruct the client to draw
     a strikethrough.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c2c5ea68-c1d0-b467-a9a7-cb3a457ff68d">DrawUnderline</a>
</td>
<td align="left" width="63%">
 IDWriteTextLayout::<a href="https://msdn.microsoft.com/cbaa3341-e43a-4d3f-89c7-dda758a63e7d">Draw</a> calls this function to instruct the client to draw
     an underline.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/a2ac70c8-e33b-46f1-b53b-1ab07555f109">IDWriteTextRenderer</a>
 

 

