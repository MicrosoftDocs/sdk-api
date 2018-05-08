---
UID: NF:xpsobjectmodel.IXpsOMImageBrush.Clone
title: IXpsOMImageBrush::Clone
author: windows-driver-content
description: Makes a deep copy of the interface.
old-location: xps\ixpsomimagebrush_clone.htm
old-project: printdocs
ms.assetid: 7c10f6e5-b223-4ddb-9fcf-c9f7bf82953f
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: Clone, Clone method [XPS Documents and Packaging], Clone method [XPS Documents and Packaging],IXpsOMImageBrush interface, IXpsOMImageBrush interface [XPS Documents and Packaging],Clone method, IXpsOMImageBrush.Clone, IXpsOMImageBrush::Clone, xps.ixpsomimagebrush_clone, xpsobjectmodel/IXpsOMImageBrush::Clone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: XPS_INTERLEAVING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsobjectmodel.h
api_name:
-	IXpsOMImageBrush.Clone
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMImageBrush::Clone


## -description


Makes a deep copy of the interface.


## -parameters




### -param imageBrush [out, retval]

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
<i>imageBrush</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method does not update any of the resource pointers in the copy.




## -see-also




<a href="https://msdn.microsoft.com/f5478582-466b-496e-b7f3-42fb8caa6814">IXpsOMImageBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

