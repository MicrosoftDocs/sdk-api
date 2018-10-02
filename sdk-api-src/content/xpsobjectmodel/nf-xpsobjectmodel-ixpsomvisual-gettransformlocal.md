---
UID: NF:xpsobjectmodel.IXpsOMVisual.GetTransformLocal
title: IXpsOMVisual::GetTransformLocal
author: windows-sdk-content
description: Gets a pointer to the IXpsOMMatrixTransform interface that contains the local, unshared, resolved matrix transform for the visual.
old-location: xps\ixpsomvisual_gettransformlocal.htm
tech.root: printdocs
ms.assetid: a7152ba0-2b65-4c66-b99b-7450a8cdb6fd
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetTransformLocal, GetTransformLocal method [XPS Documents and Packaging], GetTransformLocal method [XPS Documents and Packaging],IXpsOMVisual interface, IXpsOMVisual interface [XPS Documents and Packaging],GetTransformLocal method, IXpsOMVisual.GetTransformLocal, IXpsOMVisual::GetTransformLocal, xps.ixpsomvisual_gettransformlocal, xpsobjectmodel/IXpsOMVisual::GetTransformLocal
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
 - IXpsOMVisual.GetTransformLocal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMVisual::GetTransformLocal


## -description


Gets a pointer to the <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface that contains the local, unshared, resolved matrix transform for the visual.


## -parameters




### -param matrixTransform [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface  that contains the local, unshared, resolved matrix transform for the visual.  If a matrix transform lookup key has not been set, or if a local matrix transform has  been set, a <b>NULL</b> pointer is returned.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>matrixTransform</i></th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/ac087cb0-dd3c-4f4b-a6e0-6f0f0a219d8a">SetTransformLocal</a>


</td>
<td>
The local transform that is set by <a href="https://msdn.microsoft.com/ac087cb0-dd3c-4f4b-a6e0-6f0f0a219d8a">SetTransformLocal</a>.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/b9066cf8-37b5-4c30-ae41-f92a61aa552c">SetTransformLookup</a>


</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>
Neither <a href="https://msdn.microsoft.com/ac087cb0-dd3c-4f4b-a6e0-6f0f0a219d8a">SetTransformLocal</a> nor <a href="https://msdn.microsoft.com/b9066cf8-37b5-4c30-ae41-f92a61aa552c">SetTransformLookup</a> has been called yet.

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
<i>matrixTransform</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a>



<a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

