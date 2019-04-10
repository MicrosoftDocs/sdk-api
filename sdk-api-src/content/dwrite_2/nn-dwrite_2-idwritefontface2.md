---
UID: NN:dwrite_2.IDWriteFontFace2
title: IDWriteFontFace2 (dwrite_2.h)
author: windows-sdk-content
description: Represents an absolute reference to a font face.
old-location: directwrite\idwritefontface2.htm
tech.root: DirectWrite
ms.assetid: D74F6472-CEEC-4DF5-83C8-0D65923C8028
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteFontFace1, IDWriteFontFace1 interface [Direct Write], IDWriteFontFace1 interface [Direct Write],described, IDWriteFontFace2, directwrite.idwritefontface2, dwrite_2/IDWriteFontFace2
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
 - IDWriteFontFace1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontFace2 interface


## -description


Represents an absolute reference to a font face.  

This interface contains the font face type, appropriate file references, and face identification data.  

You obtain various font data like metrics, names, and glyph outlines from the <b>IDWriteFontFace2</b> interface.

This interface adds the ability to check if a color rendering path is potentially necessary.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFontFace1</b> interface inherits from <a href="https://msdn.microsoft.com/1DB7156F-0578-46A0-8C96-E1E34FF4E49E">IDWriteFontFace1</a>. <b>IDWriteFontFace2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFontFace1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99BB9C72-99B1-427C-B740-55A138189459">GetColorPaletteCount</a>
</td>
<td align="left" width="63%">
Gets the number of color palettes defined by the font. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4678E96C-A5E6-4294-8927-B71F55149342">GetPaletteEntries</a>
</td>
<td align="left" width="63%">
Gets color values from the font's color palette.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7DFB0D3F-18E8-44AA-A7DA-4B9D971D3C35">GetPaletteEntryCount</a>
</td>
<td align="left" width="63%">
Get the number of entries in each color palette.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/351E9A18-CD14-421F-931F-7F25FBCA6B83">GetRecommendedRenderingMode</a>
</td>
<td align="left" width="63%">
Determines the recommended text rendering and grid-fit mode to be used based on the font, size, world transform, and measuring mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77D509D4-355F-4D2F-B71B-D9DF75E19362">IsColorFont</a>
</td>
<td align="left" width="63%">
Allows you to determine if a color rendering path is potentially necessary.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1DB7156F-0578-46A0-8C96-E1E34FF4E49E">IDWriteFontFace1</a>
 

 

