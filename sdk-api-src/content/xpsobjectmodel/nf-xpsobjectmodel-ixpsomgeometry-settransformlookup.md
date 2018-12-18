---
UID: NF:xpsobjectmodel.IXpsOMGeometry.SetTransformLookup
title: IXpsOMGeometry::SetTransformLookup
author: windows-sdk-content
description: Sets the lookup key name of a shared matrix transform in a resource dictionary.
old-location: xps\ixpsomgeometry_settransformlookup.htm
tech.root: printdocs
ms.assetid: 98623f23-eb34-4140-8179-46786ab18fb0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IXpsOMGeometry interface [XPS Documents and Packaging],SetTransformLookup method, IXpsOMGeometry.SetTransformLookup, IXpsOMGeometry::SetTransformLookup, SetTransformLookup, SetTransformLookup method [XPS Documents and Packaging], SetTransformLookup method [XPS Documents and Packaging],IXpsOMGeometry interface, xps.ixpsomgeometry_settransformlookup, xpsobjectmodel/IXpsOMGeometry::SetTransformLookup
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
 - IXpsOMGeometry.SetTransformLookup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMGeometry::SetTransformLookup


## -description


Sets the lookup key name of a shared matrix transform in a resource dictionary.


## -parameters




### -param lookup [in]

The key name of the shared matrix transform in the resource dictionary.


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
<dt><b>XPS_E_INVALID_RESOURCE_KEY</b></dt>
</dl>
</td>
<td width="60%">
According to the <a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>, the value of <i>lookup</i> is not a valid lookup key string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_INVALID_LOOKUP_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The lookup key name in <i>lookup</i> references an object that is not a transform.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_LOOKUP_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No object could be found with a key name that matches the value passed in <i>lookup</i>.

</td>
</tr>
</table>
 




## -remarks



After you call <b>SetTransformLookup</b>, the local transform is released and <a href="https://msdn.microsoft.com/1ae895a1-7b63-460c-b066-d8e9c7cd03c2">GetTransformLocal</a> returns a <b>NULL</b> pointer in the <i>transform</i> parameter. The table that follows explains the relationship between the local and lookup values of this property.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>transform</i>   by <a href="https://msdn.microsoft.com/2247aa7b-28b3-459e-b565-d52a6cff7323">GetTransform</a>
</th>
<th>Object that is returned in <i>transform</i> by <a href="https://msdn.microsoft.com/1ae895a1-7b63-460c-b066-d8e9c7cd03c2">GetTransformLocal</a>
</th>
<th>Object that is returned in <i>lookup</i> by <a href="https://msdn.microsoft.com/21a9a2c5-c9f2-42a4-84c4-8f702950d7ba">GetTransformLookup</a>
</th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/ca4a458d-e2e5-4f8c-aac1-35f5ff91a0d9">SetTransformLocal</a>


</td>
<td>
The local transform that is set by <a href="https://msdn.microsoft.com/ca4a458d-e2e5-4f8c-aac1-35f5ff91a0d9">SetTransformLocal</a>.

</td>
<td>
The local transform that is set by <a href="https://msdn.microsoft.com/ca4a458d-e2e5-4f8c-aac1-35f5ff91a0d9">SetTransformLocal</a>.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>
<b>SetTransformLookup</b> (this method)

</td>
<td>
The shared transform retrieved, with a lookup key that matches the key set by <b>SetTransformLookup</b>, from the resource directory.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
The lookup key that is set by <b>SetTransformLookup</b>.

</td>
</tr>
<tr>
<td>
Neither <a href="https://msdn.microsoft.com/ca4a458d-e2e5-4f8c-aac1-35f5ff91a0d9">SetTransformLocal</a> nor <b>SetTransformLookup</b> has been called yet.

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
 

 

