---
UID: NF:xpsobjectmodel.IXpsOMGeometry.SetTransformLocal
title: IXpsOMGeometry::SetTransformLocal
author: windows-sdk-content
description: Sets the local, unshared matrix transform.
old-location: xps\ixpsomgeometry_settransformlocal.htm
tech.root: printdocs
ms.assetid: ca4a458d-e2e5-4f8c-aac1-35f5ff91a0d9
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IXpsOMGeometry interface [XPS Documents and Packaging],SetTransformLocal method, IXpsOMGeometry.SetTransformLocal, IXpsOMGeometry::SetTransformLocal, SetTransformLocal, SetTransformLocal method [XPS Documents and Packaging], SetTransformLocal method [XPS Documents and Packaging],IXpsOMGeometry interface, xps.ixpsomgeometry_settransformlocal, xpsobjectmodel/IXpsOMGeometry::SetTransformLocal
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
 - IXpsOMGeometry.SetTransformLocal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMGeometry::SetTransformLocal


## -description


Sets the local, unshared matrix transform.


## -parameters




### -param transform [in]

A pointer to the <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface to be set as the local, unshared matrix transform for the geometry.


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
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>transform</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>
 




## -remarks



After you call <b>SetTransformLocal</b>, the transform lookup key is released and <a href="https://msdn.microsoft.com/21a9a2c5-c9f2-42a4-84c4-8f702950d7ba">GetTransformLookup</a> returns a <b>NULL</b> pointer in the <i>lookup</i> parameter. The table that follows explains the relationship between the local and lookup values of this property.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>transform</i> by <a href="https://msdn.microsoft.com/2247aa7b-28b3-459e-b565-d52a6cff7323">GetTransform</a>
</th>
<th>Object that is returned in <i>transform</i> by <a href="https://msdn.microsoft.com/1ae895a1-7b63-460c-b066-d8e9c7cd03c2">GetTransformLocal</a>
</th>
<th>Object that is returned in <i>lookup</i> by <a href="https://msdn.microsoft.com/21a9a2c5-c9f2-42a4-84c4-8f702950d7ba">GetTransformLookup</a>
</th>
</tr>
<tr>
<td>
<b>SetTransformLocal</b> (this method)

</td>
<td>
The local transform that is set by <b>SetTransformLocal</b>.

</td>
<td>
The local transform that is set by <b>SetTransformLocal</b>.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/98623f23-eb34-4140-8179-46786ab18fb0">SetTransformLookup</a>


</td>
<td>
The shared transform retrieved, with a lookup key that matches the key that is set by <a href="https://msdn.microsoft.com/98623f23-eb34-4140-8179-46786ab18fb0">SetTransformLookup</a>, from the resource directory.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
The lookup key that is set by <a href="https://msdn.microsoft.com/98623f23-eb34-4140-8179-46786ab18fb0">SetTransformLookup</a>.

</td>
</tr>
<tr>
<td>
Neither <b>SetTransformLocal</b> nor <a href="https://msdn.microsoft.com/98623f23-eb34-4140-8179-46786ab18fb0">SetTransformLookup</a> has been called yet.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

