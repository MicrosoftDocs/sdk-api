---
UID: NF:xpsobjectmodel.IXpsOMVisual.GetTransform
title: IXpsOMVisual::GetTransform
author: windows-sdk-content
description: Gets a pointer to the IXpsOMMatrixTransform interface that contains the visual's resolved matrix transform.
old-location: xps\ixpsomvisual_gettransform.htm
tech.root: printdocs
ms.assetid: 966916c9-8b63-468b-80fb-0c4863ff893a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetTransform, GetTransform method [XPS Documents and Packaging], GetTransform method [XPS Documents and Packaging],IXpsOMVisual interface, IXpsOMVisual interface [XPS Documents and Packaging],GetTransform method, IXpsOMVisual.GetTransform, IXpsOMVisual::GetTransform, xps.ixpsomvisual_gettransform, xpsobjectmodel/IXpsOMVisual::GetTransform
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
 - IXpsOMVisual.GetTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xpsobjectmodel.h
: 
- IXpsOMVisual.GetTransform
: 
---

# IXpsOMVisual::GetTransform


## -description


Gets a pointer to the <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface that contains the visual's resolved matrix transform.


## -parameters




### -param matrixTransform [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface that contains the visual's resolved matrix transform. If  a matrix transform has not been set, a <b>NULL</b> pointer is returned.

The value that is returned in this parameter depends on which method has most recently been called to set the transform.

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
The shared transform that gets retrieved, with a lookup key that matches the key that is set by <a href="https://msdn.microsoft.com/b9066cf8-37b5-4c30-ae41-f92a61aa552c">SetTransformLookup</a>, from the resource directory.

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
 




## -see-also




<a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a>



<a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

