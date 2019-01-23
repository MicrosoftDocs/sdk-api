---
UID: NF:xpsobjectmodel.IXpsOMPath.SetStrokeMiterLimit
title: IXpsOMPath::SetStrokeMiterLimit
author: windows-sdk-content
description: Sets the miter limit of the path.
old-location: xps\ixpsompath_setstrokemiterlimit.htm
tech.root: printdocs
ms.assetid: 4e33f9f3-119a-4635-b44c-fa002a59fa20
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IXpsOMPath interface [XPS Documents and Packaging],SetStrokeMiterLimit method, IXpsOMPath.SetStrokeMiterLimit, IXpsOMPath::SetStrokeMiterLimit, SetStrokeMiterLimit, SetStrokeMiterLimit method [XPS Documents and Packaging], SetStrokeMiterLimit method [XPS Documents and Packaging],IXpsOMPath interface, xps.ixpsompath_setstrokemiterlimit, xpsobjectmodel/IXpsOMPath::SetStrokeMiterLimit
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
 - IXpsOMPath.SetStrokeMiterLimit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPath::SetStrokeMiterLimit


## -description


Sets the miter limit of the path.


## -parameters




### -param strokeMiterLimit [in]

The miter limit value to be set. The value must be 1.0 or greater.


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
A value that was passed in <i>strokeMiterLimit</i> was not valid.

</td>
</tr>
</table>
 




## -remarks



 The miter limit value is the ratio of the maximum miter length  to one-half of the stroke thickness.

The miter limit value describes how to render a mitered line join. This value applies only if the line join style value is <a href="https://msdn.microsoft.com/en-us/library/Dd372963(v=VS.85).aspx">XPS_LINE_JOIN_MITER</a>.




## -see-also




<a href="https://msdn.microsoft.com/93257a77-3fef-400e-bfe1-06e760ba4b93">IXpsOMPath</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

