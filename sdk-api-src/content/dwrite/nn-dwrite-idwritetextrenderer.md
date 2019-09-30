---
UID: NN:dwrite.IDWriteTextRenderer
title: IDWriteTextRenderer (dwrite.h)
author: windows-sdk-content
description: Represents a set of application-defined callbacks that perform rendering of text, inline objects, and decorations such as underlines.
old-location: directwrite\IDWriteTextRenderer.htm
tech.root: DirectWrite
ms.assetid: a2ac70c8-e33b-46f1-b53b-1ab07555f109
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteTextRenderer, IDWriteTextRenderer interface [Direct Write], IDWriteTextRenderer interface [Direct Write],described, directwrite.IDWriteTextRenderer, dwrite/IDWriteTextRenderer
ms.topic: interface
f1_keywords: 
 - "dwrite/IDWriteTextRenderer"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextRenderer interface


## -description


 Represents a set of application-defined callbacks that perform rendering of text, inline objects, and decorations such as underlines.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteTextRenderer</b> interface inherits from <a href="/windows/win32/api/dwrite/nn-dwrite-idwritepixelsnapping">IDWritePixelSnapping</a>. <b>IDWriteTextRenderer</b> also has these types of members:
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
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun">DrawGlyphRun</a>
</td>
<td align="left" width="63%">
 IDWriteTextLayout::<a href="/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw">Draw</a> calls this function to instruct the client to
     render a run of glyphs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject">DrawInlineObject</a>
</td>
<td align="left" width="63%">
 IDWriteTextLayout::<a href="/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw">Draw</a> calls this application callback when it needs to
     draw an inline object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough">DrawStrikethrough</a>
</td>
<td align="left" width="63%">
 IDWriteTextLayout::<a href="/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw">Draw</a> calls this function to instruct the client to draw
     a strikethrough.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline">DrawUnderline</a>
</td>
<td align="left" width="63%">
 IDWriteTextLayout::<a href="/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw">Draw</a> calls this function to instruct the client to draw
     an underline.

</td>
</tr>
</table> 


## -see-also




<a href="/windows/win32/api/dwrite/nn-dwrite-idwritepixelsnapping">IDWritePixelSnapping</a>
 

 

