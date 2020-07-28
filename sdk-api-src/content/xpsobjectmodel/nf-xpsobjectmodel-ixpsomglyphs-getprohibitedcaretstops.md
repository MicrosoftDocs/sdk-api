---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.GetProhibitedCaretStops
title: IXpsOMGlyphs::GetProhibitedCaretStops (xpsobjectmodel.h)
description: Gets an array of prohibited caret stop locations.
helpviewer_keywords: ["GetProhibitedCaretStops","GetProhibitedCaretStops method [XPS Documents and Packaging]","GetProhibitedCaretStops method [XPS Documents and Packaging]","IXpsOMGlyphs interface","IXpsOMGlyphs interface [XPS Documents and Packaging]","GetProhibitedCaretStops method","IXpsOMGlyphs.GetProhibitedCaretStops","IXpsOMGlyphs::GetProhibitedCaretStops","xps.ixpsomglyphs_getprohibitedcaretstops","xpsobjectmodel/IXpsOMGlyphs::GetProhibitedCaretStops"]
old-location: xps\ixpsomglyphs_getprohibitedcaretstops.htm
tech.root: xps
ms.assetid: 9e5372af-5233-4278-8b84-c3a308cc3041
ms.date: 12/05/2018
ms.keywords: GetProhibitedCaretStops, GetProhibitedCaretStops method [XPS Documents and Packaging], GetProhibitedCaretStops method [XPS Documents and Packaging],IXpsOMGlyphs interface, IXpsOMGlyphs interface [XPS Documents and Packaging],GetProhibitedCaretStops method, IXpsOMGlyphs.GetProhibitedCaretStops, IXpsOMGlyphs::GetProhibitedCaretStops, xps.ixpsomglyphs_getprohibitedcaretstops, xpsobjectmodel/IXpsOMGlyphs::GetProhibitedCaretStops
f1_keywords:
- xpsobjectmodel/IXpsOMGlyphs.GetProhibitedCaretStops
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- xpsobjectmodel.h
api_name:
- IXpsOMGlyphs.GetProhibitedCaretStops
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMGlyphs::GetProhibitedCaretStops


## -description


Gets an array of prohibited caret stop locations.


## -parameters




### -param prohibitedCaretStopCount [in, out]

The number of prohibited caret stop locations that will fit in the array referenced by <i>prohibitedCaretStops</i>. When the method returns, <i>prohibitedCaretStopCount</i> will contain the number of values returned in the array referenced by <i>prohibitedCaretStops</i>.


### -param prohibitedCaretStops [out]

An array of prohibited caret stop locations; if such are not defined, a <b>NULL</b> pointer is returned.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
<i>prohibitedCaretStopCount</i>, <i>prohibitedCaretStops</i>, or both are <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
<i>prohibitedCaretStops</i> is not large enough to receive the prohibited caret stop data. <i>prohibitedCaretStopCount</i> contains the required number of elements.

</td>
</tr>
</table>
 




## -remarks



Each caret stop index corresponds to the scalar values of a UTF-16  <b>UnicodeString</b> property.  Index 0 represents the location just before the first UTF-16 scalar value of <b>UnicodeString</b>; index 1 represents the location between the first and second UTF-16 scalar values, and so on. There is an additional index at the end of <b>UnicodeString</b>. Any unspecified index is a valid caret stop location.


<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-getprohibitedcaretstopcount">GetProhibitedCaretStopCount</a> gets the number of prohibited caret stops.

A caret stop is the index of the UTF-16 code point in the <b>UnicodeString</b> property of the glyph. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-getprohibitedcaretstopcount">GetProhibitedCaretStopCount</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
 

 

