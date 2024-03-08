---
UID: NF:xpsobjectmodel.IXpsOMGlyphsEditor.SetGlyphIndices
title: IXpsOMGlyphsEditor::SetGlyphIndices (xpsobjectmodel.h)
description: Sets an XPS_GLYPH_INDEX structure array that describes which glyph indices are to be used in the font.
helpviewer_keywords: ["IXpsOMGlyphsEditor interface [XPS Documents and Packaging]","SetGlyphIndices method","IXpsOMGlyphsEditor.SetGlyphIndices","IXpsOMGlyphsEditor::SetGlyphIndices","SetGlyphIndices","SetGlyphIndices method [XPS Documents and Packaging]","SetGlyphIndices method [XPS Documents and Packaging]","IXpsOMGlyphsEditor interface","xps.ixpsomglyphseditor_setglyphindices","xpsobjectmodel/IXpsOMGlyphsEditor::SetGlyphIndices"]
old-location: xps\ixpsomglyphseditor_setglyphindices.htm
tech.root: xps
ms.assetid: a95aaf48-9a55-4a62-b8e1-7b8d077f1b2e
ms.date: 12/05/2018
ms.keywords: IXpsOMGlyphsEditor interface [XPS Documents and Packaging],SetGlyphIndices method, IXpsOMGlyphsEditor.SetGlyphIndices, IXpsOMGlyphsEditor::SetGlyphIndices, SetGlyphIndices, SetGlyphIndices method [XPS Documents and Packaging], SetGlyphIndices method [XPS Documents and Packaging],IXpsOMGlyphsEditor interface, xps.ixpsomglyphseditor_setglyphindices, xpsobjectmodel/IXpsOMGlyphsEditor::SetGlyphIndices
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
 - IXpsOMGlyphsEditor::SetGlyphIndices
 - xpsobjectmodel/IXpsOMGlyphsEditor::SetGlyphIndices
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
 - IXpsOMGlyphsEditor.SetGlyphIndices
---

# IXpsOMGlyphsEditor::SetGlyphIndices


## -description

Sets an <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_index">XPS_GLYPH_INDEX</a> structure array that describes which glyph indices are  to be used in the font.

## -parameters

### -param indexCount [in]

The number of <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_index">XPS_GLYPH_INDEX</a> structures in the array that is referenced by <i>glyphIndices</i>. The value of 0 clears the property.

### -param glyphIndices [in]

An array of <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_index">XPS_GLYPH_INDEX</a> structures that contain the glyph indices. If <i>indexCount</i> is 0, this parameter is ignored.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <b>index</b> field of one or more <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_index">XPS_GLYPH_INDEX</a> structures has a value that  is not valid. The <b>index</b> field must have a value between and including –1 and 65535 (0xFFFF).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>glyphIndices</i> is <b>NULL</b> and <i>indexCount</i> is greater than 0.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_INVALID_FLOAT</b></dt>
</dl>
</td>
<td width="60%">
The <b>advanceWidth</b>, <b>horizontalOffset</b>, or <b>verticalOffset</b>  field of one or more <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_index">XPS_GLYPH_INDEX</a> structures has a floating-point value that is not valid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_NEGATIVE_FLOAT</b></dt>
</dl>
</td>
<td width="60%">
The <b>advanceWidth</b> field of one or more <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_index">XPS_GLYPH_INDEX</a> structures has a value that  is not valid. The <b>advanceWidth</b> field must have a non-negative value or a value of  exactly –1.0; a negative value that is not exactly –1.0 is not valid.

</td>
</tr>
</table>

## -remarks

  The glyph indices that are passed in <i>glyphIndices</i> override the default cmap mapping from the <b>UnicodeString</b> property to the glyph index. Each <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_index">XPS_GLYPH_INDEX</a> structure also has advance width and vertical and horizontal offset information.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor">IXpsOMGlyphsEditor</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_index">XPS_GLYPH_INDEX</a>