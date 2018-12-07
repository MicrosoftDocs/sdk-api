---
UID: NF:xpsobjectmodel.IXpsOMPath.GetStrokeDashOffset
title: IXpsOMPath::GetStrokeDashOffset
author: windows-sdk-content
description: Gets the offset from the origin of the stroke to the starting point of the dash array pattern.
old-location: xps\ixpsompath_getstrokedashoffset.htm
tech.root: printdocs
ms.assetid: 173e820f-e926-44cc-a6ba-54edde770f73
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetStrokeDashOffset, GetStrokeDashOffset method [XPS Documents and Packaging], GetStrokeDashOffset method [XPS Documents and Packaging],IXpsOMPath interface, IXpsOMPath interface [XPS Documents and Packaging],GetStrokeDashOffset method, IXpsOMPath.GetStrokeDashOffset, IXpsOMPath::GetStrokeDashOffset, xps.ixpsompath_getstrokedashoffset, xpsobjectmodel/IXpsOMPath::GetStrokeDashOffset
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
 - IXpsOMPath.GetStrokeDashOffset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPath::GetStrokeDashOffset


## -description


Gets the offset from the origin of the stroke to the starting point of the dash array pattern.


## -parameters




### -param strokeDashOffset [out, retval]

The offset value; specified in multiples of the stroke thickness.


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
<i>strokeDashOffset</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/93257a77-3fef-400e-bfe1-06e760ba4b93">IXpsOMPath</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

