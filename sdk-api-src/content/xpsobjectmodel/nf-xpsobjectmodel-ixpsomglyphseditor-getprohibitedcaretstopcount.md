---
UID: NF:xpsobjectmodel.IXpsOMGlyphsEditor.GetProhibitedCaretStopCount
title: IXpsOMGlyphsEditor::GetProhibitedCaretStopCount (xpsobjectmodel.h)
description: Gets the number of prohibited caret stops. (IXpsOMGlyphsEditor.GetProhibitedCaretStopCount)
helpviewer_keywords: ["GetProhibitedCaretStopCount","GetProhibitedCaretStopCount method [XPS Documents and Packaging]","GetProhibitedCaretStopCount method [XPS Documents and Packaging]","IXpsOMGlyphsEditor interface","IXpsOMGlyphsEditor interface [XPS Documents and Packaging]","GetProhibitedCaretStopCount method","IXpsOMGlyphsEditor.GetProhibitedCaretStopCount","IXpsOMGlyphsEditor::GetProhibitedCaretStopCount","xps.ixpsomglyphseditor_getprohibitedcaretstopcount","xpsobjectmodel/IXpsOMGlyphsEditor::GetProhibitedCaretStopCount"]
old-location: xps\ixpsomglyphseditor_getprohibitedcaretstopcount.htm
tech.root: xps
ms.assetid: 8aeb4868-f52e-4e80-b0c6-c8f759066fb2
ms.date: 12/05/2018
ms.keywords: GetProhibitedCaretStopCount, GetProhibitedCaretStopCount method [XPS Documents and Packaging], GetProhibitedCaretStopCount method [XPS Documents and Packaging],IXpsOMGlyphsEditor interface, IXpsOMGlyphsEditor interface [XPS Documents and Packaging],GetProhibitedCaretStopCount method, IXpsOMGlyphsEditor.GetProhibitedCaretStopCount, IXpsOMGlyphsEditor::GetProhibitedCaretStopCount, xps.ixpsomglyphseditor_getprohibitedcaretstopcount, xpsobjectmodel/IXpsOMGlyphsEditor::GetProhibitedCaretStopCount
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
 - IXpsOMGlyphsEditor::GetProhibitedCaretStopCount
 - xpsobjectmodel/IXpsOMGlyphsEditor::GetProhibitedCaretStopCount
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
 - IXpsOMGlyphsEditor.GetProhibitedCaretStopCount
---

# IXpsOMGlyphsEditor::GetProhibitedCaretStopCount


## -description

Gets the number of prohibited caret stops.

## -parameters

### -param prohibitedCaretStopCount [out, retval]

The number of prohibited caret stops.

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
<i>prohibitedCaretStopCount</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

To get the prohibited caret stops, call <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphseditor-getprohibitedcaretstops">GetProhibitedCaretStops</a>.  

Each caret stop index corresponds to the scalar values of a UTF-16  <b>UnicodeString</b> property.  Index 0 represents the location just before the first UTF-16 scalar value of <b>UnicodeString</b>; index 1 represents the location between the first and second UTF-16 scalar values, and so on. There is an additional index at the end of <b>UnicodeString</b>. Any unspecified index is a valid caret stop location.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor">IXpsOMGlyphsEditor</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
