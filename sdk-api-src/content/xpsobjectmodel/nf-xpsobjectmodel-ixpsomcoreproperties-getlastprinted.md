---
UID: NF:xpsobjectmodel.IXpsOMCoreProperties.GetLastPrinted
title: IXpsOMCoreProperties::GetLastPrinted (xpsobjectmodel.h)
author: windows-sdk-content
description: Gets the lastPrinted property.
old-location: xps\ixpsomcoreproperties_getlastprinted.htm
tech.root: printdocs
ms.assetid: c7e4b994-ec4f-415d-a340-813f00adba19
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetLastPrinted, GetLastPrinted method [XPS Documents and Packaging], GetLastPrinted method [XPS Documents and Packaging],IXpsOMCoreProperties interface, IXpsOMCoreProperties interface [XPS Documents and Packaging],GetLastPrinted method, IXpsOMCoreProperties.GetLastPrinted, IXpsOMCoreProperties::GetLastPrinted, xps.ixpsomcoreproperties_getlastprinted, xpsobjectmodel/IXpsOMCoreProperties::GetLastPrinted
ms.topic: method
f1_keywords: 
 - "xpsobjectmodel/IXpsOMCoreProperties.GetLastPrinted"
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
 - IXpsOMCoreProperties.GetLastPrinted
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMCoreProperties::GetLastPrinted


## -description


Gets the <b>lastPrinted</b> property.


## -parameters




### -param lastPrinted [out, retval]

The date and time that  are read from the <b>lastPrinted</b> property.


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
<i>lastPrinted</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The <b>lastPrinted</b> property contains the date and time the package was last printed.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a>



<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">Standard ECMA-376, Office Open XML File Formats</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
 

 

