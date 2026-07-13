---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.GetGlyphsEditor
title: IXpsOMGlyphs::GetGlyphsEditor (xpsobjectmodel.h)
description: Gets a pointer to the IXpsOMGlyphsEditor interface that will be used to edit the glyphs in the object.
helpviewer_keywords: ["GetGlyphsEditor","GetGlyphsEditor method [XPS Documents and Packaging]","GetGlyphsEditor method [XPS Documents and Packaging]","IXpsOMGlyphs interface","IXpsOMGlyphs interface [XPS Documents and Packaging]","GetGlyphsEditor method","IXpsOMGlyphs.GetGlyphsEditor","IXpsOMGlyphs::GetGlyphsEditor","xps.ixpsomglyphs_getglyphseditor","xpsobjectmodel/IXpsOMGlyphs::GetGlyphsEditor"]
old-location: xps\ixpsomglyphs_getglyphseditor.htm
tech.root: xps
ms.assetid: 1c641d99-9303-484d-82e0-2d71e2c43561
ms.date: 12/05/2018
ms.keywords: GetGlyphsEditor, GetGlyphsEditor method [XPS Documents and Packaging], GetGlyphsEditor method [XPS Documents and Packaging],IXpsOMGlyphs interface, IXpsOMGlyphs interface [XPS Documents and Packaging],GetGlyphsEditor method, IXpsOMGlyphs.GetGlyphsEditor, IXpsOMGlyphs::GetGlyphsEditor, xps.ixpsomglyphs_getglyphseditor, xpsobjectmodel/IXpsOMGlyphs::GetGlyphsEditor
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
 - IXpsOMGlyphs::GetGlyphsEditor
 - xpsobjectmodel/IXpsOMGlyphs::GetGlyphsEditor
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
 - IXpsOMGlyphs.GetGlyphsEditor
---

# IXpsOMGlyphs::GetGlyphsEditor


## -description

Gets a pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor">IXpsOMGlyphsEditor</a> interface that will be used to edit the glyphs in the object.

## -parameters

### -param editor [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor">IXpsOMGlyphsEditor</a> interface.

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
<i>editor</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

An <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor">IXpsOMGlyphsEditor</a>  interface is required to edit the read-only properties of the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a> interface.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor">IXpsOMGlyphsEditor</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>