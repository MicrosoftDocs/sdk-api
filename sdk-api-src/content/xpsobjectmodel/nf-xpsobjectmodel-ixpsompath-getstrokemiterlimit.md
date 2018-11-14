---
UID: NF:xpsobjectmodel.IXpsOMPath.GetStrokeMiterLimit
title: IXpsOMPath::GetStrokeMiterLimit
author: windows-sdk-content
description: Gets the miter limit value that is set for the stroke.
old-location: xps\ixpsompath_getstrokemiterlimit.htm
tech.root: printdocs
ms.assetid: 4271c7ff-636c-4ab0-b83f-90c769baf74c
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetStrokeMiterLimit, GetStrokeMiterLimit method [XPS Documents and Packaging], GetStrokeMiterLimit method [XPS Documents and Packaging],IXpsOMPath interface, IXpsOMPath interface [XPS Documents and Packaging],GetStrokeMiterLimit method, IXpsOMPath.GetStrokeMiterLimit, IXpsOMPath::GetStrokeMiterLimit, xps.ixpsompath_getstrokemiterlimit, xpsobjectmodel/IXpsOMPath::GetStrokeMiterLimit
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
 - IXpsOMPath.GetStrokeMiterLimit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xpsobjectmodel.h
: 
- IXpsOMPath.GetStrokeMiterLimit
: 
---

# IXpsOMPath::GetStrokeMiterLimit


## -description


Gets the miter limit value that is  set for the stroke.


## -parameters




### -param strokeMiterLimit [out, retval]

The miter limit value that is set for the stroke.


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
<i>strokeMiterLimit</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



 The miter limit value is the ratio of the maximum miter length  to one-half of the stroke thickness.

The miter limit value describes how to render a mitered line join; this value applies only if the line join style value is <a href="https://msdn.microsoft.com/b0409564-a6b3-4e9d-b136-3d865dd46f1d">XPS_LINE_JOIN_MITER</a>.




## -see-also




<a href="https://msdn.microsoft.com/93257a77-3fef-400e-bfe1-06e760ba4b93">IXpsOMPath</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/b0409564-a6b3-4e9d-b136-3d865dd46f1d">XPS_LINE_JOIN_MITER</a>
 

 

