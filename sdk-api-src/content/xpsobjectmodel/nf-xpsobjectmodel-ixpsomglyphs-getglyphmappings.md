---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.GetGlyphMappings
title: IXpsOMGlyphs::GetGlyphMappings (xpsobjectmodel.h)
description: Gets an array of XPS_GLYPH_MAPPING structures that describe how to map UTF-16 scalar values to entries in the array of XPS_GLYPH_INDEX structures, which is returned by GetGlyphIndices. (IXpsOMGlyphs.GetGlyphMappings)
helpviewer_keywords: ["GetGlyphMappings","GetGlyphMappings method [XPS Documents and Packaging]","GetGlyphMappings method [XPS Documents and Packaging]","IXpsOMGlyphs interface","IXpsOMGlyphs interface [XPS Documents and Packaging]","GetGlyphMappings method","IXpsOMGlyphs.GetGlyphMappings","IXpsOMGlyphs::GetGlyphMappings","xps.ixpsomglyphs_getglyphmappings","xpsobjectmodel/IXpsOMGlyphs::GetGlyphMappings"]
old-location: xps\ixpsomglyphs_getglyphmappings.htm
tech.root: xps
ms.assetid: c7cf4352-f08a-43cb-a063-5d369017a887
ms.date: 12/05/2018
ms.keywords: GetGlyphMappings, GetGlyphMappings method [XPS Documents and Packaging], GetGlyphMappings method [XPS Documents and Packaging],IXpsOMGlyphs interface, IXpsOMGlyphs interface [XPS Documents and Packaging],GetGlyphMappings method, IXpsOMGlyphs.GetGlyphMappings, IXpsOMGlyphs::GetGlyphMappings, xps.ixpsomglyphs_getglyphmappings, xpsobjectmodel/IXpsOMGlyphs::GetGlyphMappings
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
 - IXpsOMGlyphs::GetGlyphMappings
 - xpsobjectmodel/IXpsOMGlyphs::GetGlyphMappings
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
 - IXpsOMGlyphs.GetGlyphMappings
---

# IXpsOMGlyphs::GetGlyphMappings


## -description

Gets an array of <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_mapping">XPS_GLYPH_MAPPING</a> structures that describe how to map UTF-16 scalar values to entries in the array of <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_index">XPS_GLYPH_INDEX</a> structures, which is returned by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-getglyphindices">GetGlyphIndices</a>.

## -parameters

### -param glyphMappingCount [in, out]

The number of <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_mapping">XPS_GLYPH_MAPPING</a> structures that will fit in the array referenced by <i>glyphMappings</i>. When the method returns, <i>glyphMappingCount</i> contains the number of values returned in the array referenced by <i>glyphMappings</i>.

### -param glyphMappings [in, out]

An array of <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_mapping">XPS_GLYPH_MAPPING</a> structures that contain the glyph mapping values.

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
<i>glyphMappingCount</i>, <i>glyphMappings</i>, or both are <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
<i>glyphMappings</i> is not large enough to receive the glyph index data. <i>glyphMappingCount</i> contains the required number of elements.

</td>
</tr>
</table>

## -remarks

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-getglyphmappingcount">GetGlyphMappingCount</a> gets the number of glyph mappings.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-getglyphmappingcount">GetGlyphMappingCount</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_index">XPS_GLYPH_INDEX</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_mapping">XPS_GLYPH_MAPPING</a>
