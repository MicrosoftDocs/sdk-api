---
UID: NN:dwrite_2.IDWriteTextFormat1
title: IDWriteTextFormat1 (dwrite_2.h)
description: Describes the font and paragraph properties used to format text, and it describes locale information.
old-location: directwrite\idwritetextformat1.htm
tech.root: DirectWrite
ms.assetid: 15295A17-E542-4071-AE38-02014A1235D5
ms.date: 12/05/2018
ms.keywords: IDWriteTextFormat1, IDWriteTextFormat1 interface [Direct Write], IDWriteTextFormat1 interface [Direct Write],described, directwrite.idwritetextformat1, dwrite_2/IDWriteTextFormat1
f1_keywords:
- dwrite_2/IDWriteTextFormat1
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
- IDWriteTextFormat1
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextFormat1 interface


## -description


Describes the font and paragraph properties used to format text, and it describes locale information.
        This interface has all the same methods as <a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a> and  adds the ability for you to apply an explicit orientation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteTextFormat1</b> interface inherits from <a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a>. <b>IDWriteTextFormat1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteTextFormat1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getfontfallback">GetFontFallback</a>
</td>
<td align="left" width="63%">
Gets the current fallback. If none was ever set since creating the layout, it will be nullptr.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getlastlinewrapping">GetLastLineWrapping</a>
</td>
<td align="left" width="63%">
Gets the wrapping mode of the last line.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getopticalalignment">GetOpticalAlignment</a>
</td>
<td align="left" width="63%">
Gets the optical margin alignment for the text format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getverticalglyphorientation">GetVerticalGlyphOrientation</a>
</td>
<td align="left" width="63%">
Get the preferred orientation of glyphs when using a vertical reading direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setfontfallback">SetFontFallback</a>
</td>
<td align="left" width="63%">
Applies the custom font fallback onto the layout. If none is set, it uses the default system fallback list.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setlastlinewrapping">SetLastLineWrapping</a>
</td>
<td align="left" width="63%">
Sets the wrapping mode of the last line.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setopticalalignment">SetOpticalAlignment</a>
</td>
<td align="left" width="63%">
Sets the optical margin alignment for the text format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setverticalglyphorientation">SetVerticalGlyphOrientation</a>
</td>
<td align="left" width="63%">
Sets the orientation of a text format.

</td>
</tr>
</table> 


## -see-also




<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a>
 

 

