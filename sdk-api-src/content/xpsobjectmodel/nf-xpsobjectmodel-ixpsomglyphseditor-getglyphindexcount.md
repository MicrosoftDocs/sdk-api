---
UID: NF:xpsobjectmodel.IXpsOMGlyphsEditor.GetGlyphIndexCount
title: IXpsOMGlyphsEditor::GetGlyphIndexCount (xpsobjectmodel.h)
description: Gets the number of glyph indices.
helpviewer_keywords: ["GetGlyphIndexCount","GetGlyphIndexCount method [XPS Documents and Packaging]","GetGlyphIndexCount method [XPS Documents and Packaging]","IXpsOMGlyphsEditor interface","IXpsOMGlyphsEditor interface [XPS Documents and Packaging]","GetGlyphIndexCount method","IXpsOMGlyphsEditor.GetGlyphIndexCount","IXpsOMGlyphsEditor::GetGlyphIndexCount","xps.ixpsomglyphseditor_getglyphindexcount","xpsobjectmodel/IXpsOMGlyphsEditor::GetGlyphIndexCount"]
old-location: xps\ixpsomglyphseditor_getglyphindexcount.htm
tech.root: xps
ms.assetid: e7b83f08-e87f-4921-8dbb-f33453c63732
ms.date: 12/05/2018
ms.keywords: GetGlyphIndexCount, GetGlyphIndexCount method [XPS Documents and Packaging], GetGlyphIndexCount method [XPS Documents and Packaging],IXpsOMGlyphsEditor interface, IXpsOMGlyphsEditor interface [XPS Documents and Packaging],GetGlyphIndexCount method, IXpsOMGlyphsEditor.GetGlyphIndexCount, IXpsOMGlyphsEditor::GetGlyphIndexCount, xps.ixpsomglyphseditor_getglyphindexcount, xpsobjectmodel/IXpsOMGlyphsEditor::GetGlyphIndexCount
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
 - IXpsOMGlyphsEditor::GetGlyphIndexCount
 - xpsobjectmodel/IXpsOMGlyphsEditor::GetGlyphIndexCount
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
 - IXpsOMGlyphsEditor.GetGlyphIndexCount
---

# IXpsOMGlyphsEditor::GetGlyphIndexCount


## -description

Gets the number of glyph indices.

## -parameters

### -param indexCount [out, retval]

The glyph index count.

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
<i>indexCount</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

To get the glyph indices, call <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphseditor-getglyphindices">GetGlyphIndices</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor">IXpsOMGlyphsEditor</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>