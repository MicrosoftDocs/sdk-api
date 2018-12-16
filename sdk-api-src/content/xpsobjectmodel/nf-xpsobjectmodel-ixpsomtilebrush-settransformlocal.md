---
UID: NF:xpsobjectmodel.IXpsOMTileBrush.SetTransformLocal
title: IXpsOMTileBrush::SetTransformLocal
author: windows-sdk-content
description: Sets the IXpsOMMatrixTransform interface pointer to a local, unshared matrix transform.
old-location: xps\ixpsomtilebrush_settransformlocal.htm
tech.root: printdocs
ms.assetid: a0a0f0e9-d8b5-4b42-804b-66780f56b09a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IXpsOMTileBrush interface [XPS Documents and Packaging],SetTransformLocal method, IXpsOMTileBrush.SetTransformLocal, IXpsOMTileBrush::SetTransformLocal, SetTransformLocal, SetTransformLocal method [XPS Documents and Packaging], SetTransformLocal method [XPS Documents and Packaging],IXpsOMTileBrush interface, xps.ixpsomtilebrush_settransformlocal, xpsobjectmodel/IXpsOMTileBrush::SetTransformLocal
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
 - IXpsOMTileBrush.SetTransformLocal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMTileBrush::SetTransformLocal


## -description


Sets the <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface pointer to a local, unshared matrix transform.


## -parameters




### -param transform [in]

A pointer to the <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface to be set as the local, unshared matrix transform. If a local transform has been set, a <b>NULL</b> pointer will release it.


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



The transform determines how the output area is transformed before the brush image is rendered in the path, stroke, or glyph that is using the tile brush.

After you call <b>SetTransformLocal</b>, the transform lookup key is released and <a href="https://msdn.microsoft.com/bebed09b-7af7-4da1-aaa3-e8e2a45f2717">GetTransformLookup</a> returns a <b>NULL</b> pointer in the <i>key</i> parameter. The table that follows explains the relationship between the local and lookup values of this property.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned  in <i>transform</i> by <a href="https://msdn.microsoft.com/db4c4ef8-d5f4-4cff-b38d-d211e14a98c1">GetTransform</a>
</th>
<th>Object that is returned  in <i>transform</i> by <a href="https://msdn.microsoft.com/e06661dd-387c-46c4-8c37-f4e101d3c536">GetTransformLocal</a>
</th>
<th>String that is returned  in <i>key</i> by <a href="https://msdn.microsoft.com/bebed09b-7af7-4da1-aaa3-e8e2a45f2717">GetTransformLookup</a>
</th>
</tr>
<tr>
<td>
<b>SetTransformLocal</b> (this method)

</td>
<td>
The transform that is set by <b>SetTransformLocal</b>.

</td>
<td>
The transform that is set by <b>SetTransformLocal</b>.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/b2d9519a-9e22-44ba-839d-e1ba33aacc26">SetTransformLookup</a>


</td>
<td>
The transform which is retrieved, using a lookup key that matches the key that is set by <a href="https://msdn.microsoft.com/b2d9519a-9e22-44ba-839d-e1ba33aacc26">SetTransformLookup</a>, from the resource directory.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
The lookup key that is set by <a href="https://msdn.microsoft.com/b2d9519a-9e22-44ba-839d-e1ba33aacc26">SetTransformLookup</a>.

</td>
</tr>
<tr>
<td>
Neither <b>SetTransformLocal</b> nor <a href="https://msdn.microsoft.com/b2d9519a-9e22-44ba-839d-e1ba33aacc26">SetTransformLookup</a> has been called yet.

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




<a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a>



<a href="https://msdn.microsoft.com/fc9e1925-0dbc-447b-9acc-e7f719df62d1">IXpsOMTileBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

