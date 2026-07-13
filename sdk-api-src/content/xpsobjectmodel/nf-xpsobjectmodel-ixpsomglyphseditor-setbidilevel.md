---
UID: NF:xpsobjectmodel.IXpsOMGlyphsEditor.SetBidiLevel
title: IXpsOMGlyphsEditor::SetBidiLevel (xpsobjectmodel.h)
description: Sets the level of bidirectional text.
helpviewer_keywords: ["IXpsOMGlyphsEditor interface [XPS Documents and Packaging]","SetBidiLevel method","IXpsOMGlyphsEditor.SetBidiLevel","IXpsOMGlyphsEditor::SetBidiLevel","SetBidiLevel","SetBidiLevel method [XPS Documents and Packaging]","SetBidiLevel method [XPS Documents and Packaging]","IXpsOMGlyphsEditor interface","xps.ixpsomglyphseditor_setbidilevel","xpsobjectmodel/IXpsOMGlyphsEditor::SetBidiLevel"]
old-location: xps\ixpsomglyphseditor_setbidilevel.htm
tech.root: xps
ms.assetid: a8035863-d1ed-4215-add3-6e60cfca7f1c
ms.date: 12/05/2018
ms.keywords: IXpsOMGlyphsEditor interface [XPS Documents and Packaging],SetBidiLevel method, IXpsOMGlyphsEditor.SetBidiLevel, IXpsOMGlyphsEditor::SetBidiLevel, SetBidiLevel, SetBidiLevel method [XPS Documents and Packaging], SetBidiLevel method [XPS Documents and Packaging],IXpsOMGlyphsEditor interface, xps.ixpsomglyphseditor_setbidilevel, xpsobjectmodel/IXpsOMGlyphsEditor::SetBidiLevel
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
 - IXpsOMGlyphsEditor::SetBidiLevel
 - xpsobjectmodel/IXpsOMGlyphsEditor::SetBidiLevel
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
 - IXpsOMGlyphsEditor.SetBidiLevel
---

# IXpsOMGlyphsEditor::SetBidiLevel


## -description

Sets the level of bidirectional text.

## -parameters

### -param bidiLevel [in]

The level of bidirectional text.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>bidiLevel</i> is outside of the allowed range. For more information, see the Remarks section.

</td>
</tr>
</table>

## -remarks

The <b>BidiLevel</b> property specifies the bidirectional nesting level of the Unicode algorithm. Even values imply the left-to-right layout and odd values the right-to-left layout. Right-to-left layout places the run origin on the right side of the first glyph. Advance widths  that are positive will move to the left, allowing subsequent glyphs to be placed to the left of the previous glyph.

The range of allowed values for this property is between 0 and 61, inclusive, and the default value is 0.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor">IXpsOMGlyphsEditor</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>