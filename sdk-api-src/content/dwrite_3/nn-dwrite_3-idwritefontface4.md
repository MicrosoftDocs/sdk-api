---
UID: NN:dwrite_3.IDWriteFontFace4
title: IDWriteFontFace4 (dwrite_3.h)
author: windows-sdk-content
description: Represents an absolute reference to a font face. It contains font face type, appropriate file references and face identification data. Various font data such as metrics, names and glyph outlines are obtained from IDWriteFontFace.
old-location: directwrite\idwritefontface4.htm
tech.root: DirectWrite
ms.assetid: 08A0E6F3-611B-4C19-835B-1353D4938181
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteFontFace4, IDWriteFontFace4 interface [Direct Write], IDWriteFontFace4 interface [Direct Write],described, directwrite.idwritefontface4, dwrite_3/IDWriteFontFace4
ms.topic: interface
f1_keywords: ["dwrite_3/IDWriteFontFace4"]
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteFontFace4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFontFace4 interface


## -description


Represents an absolute reference to a font face. It contains font face type, appropriate file references and face identification data.
        Various font data such as metrics, names and glyph outlines are obtained from IDWriteFontFace.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFontFace4</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nn-dwrite_3-idwritefontface3">IDWriteFontFace3</a>. <b>IDWriteFontFace4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFontFace4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nf-dwrite_3-idwritefontface4-getglyphimagedata">GetGlyphImageData</a>
</td>
<td align="left" width="63%">
Gets a pointer to the glyph data based on the desired image format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nf-dwrite_3-getglyphimageformats">GetGlyphImageFormats</a>
</td>
<td align="left" width="63%">Overloaded. Gets supported glyph image formats.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nf-dwrite_3-idwritefontface4-releaseglyphimagedata">ReleaseGlyphImageData</a>
</td>
<td align="left" width="63%">
Releases the table data obtained from ReadGlyphData.

</td>
</tr>
</table> 

