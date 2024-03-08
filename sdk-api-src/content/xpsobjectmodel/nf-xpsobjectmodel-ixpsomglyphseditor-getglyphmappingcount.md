---
UID: NF:xpsobjectmodel.IXpsOMGlyphsEditor.GetGlyphMappingCount
title: IXpsOMGlyphsEditor::GetGlyphMappingCount (xpsobjectmodel.h)
description: Gets the number of glyph mappings. (IXpsOMGlyphsEditor.GetGlyphMappingCount)
helpviewer_keywords: ["GetGlyphMappingCount","GetGlyphMappingCount method [XPS Documents and Packaging]","GetGlyphMappingCount method [XPS Documents and Packaging]","IXpsOMGlyphsEditor interface","IXpsOMGlyphsEditor interface [XPS Documents and Packaging]","GetGlyphMappingCount method","IXpsOMGlyphsEditor.GetGlyphMappingCount","IXpsOMGlyphsEditor::GetGlyphMappingCount","xps.ixpsomglyphseditor_getglyphmappingcount","xpsobjectmodel/IXpsOMGlyphsEditor::GetGlyphMappingCount"]
old-location: xps\ixpsomglyphseditor_getglyphmappingcount.htm
tech.root: xps
ms.assetid: 06aa2546-c1d1-47d6-9d3d-94d13310e42b
ms.date: 12/05/2018
ms.keywords: GetGlyphMappingCount, GetGlyphMappingCount method [XPS Documents and Packaging], GetGlyphMappingCount method [XPS Documents and Packaging],IXpsOMGlyphsEditor interface, IXpsOMGlyphsEditor interface [XPS Documents and Packaging],GetGlyphMappingCount method, IXpsOMGlyphsEditor.GetGlyphMappingCount, IXpsOMGlyphsEditor::GetGlyphMappingCount, xps.ixpsomglyphseditor_getglyphmappingcount, xpsobjectmodel/IXpsOMGlyphsEditor::GetGlyphMappingCount
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
 - IXpsOMGlyphsEditor::GetGlyphMappingCount
 - xpsobjectmodel/IXpsOMGlyphsEditor::GetGlyphMappingCount
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
 - IXpsOMGlyphsEditor.GetGlyphMappingCount
---

# IXpsOMGlyphsEditor::GetGlyphMappingCount


## -description

Gets the number of glyph mappings.

## -parameters

### -param glyphMappingCount [out, retval]

The number of glyph mappings.

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
<i>glyphMappingCount</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

To get the glyph mappings, call <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphseditor-getglyphmappings">GetGlyphMappings</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor">IXpsOMGlyphsEditor</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
