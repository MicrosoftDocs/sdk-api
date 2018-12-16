---
UID: NF:xpsobjectmodel.IXpsOMSolidColorBrush.Clone
title: IXpsOMSolidColorBrush::Clone
author: windows-sdk-content
description: Makes a deep copy of the interface.
old-location: xps\ixpsomsolidcolorbrush_clone.htm
tech.root: printdocs
ms.assetid: 7f25d5cf-b53d-4e86-ae61-1d0c9afc6236
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Clone, Clone method [XPS Documents and Packaging], Clone method [XPS Documents and Packaging],IXpsOMSolidColorBrush interface, IXpsOMSolidColorBrush interface [XPS Documents and Packaging],Clone method, IXpsOMSolidColorBrush.Clone, IXpsOMSolidColorBrush::Clone, xps.ixpsomsolidcolorbrush_clone, xpsobjectmodel/IXpsOMSolidColorBrush::Clone
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
 - IXpsOMSolidColorBrush.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMSolidColorBrush::Clone


## -description


Makes a deep copy of the interface.


## -parameters




### -param solidColorBrush [out, retval]

A pointer to the copy of the interface.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>solidColorBrush</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method does not update any of the resource pointers in the copy.




## -see-also




<a href="https://msdn.microsoft.com/26580a25-09d1-4a9b-85c3-aa8ddcc97867">IXpsOMSolidColorBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

