---
UID: NF:xpsobjectmodel.IXpsOMTileBrush.SetTransformLookup
title: IXpsOMTileBrush::SetTransformLookup
author: windows-sdk-content
description: Sets the lookup key name of a shared matrix transform that will be used as the transform for this brush.
old-location: xps\ixpsomtilebrush_settransformlookup.htm
tech.root: printdocs
ms.assetid: b2d9519a-9e22-44ba-839d-e1ba33aacc26
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IXpsOMTileBrush interface [XPS Documents and Packaging],SetTransformLookup method, IXpsOMTileBrush.SetTransformLookup, IXpsOMTileBrush::SetTransformLookup, SetTransformLookup, SetTransformLookup method [XPS Documents and Packaging], SetTransformLookup method [XPS Documents and Packaging],IXpsOMTileBrush interface, xps.ixpsomtilebrush_settransformlookup, xpsobjectmodel/IXpsOMTileBrush::SetTransformLookup
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
 - IXpsOMTileBrush.SetTransformLookup
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
- IXpsOMTileBrush.SetTransformLookup
: 
---

# IXpsOMTileBrush::SetTransformLookup


## -description


Sets the lookup key name of a shared matrix transform that will be used as the transform for this brush.The shared matrix transform that is referenced by the lookup key is stored in the resource dictionary.


## -parameters




### -param key [in]

A string variable that contains the lookup key name of a shared matrix transform in the resource dictionary. If a lookup key has already been set, a <b>NULL</b> pointer will clear it.


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
The lookup key name in <i>key</i> references an object that is not a geometry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_LOOKUP_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No object could be found with a key name that matched the value passed in <i>key</i>.

</td>
</tr>
</table>
 




## -remarks



The transform is applied before the brush image is rendered in the path, stroke, or glyph that is using the tile brush. The tile brush has only one transform, which can be local or remote.



After you call <b>SetTransformLookup</b>, the local transform is released and <a href="https://msdn.microsoft.com/e06661dd-387c-46c4-8c37-f4e101d3c536">GetTransformLocal</a> returns a <b>NULL</b> pointer in the <i>transform</i> parameter. The table that follows explains the relationship between the local and lookup values of this property.


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

<a href="https://msdn.microsoft.com/a0a0f0e9-d8b5-4b42-804b-66780f56b09a">SetTransformLocal</a>


</td>
<td>
The transform that is set by <a href="https://msdn.microsoft.com/a0a0f0e9-d8b5-4b42-804b-66780f56b09a">SetTransformLocal</a>.

</td>
<td>
The transform that is set by <a href="https://msdn.microsoft.com/a0a0f0e9-d8b5-4b42-804b-66780f56b09a">SetTransformLocal</a>.

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
The transform which is retrieved—using a lookup key that matches the key that is set by <b>SetTransformLookup</b>— from the resource directory.

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
Neither <a href="https://msdn.microsoft.com/a0a0f0e9-d8b5-4b42-804b-66780f56b09a">SetTransformLocal</a> nor <b>SetTransformLookup</b> has been called yet.

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




<a href="https://msdn.microsoft.com/fc9e1925-0dbc-447b-9acc-e7f719df62d1">IXpsOMTileBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

