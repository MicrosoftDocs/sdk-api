---
UID: NF:xpsobjectmodel.IXpsOMGlyphsEditor.GetProhibitedCaretStopCount
title: IXpsOMGlyphsEditor::GetProhibitedCaretStopCount
author: windows-sdk-content
description: Gets the number of prohibited caret stops.
old-location: xps\ixpsomglyphseditor_getprohibitedcaretstopcount.htm
tech.root: printdocs
ms.assetid: 8aeb4868-f52e-4e80-b0c6-c8f759066fb2
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetProhibitedCaretStopCount, GetProhibitedCaretStopCount method [XPS Documents and Packaging], GetProhibitedCaretStopCount method [XPS Documents and Packaging],IXpsOMGlyphsEditor interface, IXpsOMGlyphsEditor interface [XPS Documents and Packaging],GetProhibitedCaretStopCount method, IXpsOMGlyphsEditor.GetProhibitedCaretStopCount, IXpsOMGlyphsEditor::GetProhibitedCaretStopCount, xps.ixpsomglyphseditor_getprohibitedcaretstopcount, xpsobjectmodel/IXpsOMGlyphsEditor::GetProhibitedCaretStopCount
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IXpsOMGlyphsEditor.GetProhibitedCaretStopCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMGlyphsEditor::GetProhibitedCaretStopCount


## -description


Gets the number of prohibited caret stops.


## -parameters




### -param prohibitedCaretStopCount [out, retval]

The number of prohibited caret stops.


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
<i>prohibitedCaretStopCount</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



To get the prohibited caret stops, call <a href="https://msdn.microsoft.com/274d2137-c26f-438c-8c1b-591fbcb72c72">GetProhibitedCaretStops</a>.  

Each caret stop index corresponds to the scalar values of a UTF-16  <b>UnicodeString</b> property.  Index 0 represents the location just before the first UTF-16 scalar value of <b>UnicodeString</b>; index 1 represents the location between the first and second UTF-16 scalar values, and so on. There is an additional index at the end of <b>UnicodeString</b>. Any unspecified index is a valid caret stop location.




## -see-also




<a href="https://msdn.microsoft.com/5bdf2892-ce6f-4560-b638-e441166fc309">IXpsOMGlyphsEditor</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

