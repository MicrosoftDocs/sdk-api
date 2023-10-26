---
UID: NF:xpsobjectmodel.IXpsOMGlyphsEditor.GetBidiLevel
title: IXpsOMGlyphsEditor::GetBidiLevel (xpsobjectmodel.h)
description: Gets the bidirectional text level of the parent IXpsOMGlyphs interface.
helpviewer_keywords: ["GetBidiLevel","GetBidiLevel method [XPS Documents and Packaging]","GetBidiLevel method [XPS Documents and Packaging]","IXpsOMGlyphsEditor interface","IXpsOMGlyphsEditor interface [XPS Documents and Packaging]","GetBidiLevel method","IXpsOMGlyphsEditor.GetBidiLevel","IXpsOMGlyphsEditor::GetBidiLevel","xps.ixpsomglyphseditor_getbidilevel","xpsobjectmodel/IXpsOMGlyphsEditor::GetBidiLevel"]
old-location: xps\ixpsomglyphseditor_getbidilevel.htm
tech.root: xps
ms.assetid: 86021e6e-5a91-44f5-814d-602705b97fb2
ms.date: 12/05/2018
ms.keywords: GetBidiLevel, GetBidiLevel method [XPS Documents and Packaging], GetBidiLevel method [XPS Documents and Packaging],IXpsOMGlyphsEditor interface, IXpsOMGlyphsEditor interface [XPS Documents and Packaging],GetBidiLevel method, IXpsOMGlyphsEditor.GetBidiLevel, IXpsOMGlyphsEditor::GetBidiLevel, xps.ixpsomglyphseditor_getbidilevel, xpsobjectmodel/IXpsOMGlyphsEditor::GetBidiLevel
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
 - IXpsOMGlyphsEditor::GetBidiLevel
 - xpsobjectmodel/IXpsOMGlyphsEditor::GetBidiLevel
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
 - IXpsOMGlyphsEditor.GetBidiLevel
---

# IXpsOMGlyphsEditor::GetBidiLevel


## -description

Gets the bidirectional text level  of the parent  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a> interface.

## -parameters

### -param bidiLevel [out, retval]

The bidirectional text level.

Range: 0–61

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
bidiLevel is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The <b>BidiLevel</b> property specifies the bidirectional nesting level of the Unicode algorithm. Even values imply the left-to-right layout and odd values the right-to-left layout. Right-to-left layout places the run origin at the right side of the first glyph.  Advance widths that are positive will move to the left, allowing subsequent glyphs to be placed to the left of the previous glyph.

The range of allowed values for this property is  between 0 and  61, inclusive, and the default value is 0.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor">IXpsOMGlyphsEditor</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>