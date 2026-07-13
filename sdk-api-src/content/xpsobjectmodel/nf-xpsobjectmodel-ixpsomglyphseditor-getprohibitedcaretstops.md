---
UID: NF:xpsobjectmodel.IXpsOMGlyphsEditor.GetProhibitedCaretStops
title: IXpsOMGlyphsEditor::GetProhibitedCaretStops (xpsobjectmodel.h)
description: Gets an array of prohibited caret stop locations. (IXpsOMGlyphsEditor.GetProhibitedCaretStops)
helpviewer_keywords: ["GetProhibitedCaretStops","GetProhibitedCaretStops method [XPS Documents and Packaging]","GetProhibitedCaretStops method [XPS Documents and Packaging]","IXpsOMGlyphsEditor interface","IXpsOMGlyphsEditor interface [XPS Documents and Packaging]","GetProhibitedCaretStops method","IXpsOMGlyphsEditor.GetProhibitedCaretStops","IXpsOMGlyphsEditor::GetProhibitedCaretStops","xps.ixpsomglyphseditor_getprohibitedcaretstops","xpsobjectmodel/IXpsOMGlyphsEditor::GetProhibitedCaretStops"]
old-location: xps\ixpsomglyphseditor_getprohibitedcaretstops.htm
tech.root: xps
ms.assetid: 274d2137-c26f-438c-8c1b-591fbcb72c72
ms.date: 12/05/2018
ms.keywords: GetProhibitedCaretStops, GetProhibitedCaretStops method [XPS Documents and Packaging], GetProhibitedCaretStops method [XPS Documents and Packaging],IXpsOMGlyphsEditor interface, IXpsOMGlyphsEditor interface [XPS Documents and Packaging],GetProhibitedCaretStops method, IXpsOMGlyphsEditor.GetProhibitedCaretStops, IXpsOMGlyphsEditor::GetProhibitedCaretStops, xps.ixpsomglyphseditor_getprohibitedcaretstops, xpsobjectmodel/IXpsOMGlyphsEditor::GetProhibitedCaretStops
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
 - IXpsOMGlyphsEditor::GetProhibitedCaretStops
 - xpsobjectmodel/IXpsOMGlyphsEditor::GetProhibitedCaretStops
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
 - IXpsOMGlyphsEditor.GetProhibitedCaretStops
---

# IXpsOMGlyphsEditor::GetProhibitedCaretStops


## -description

Gets an array of prohibited caret stop locations.

## -parameters

### -param count [in, out]

The number of prohibited caret stop values that will fit in the array that is  referenced by the <i>prohibitedCaretStops</i> parameter. When the method returns, <i>prohibitedCaretStopCount</i> will contain the number of values in that array.

### -param prohibitedCaretStops [out]

An array of glyph mapping values. If   no prohibited caret stops have been defined, a <b>NULL</b> pointer is returned.

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
<i>prohibitedCaretStopCount</i>, <i>prohibitedCaretStops</i>, or both were <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
<i>prohibitedCaretStops</i> was not large enough to receive the prohibited caret stop data. <i>prohibitedCaretStopCount</i> contains the required number of elements.

</td>
</tr>
</table>

## -remarks

Each caret stop index corresponds to the scalar values of a UTF-16  <b>UnicodeString</b> property.  Index 0 represents the location just before the first UTF-16 scalar value of <b>UnicodeString</b>; index 1 represents the location between the first and second UTF-16 scalar values, and so on. There is an additional index at the end of <b>UnicodeString</b>. Any unspecified index is a valid caret stop location.


<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphseditor-getprohibitedcaretstopcount">GetProhibitedCaretStopCount</a> gets the number of prohibited caret stops.

A caret stop is the index of the UTF-16 code point in the <b>UnicodeString</b> property of the glyph.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor">IXpsOMGlyphsEditor</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
