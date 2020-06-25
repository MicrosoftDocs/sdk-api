---
UID: NN:dwrite_2.IDWriteTextLayout2
title: IDWriteTextLayout2 (dwrite_2.h)
description: Represents a block of text after it has been fully analyzed and formatted.
helpviewer_keywords: ["IDWriteTextLayout2","IDWriteTextLayout2 interface [Direct Write]","IDWriteTextLayout2 interface [Direct Write]","described","directwrite.idwritetextlayout2","dwrite_2/IDWriteTextLayout2"]
old-location: directwrite\idwritetextlayout2.htm
tech.root: DirectWrite
ms.assetid: 034D795B-016A-401E-AD75-D5B0D1E87806
ms.date: 12/05/2018
ms.keywords: IDWriteTextLayout2, IDWriteTextLayout2 interface [Direct Write], IDWriteTextLayout2 interface [Direct Write],described, directwrite.idwritetextlayout2, dwrite_2/IDWriteTextLayout2
f1_keywords:
- dwrite_2/IDWriteTextLayout2
dev_langs:
- c++
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
- IDWriteTextLayout2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextLayout2 interface


## -description


Represents a block of text after it has been fully analyzed and formatted.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteTextLayout2</b> interface inherits from <a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1">IDWriteTextLayout1</a>. <b>IDWriteTextLayout2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteTextLayout2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getfontfallback">GetFontFallback</a>
</td>
<td align="left" width="63%">
Get the current font fallback object.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getlastlinewrapping">GetLastLineWrapping</a>
</td>
<td align="left" width="63%">
Get whether or not the last word on the last line is wrapped.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/DirectWrite/idwritetextlayout2-getmetrics">GetMetrics</a>
</td>
<td align="left" width="63%">
 Retrieves overall metrics for the formatted string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getopticalalignment">GetOpticalAlignment</a>
</td>
<td align="left" width="63%">
Get how the glyphs align to the edges the margin.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getverticalglyphorientation">GetVerticalGlyphOrientation</a>
</td>
<td align="left" width="63%">
Get the preferred orientation of glyphs when using a vertical reading direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setfontfallback">SetFontFallback</a>
</td>
<td align="left" width="63%">
Apply a custom font fallback onto layout.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setlastlinewrapping">SetLastLineWrapping</a>
</td>
<td align="left" width="63%">
Set whether or not the last word on the last line is wrapped. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setopticalalignment">SetOpticalAlignment</a>
</td>
<td align="left" width="63%">
Set how the glyphs align to the edges the margin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setverticalglyphorientation">SetVerticalGlyphOrientation</a>
</td>
<td align="left" width="63%">
Set the preferred orientation of glyphs when using a vertical reading direction.

</td>
</tr>
</table> 


## -see-also




<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1">IDWriteTextLayout1</a>
 

 

