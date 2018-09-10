---
UID: NF:xpsobjectmodel.IXpsOMPath.GetFillBrushLocal
title: IXpsOMPath::GetFillBrushLocal
author: windows-sdk-content
description: Gets a pointer to the local, unshared IXpsOMBrush interface that contains the fill brush for the path.
old-location: xps\ixpsompath_getfillbrushlocal.htm
tech.root: printdocs
ms.assetid: 5c5a7150-19d6-40aa-871b-5600c0b0a947
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetFillBrushLocal, GetFillBrushLocal method [XPS Documents and Packaging], GetFillBrushLocal method [XPS Documents and Packaging],IXpsOMPath interface, IXpsOMPath interface [XPS Documents and Packaging],GetFillBrushLocal method, IXpsOMPath.GetFillBrushLocal, IXpsOMPath::GetFillBrushLocal, xps.ixpsompath_getfillbrushlocal, xpsobjectmodel/IXpsOMPath::GetFillBrushLocal
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
 - IXpsOMPath.GetFillBrushLocal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPath::GetFillBrushLocal


## -description


Gets a pointer to the local, unshared <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a> interface that contains the fill brush for the path.


## -parameters




### -param brush [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a> interface to be used as the local, unshared fill brush for the path. If a fill brush lookup key has been set or if a local fill brush has not been set, a <b>NULL</b> pointer is returned.

The value that is returned in this parameter depends on which method has most recently been called to set the brush.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>brush</i></th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/ddec7d68-16a5-4c34-87c1-6a5de97aaa0c">SetFillBrushLocal</a>


</td>
<td>
The local brush that is set by <a href="https://msdn.microsoft.com/ddec7d68-16a5-4c34-87c1-6a5de97aaa0c">SetFillBrushLocal</a>.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/5a02af98-8bfc-4fb2-92b3-15b16b4b69c1">SetFillBrushLookup</a>


</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>
Neither <a href="https://msdn.microsoft.com/ddec7d68-16a5-4c34-87c1-6a5de97aaa0c">SetFillBrushLocal</a> nor <a href="https://msdn.microsoft.com/5a02af98-8bfc-4fb2-92b3-15b16b4b69c1">SetFillBrushLookup</a> has been called yet.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
</table>
 


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
<i>brush</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a>



<a href="https://msdn.microsoft.com/93257a77-3fef-400e-bfe1-06e760ba4b93">IXpsOMPath</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

