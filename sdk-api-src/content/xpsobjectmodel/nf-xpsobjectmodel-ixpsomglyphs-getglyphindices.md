---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.GetGlyphIndices
title: IXpsOMGlyphs::GetGlyphIndices (xpsobjectmodel.h)
description: Gets an array of XPS_GLYPH_INDEX structures that describe the specific glyph indices in the font. (IXpsOMGlyphs.GetGlyphIndices)
helpviewer_keywords: ["GetGlyphIndices","GetGlyphIndices method [XPS Documents and Packaging]","GetGlyphIndices method [XPS Documents and Packaging]","IXpsOMGlyphs interface","IXpsOMGlyphs interface [XPS Documents and Packaging]","GetGlyphIndices method","IXpsOMGlyphs.GetGlyphIndices","IXpsOMGlyphs::GetGlyphIndices","xps.ixpsomglyphs_getglyphindices","xpsobjectmodel/IXpsOMGlyphs::GetGlyphIndices"]
old-location: xps\ixpsomglyphs_getglyphindices.htm
tech.root: xps
ms.assetid: 6698ae0b-3525-4612-8234-8ba4dd2870a0
ms.date: 12/05/2018
ms.keywords: GetGlyphIndices, GetGlyphIndices method [XPS Documents and Packaging], GetGlyphIndices method [XPS Documents and Packaging],IXpsOMGlyphs interface, IXpsOMGlyphs interface [XPS Documents and Packaging],GetGlyphIndices method, IXpsOMGlyphs.GetGlyphIndices, IXpsOMGlyphs::GetGlyphIndices, xps.ixpsomglyphs_getglyphindices, xpsobjectmodel/IXpsOMGlyphs::GetGlyphIndices
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsOMGlyphs::GetGlyphIndices
 - xpsobjectmodel/IXpsOMGlyphs::GetGlyphIndices
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMGlyphs.GetGlyphIndices
---

# IXpsOMGlyphs::GetGlyphIndices


## -description

Gets an array of <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_index">XPS_GLYPH_INDEX</a> structures that describe the specific glyph indices in the font.

## -parameters

### -param indexCount [in, out]

The number of <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_index">XPS_GLYPH_INDEX</a> structures that will fit in  the array that is referenced by <i>glyphIndices</i>. When the method returns, <i>indexCount</i>  will contain the number of <b>XPS_GLYPH_INDEX</b> structures that are returned in the array referenced by <i>glyphIndices</i>.

### -param glyphIndices [in, out]

The address of an array of <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_index">XPS_GLYPH_INDEX</a> structures that receive the glyph indices.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>indexCount</i> or <i>glyphIndices</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
<i>glyphIndices</i> is not large enough to receive the glyph index data. <i>indexCount</i> contains the required number of elements.

</td>
</tr>
</table>

## -remarks

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-getglyphindexcount">GetGlyphIndexCount</a> gets the number of elements in the glyph index array.

The glyph indices override the default <b>cmap</b> mapping from the <b>UnicodeString</b> to the glyph index. The <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_index">XPS_GLYPH_INDEX</a> structure also contains advance width as well as vertical and horizontal offset information.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-getglyphindexcount">GetGlyphIndexCount</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_index">XPS_GLYPH_INDEX</a>
