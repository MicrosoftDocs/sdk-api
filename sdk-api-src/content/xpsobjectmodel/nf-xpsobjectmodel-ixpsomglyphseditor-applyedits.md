---
UID: NF:xpsobjectmodel.IXpsOMGlyphsEditor.ApplyEdits
title: IXpsOMGlyphsEditor::ApplyEdits (xpsobjectmodel.h)
description: Performs cross-property validation and then copies the changes to the parent IXpsOMGlyphs interface.
helpviewer_keywords: ["ApplyEdits","ApplyEdits method [XPS Documents and Packaging]","ApplyEdits method [XPS Documents and Packaging]","IXpsOMGlyphsEditor interface","IXpsOMGlyphsEditor interface [XPS Documents and Packaging]","ApplyEdits method","IXpsOMGlyphsEditor.ApplyEdits","IXpsOMGlyphsEditor::ApplyEdits","xps.ixpsomglyphseditor_applyedits","xpsobjectmodel/IXpsOMGlyphsEditor::ApplyEdits"]
old-location: xps\ixpsomglyphseditor_applyedits.htm
tech.root: xps
ms.assetid: ddbd8dc4-5d4f-4b30-8943-f4a5bc8e64c2
ms.date: 12/05/2018
ms.keywords: ApplyEdits, ApplyEdits method [XPS Documents and Packaging], ApplyEdits method [XPS Documents and Packaging],IXpsOMGlyphsEditor interface, IXpsOMGlyphsEditor interface [XPS Documents and Packaging],ApplyEdits method, IXpsOMGlyphsEditor.ApplyEdits, IXpsOMGlyphsEditor::ApplyEdits, xps.ixpsomglyphseditor_applyedits, xpsobjectmodel/IXpsOMGlyphsEditor::ApplyEdits
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
 - IXpsOMGlyphsEditor::ApplyEdits
 - xpsobjectmodel/IXpsOMGlyphsEditor::ApplyEdits
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
 - IXpsOMGlyphsEditor.ApplyEdits
---

# IXpsOMGlyphsEditor::ApplyEdits

## -description

Performs cross-property validation and then copies the changes to the parent <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a> interface.



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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor">IXpsOMGlyphsEditor</a> interface does not belong to a valid <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a> interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_CARET_OUTSIDE_STRING</b></dt>
</dl>
</td>
<td width="60%">
Caret stops were specified for an empty string, or the caret jump index has exceeded the length of the Unicode string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_MAPPING_OUTSIDE_INDICES</b></dt>
</dl>
</td>
<td width="60%">
The glyph mappings exceed the number of glyph indices.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_MAPPING_OUTSIDE_STRING</b></dt>
</dl>
</td>
<td width="60%">
Glyph mappings were defined for an empty string. If the Unicode string is empty, there must not be any glyph mappings defined.

or

The glyph mappings exceed the length of the Unicode string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_MISSING_GLYPHS</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a> interface without a Unicode string does not have any glyph indices specified. An <b>IXpsOMGlyphs</b> interface must specify either a Unicode string or an array of glyph indices.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_ODD_BIDILEVEL</b></dt>
</dl>
</td>
<td width="60%">
The text string was specified as sideways and right-to-left. If the text is sideways, it cannot have a bidi level that is an odd value (right-to-left). Likewise, if the bidi level is an odd value, it cannot be sideways.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_ONE_TO_ONE_MAPPING_EXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Glyph mappings did not match the Unicode string contents.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_TOO_MANY_INDICES</b></dt>
</dl>
</td>
<td width="60%">
                There were more glyph indices than Unicode code points. If there are no glyph mappings, the number of glyph indices must be less than or equal to the number of  Unicode code points.

</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor">IXpsOMGlyphsEditor</a>  interface remains valid after  this method is called, allowing for additional  modifications to be made.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor">IXpsOMGlyphsEditor</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
