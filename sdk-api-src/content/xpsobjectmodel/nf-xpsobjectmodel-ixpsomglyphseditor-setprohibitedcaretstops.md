---
UID: NF:xpsobjectmodel.IXpsOMGlyphsEditor.SetProhibitedCaretStops
title: IXpsOMGlyphsEditor::SetProhibitedCaretStops (xpsobjectmodel.h)
author: windows-sdk-content
description: Sets an array of prohibited caret stop locations.
old-location: xps\ixpsomglyphseditor_setprohibitedcaretstops.htm
tech.root: printdocs
ms.assetid: 5f2e1014-d50b-4755-a533-239b6ba9009e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IXpsOMGlyphsEditor interface [XPS Documents and Packaging],SetProhibitedCaretStops method, IXpsOMGlyphsEditor.SetProhibitedCaretStops, IXpsOMGlyphsEditor::SetProhibitedCaretStops, SetProhibitedCaretStops, SetProhibitedCaretStops method [XPS Documents and Packaging], SetProhibitedCaretStops method [XPS Documents and Packaging],IXpsOMGlyphsEditor interface, xps.ixpsomglyphseditor_setprohibitedcaretstops, xpsobjectmodel/IXpsOMGlyphsEditor::SetProhibitedCaretStops
ms.topic: method
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
 - IXpsOMGlyphsEditor.SetProhibitedCaretStops
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMGlyphsEditor::SetProhibitedCaretStops


## -description


Sets an array of prohibited caret stop locations.




## -parameters




### -param count [in]

The number of prohibited caret stop locations in the array that is referenced by <i>prohibitedCaretStops</i>. A value of 0 clears the property.


### -param prohibitedCaretStops [in]

The array of prohibited caret stop locations to be set. If <i>count</i> is 0, this parameter is ignored and can be set to <b>NULL</b>.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.

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
<i>prohibitedCaretStops</i> is <b>NULL</b> and <i>count</i> is greater than 0.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_CARET_OUTOFORDER</b></dt>
</dl>
</td>
<td width="60%">
A caret location value is out of order. The location values must be sorted in ascending order.

</td>
</tr>
</table>
 




## -remarks



Each caret stop index corresponds to the scalar values of a UTF-16  <b>UnicodeString</b> property.  Index 0 represents the location just before the first UTF-16 scalar value of <b>UnicodeString</b>; index 1 represents the location between the first and second UTF-16 scalar values, and so on. There is an additional index at the end of <b>UnicodeString</b>. Any unspecified index is a valid caret stop location.




## -see-also




<a href="https://msdn.microsoft.com/5bdf2892-ce6f-4560-b638-e441166fc309">IXpsOMGlyphsEditor</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

