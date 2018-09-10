---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.GetProhibitedCaretStopCount
title: IXpsOMGlyphs::GetProhibitedCaretStopCount
author: windows-sdk-content
description: Gets the number of prohibited caret stops.
old-location: xps\ixpsomglyphs_getprohibitedcaretstopcount.htm
tech.root: printdocs
ms.assetid: 1f4974e9-b88b-40c0-89f5-b69fec5c2d83
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetProhibitedCaretStopCount, GetProhibitedCaretStopCount method [XPS Documents and Packaging], GetProhibitedCaretStopCount method [XPS Documents and Packaging],IXpsOMGlyphs interface, IXpsOMGlyphs interface [XPS Documents and Packaging],GetProhibitedCaretStopCount method, IXpsOMGlyphs.GetProhibitedCaretStopCount, IXpsOMGlyphs::GetProhibitedCaretStopCount, xps.ixpsomglyphs_getprohibitedcaretstopcount, xpsobjectmodel/IXpsOMGlyphs::GetProhibitedCaretStopCount
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
 - IXpsOMGlyphs.GetProhibitedCaretStopCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMGlyphs::GetProhibitedCaretStopCount


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




<a href="https://msdn.microsoft.com/9e5372af-5233-4278-8b84-c3a308cc3041">GetProhibitedCaretStops</a> gets the prohibited caret stops.

Each caret stop index corresponds to the scalar values of a UTF-16  <b>UnicodeString</b> property.  Index 0 represents the location just before the first UTF-16 scalar value of <b>UnicodeString</b>; index 1 represents the location between the first and second UTF-16 scalar values, and so on. There is an additional index at the end of <b>UnicodeString</b>. Any unspecified index is a valid caret stop location.




## -see-also




<a href="https://msdn.microsoft.com/9e5372af-5233-4278-8b84-c3a308cc3041">GetProhibitedCaretStops</a>



<a href="https://msdn.microsoft.com/6d2cda65-c719-46f2-97c9-8aee7b5f84b9">IXpsOMGlyphs</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

