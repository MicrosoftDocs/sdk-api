---
UID: NF:xpsobjectmodel.IXpsOMGradientBrush.GetTransformLocal
title: IXpsOMGradientBrush::GetTransformLocal
author: windows-sdk-content
description: Gets a pointer to the IXpsOMMatrixTransform interface that contains the local, unshared, resolved matrix transform for the brush.
old-location: xps\ixpsomgradientbrush_gettransformlocal.htm
old-project: printdocs
ms.assetid: dfdd6797-b7e6-46fa-92b1-d9c418e8a510
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetTransformLocal, GetTransformLocal method [XPS Documents and Packaging], GetTransformLocal method [XPS Documents and Packaging],IXpsOMGradientBrush interface, IXpsOMGradientBrush interface [XPS Documents and Packaging],GetTransformLocal method, IXpsOMGradientBrush.GetTransformLocal, IXpsOMGradientBrush::GetTransformLocal, xps.ixpsomgradientbrush_gettransformlocal, xpsobjectmodel/IXpsOMGradientBrush::GetTransformLocal
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: XPS_INTERLEAVING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMGradientBrush.GetTransformLocal
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMGradientBrush::GetTransformLocal


## -description


Gets a pointer to the <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface that contains the local, unshared, resolved matrix transform for the brush.


## -parameters




### -param transform [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface  that contains the local, unshared, resolved matrix transform for the brush. If  the transform has not been set or if a matrix transform lookup key has been set, a <b>NULL</b> pointer is returned.

The value that is returned in this parameter depends on which method has been most recently called to set the transform.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>transform</i></th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/aabb0410-bdff-4b6b-8d8a-de1cc6fca68b">SetTransformLocal</a>


</td>
<td>
The local transform that is set by <a href="https://msdn.microsoft.com/aabb0410-bdff-4b6b-8d8a-de1cc6fca68b">SetTransformLocal</a>.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/342434ff-9fdc-43ea-8beb-9d518f7a9454">SetTransformLookup</a>


</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>
Neither <a href="https://msdn.microsoft.com/aabb0410-bdff-4b6b-8d8a-de1cc6fca68b">SetTransformLocal</a> nor <a href="https://msdn.microsoft.com/342434ff-9fdc-43ea-8beb-9d518f7a9454">SetTransformLookup</a> has been called yet.

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
<i>transform</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



 The transform  determines how the gradient is transformed. The visible part of the gradient that is ultimately rendered in the image is determined by the path, stroke, or glyph that is using the gradient brush.




## -see-also




<a href="https://msdn.microsoft.com/d381b813-5368-4ffe-a9a1-0f5027ae9d80">IXpsOMGradientBrush</a>



<a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

