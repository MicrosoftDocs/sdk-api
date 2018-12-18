---
UID: NF:xpsobjectmodel.IXpsOMTileBrush.GetTransform
title: IXpsOMTileBrush::GetTransform
author: windows-sdk-content
description: Gets a pointer to the IXpsOMMatrixTransform interface that contains the resolved matrix transform for the brush.
old-location: xps\ixpsomtilebrush_gettransform.htm
tech.root: printdocs
ms.assetid: db4c4ef8-d5f4-4cff-b38d-d211e14a98c1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTransform, GetTransform method [XPS Documents and Packaging], GetTransform method [XPS Documents and Packaging],IXpsOMTileBrush interface, IXpsOMTileBrush interface [XPS Documents and Packaging],GetTransform method, IXpsOMTileBrush.GetTransform, IXpsOMTileBrush::GetTransform, xps.ixpsomtilebrush_gettransform, xpsobjectmodel/IXpsOMTileBrush::GetTransform
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
 - IXpsOMTileBrush.GetTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMTileBrush::GetTransform


## -description


Gets a pointer to the <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface that contains the resolved matrix transform for the brush.


## -parameters




### -param transform [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a>  interface that contains the resolved matrix transform for the brush. If a matrix transform has not been set, a <b>NULL</b> pointer is returned.

The value that is returned in this parameter depends on which method has most recently been called to set the transform.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned  in <i>transform</i></th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/a0a0f0e9-d8b5-4b42-804b-66780f56b09a">SetTransformLocal</a>


</td>
<td>
The transform that is set by <a href="https://msdn.microsoft.com/a0a0f0e9-d8b5-4b42-804b-66780f56b09a">SetTransformLocal</a>.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/b2d9519a-9e22-44ba-839d-e1ba33aacc26">SetTransformLookup</a>


</td>
<td>
The transform which is retrieved, using a lookup key that matches the key that is set by <a href="https://msdn.microsoft.com/b2d9519a-9e22-44ba-839d-e1ba33aacc26">SetTransformLookup</a>, from the resource directory.

</td>
</tr>
<tr>
<td>
Neither <a href="https://msdn.microsoft.com/a0a0f0e9-d8b5-4b42-804b-66780f56b09a">SetTransformLocal</a> nor <a href="https://msdn.microsoft.com/b2d9519a-9e22-44ba-839d-e1ba33aacc26">SetTransformLookup</a> has been called yet.

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

</td>
</tr>
</table>
 




## -remarks



The transform determines how the output area is transformed before the brush image is rendered in the path, stroke, or glyph that is using the tile brush.




## -see-also




<a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a>



<a href="https://msdn.microsoft.com/fc9e1925-0dbc-447b-9acc-e7f719df62d1">IXpsOMTileBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

