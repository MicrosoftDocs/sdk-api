---
UID: NN:dwrite.IDWriteInlineObject
title: IDWriteInlineObject
author: windows-sdk-content
description: Wraps an application-defined inline graphic, allowing DWrite to query metrics as if the graphic were a glyph inline with the text.
old-location: directwrite\IDWriteInlineObject.htm
tech.root: DirectWrite
ms.assetid: cf915458-acbc-4a37-be5c-b1337153f386
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IDWriteInlineObject, IDWriteInlineObject interface [Direct Write], IDWriteInlineObject interface [Direct Write],described, directwrite.IDWriteInlineObject, dwrite/IDWriteInlineObject
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
 - IDWriteInlineObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteInlineObject interface


## -description


 Wraps an application-defined inline graphic, allowing DWrite to query metrics as if the graphic were a glyph inline with the text.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteInlineObject</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteInlineObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteInlineObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cbaa3341-e43a-4d3f-89c7-dda758a63e7d">Draw</a>
</td>
<td align="left" width="63%">
 The application implemented rendering callback (<a href="https://msdn.microsoft.com/ea1c4cd0-d9b5-46af-b53e-a2d8fc442acf">IDWriteTextRenderer::DrawInlineObject</a>)
     can use this to draw the inline object without needing to cast or query the object
     type. The text layout does not call this method directly.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c46614a6-2b48-46db-a1e2-73383d6386c5">GetBreakConditions</a>
</td>
<td align="left" width="63%">
 Layout uses this to determine the line-breaking behavior of the inline object
     among the text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/809a4e29-0423-40b2-9d40-105d30574fa1">GetMetrics</a>
</td>
<td align="left" width="63%">

<a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a> calls this callback function to get the measurement of the inline object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3b3e9f0-ee35-4117-9a62-a975c03b5ca9">GetOverhangMetrics</a>
</td>
<td align="left" width="63%">

<a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a> calls this callback function to get the visible extents (in DIPs) of the inline object. In the case of a simple bitmap, with no padding and no overhang, all the overhangs will
    simply be zeroes.

</td>
</tr>
</table> 

