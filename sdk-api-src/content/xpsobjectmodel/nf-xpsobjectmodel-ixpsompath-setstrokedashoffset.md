---
UID: NF:xpsobjectmodel.IXpsOMPath.SetStrokeDashOffset
title: IXpsOMPath::SetStrokeDashOffset (xpsobjectmodel.h)
author: windows-sdk-content
description: Sets the offset from the origin of the stroke to the starting point of the dash array pattern.
old-location: xps\ixpsompath_setstrokedashoffset.htm
tech.root: printdocs
ms.assetid: f6d222e4-9480-4dc7-9963-7dd637892281
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsOMPath interface [XPS Documents and Packaging],SetStrokeDashOffset method, IXpsOMPath.SetStrokeDashOffset, IXpsOMPath::SetStrokeDashOffset, SetStrokeDashOffset, SetStrokeDashOffset method [XPS Documents and Packaging], SetStrokeDashOffset method [XPS Documents and Packaging],IXpsOMPath interface, xps.ixpsompath_setstrokedashoffset, xpsobjectmodel/IXpsOMPath::SetStrokeDashOffset
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
 - IXpsOMPath.SetStrokeDashOffset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPath::SetStrokeDashOffset


## -description


Sets the offset from the origin of the stroke to the starting point of the dash array pattern.


## -parameters




### -param strokeDashOffset [in]

The offset value to be set.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>strokeDashOffset</i> is not a valid offset value.

</td>
</tr>
</table>
 




## -remarks



 The  offset describes the distance from the origin of the stroke where the dash  starts, and  is specified in multiples of the stroke thickness.




## -see-also




<a href="https://msdn.microsoft.com/93257a77-3fef-400e-bfe1-06e760ba4b93">IXpsOMPath</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

