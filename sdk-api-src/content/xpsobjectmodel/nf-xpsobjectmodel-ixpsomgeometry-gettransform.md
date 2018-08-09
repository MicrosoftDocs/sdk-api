---
UID: NF:xpsobjectmodel.IXpsOMGeometry.GetTransform
title: IXpsOMGeometry::GetTransform
author: windows-sdk-content
description: Gets a pointer to the geometry's IXpsOMMatrixTransform interface, which contains the resolved matrix transform for the geometry.
old-location: xps\ixpsomgeometry_gettransform.htm
old-project: printdocs
ms.assetid: 2247aa7b-28b3-459e-b565-d52a6cff7323
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetTransform, GetTransform method [XPS Documents and Packaging], GetTransform method [XPS Documents and Packaging],IXpsOMGeometry interface, IXpsOMGeometry interface [XPS Documents and Packaging],GetTransform method, IXpsOMGeometry.GetTransform, IXpsOMGeometry::GetTransform, xps.ixpsomgeometry_gettransform, xpsobjectmodel/IXpsOMGeometry::GetTransform
ms.prod: windows
ms.technology: windows-sdk
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
 - IXpsOMGeometry.GetTransform
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMGeometry::GetTransform


## -description


Gets a pointer to the geometry's <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface, which contains the resolved matrix transform for the geometry.


## -parameters




### -param transform [out, retval]

A pointer to the geometry's <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface, which contains the resolved matrix transform for the geometry. If  a matrix transform has not been set, a <b>NULL</b> pointer will be returned.

The value that is returned in this parameter depends on which method has most recently been called to set the transform.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>transform</i></th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/ca4a458d-e2e5-4f8c-aac1-35f5ff91a0d9">SetTransformLocal</a>


</td>
<td>
The local transform that is set by <a href="https://msdn.microsoft.com/ca4a458d-e2e5-4f8c-aac1-35f5ff91a0d9">SetTransformLocal</a>.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/98623f23-eb34-4140-8179-46786ab18fb0">SetTransformLookup</a>


</td>
<td>
The shared transform retrieved, with a lookup key that matches the key that is set by <a href="https://msdn.microsoft.com/98623f23-eb34-4140-8179-46786ab18fb0">SetTransformLookup</a>, from the resource directory.

</td>
</tr>
<tr>
<td>
Neither <a href="https://msdn.microsoft.com/ca4a458d-e2e5-4f8c-aac1-35f5ff91a0d9">SetTransformLocal</a> nor <a href="https://msdn.microsoft.com/98623f23-eb34-4140-8179-46786ab18fb0">SetTransformLookup</a> has been called yet.

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
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_LOOKUP_INVALID_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The lookup key name set by  <a href="https://msdn.microsoft.com/b2af731a-bea7-4f1b-8e31-b0173e38fd67">SetStrokeBrushLookup</a> references an object that is not a brush.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_LOOKUP_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No object could be found with a key name that matched the lookup value.

No object could be found with a key name that matched the value passed in <i>lookup</i>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a>



<a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

