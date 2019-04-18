---
UID: NF:xpsobjectmodel.IXpsOMPath.SetStrokeThickness
title: IXpsOMPath::SetStrokeThickness (xpsobjectmodel.h)
author: windows-sdk-content
description: Sets the stroke thickness.
old-location: xps\ixpsompath_setstrokethickness.htm
tech.root: printdocs
ms.assetid: e16774e2-9c70-46b6-a894-e289cdee47b3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsOMPath interface [XPS Documents and Packaging],SetStrokeThickness method, IXpsOMPath.SetStrokeThickness, IXpsOMPath::SetStrokeThickness, SetStrokeThickness, SetStrokeThickness method [XPS Documents and Packaging], SetStrokeThickness method [XPS Documents and Packaging],IXpsOMPath interface, xps.ixpsompath_setstrokethickness, xpsobjectmodel/IXpsOMPath::SetStrokeThickness
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
 - IXpsOMPath.SetStrokeThickness
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMPath::SetStrokeThickness


## -description


Sets the stroke thickness.


## -parameters




### -param strokeThickness [in]

The stroke thickness value to be set; must be 0.0 or greater.


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
A value that was passed in <i>strokeThickness</i> was not valid.

</td>
</tr>
</table>
 




## -remarks



The value returned in <i>strokeThickness</i> specifies  the thickness of a stroke in units of the effective coordinate space; the units include the path's render transform.

The stroke is drawn on top of the boundary of the path's geometry, such that one half of the stroke's width extends outside of the path's specified geometry  and the other half falls inside of it.




## -see-also




<a href="https://msdn.microsoft.com/93257a77-3fef-400e-bfe1-06e760ba4b93">IXpsOMPath</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

