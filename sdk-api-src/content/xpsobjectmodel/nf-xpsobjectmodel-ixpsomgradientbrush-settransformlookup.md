---
UID: NF:xpsobjectmodel.IXpsOMGradientBrush.SetTransformLookup
title: IXpsOMGradientBrush::SetTransformLookup
author: windows-sdk-content
description: Sets the name of the lookup key of a shared matrix transform that is to be used for the brush.
old-location: xps\ixpsomgradientbrush_settransformlookup.htm
old-project: printdocs
ms.assetid: 342434ff-9fdc-43ea-8beb-9d518f7a9454
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IXpsOMGradientBrush interface [XPS Documents and Packaging],SetTransformLookup method, IXpsOMGradientBrush.SetTransformLookup, IXpsOMGradientBrush::SetTransformLookup, SetTransformLookup, SetTransformLookup method [XPS Documents and Packaging], SetTransformLookup method [XPS Documents and Packaging],IXpsOMGradientBrush interface, xps.ixpsomgradientbrush_settransformlookup, xpsobjectmodel/IXpsOMGradientBrush::SetTransformLookup
ms.prod: windows
ms.technology: windows-sdk
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
 - IXpsOMGradientBrush.SetTransformLookup
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMGradientBrush::SetTransformLookup


## -description


Sets the name of the lookup key of a shared matrix transform that is to be used for the brush.

The key name identifies a shared resource in a resource dictionary.


## -parameters




### -param key [in]

The name of the lookup key of the matrix transform that is to be used for the brush. 


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



After you call <b>SetTransformLookup</b>, the local transform is released and <a href="https://msdn.microsoft.com/dfdd6797-b7e6-46fa-92b1-d9c418e8a510">GetTransformLocal</a> returns a <b>NULL</b> pointer in the <i>transform</i> parameter. The table that follows explains the relationship between the local and lookup values of this property.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned  in <i>transform</i> by <a href="https://msdn.microsoft.com/6b5474d2-a97e-4446-b4a9-7efb51c31ad3">GetTransform</a>
</th>
<th>Object that is returned  in <i>transform</i> by <a href="https://msdn.microsoft.com/dfdd6797-b7e6-46fa-92b1-d9c418e8a510">GetTransformLocal</a>
</th>
<th>Object that is returned  in <i>key</i> by <a href="https://msdn.microsoft.com/60a91156-f9c8-4f6b-92b7-21e2fcd337fc">GetTransformLookup</a>
</th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/aabb0410-bdff-4b6b-8d8a-de1cc6fca68b">SetTransformLocal</a>


</td>
<td>
The local transform that is set by <a href="https://msdn.microsoft.com/aabb0410-bdff-4b6b-8d8a-de1cc6fca68b">SetTransformLocal</a>.

</td>
<td>
The local transform that is set by <a href="https://msdn.microsoft.com/aabb0410-bdff-4b6b-8d8a-de1cc6fca68b">SetTransformLocal</a>.

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
The shared transform retrieved, with a lookup key that matches the key that is set by <b>SetTransformLookup</b>, from the resource directory.

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
Neither <a href="https://msdn.microsoft.com/aabb0410-bdff-4b6b-8d8a-de1cc6fca68b">SetTransformLocal</a> nor <b>SetTransformLookup</b> has been called yet.

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
 

 The transform referenced by <i>key</i>  determines how the gradient is transformed. The visible part of the gradient that is ultimately rendered in the image is determined by the path, stroke, or glyph that is using the brush.




## -see-also




<a href="https://msdn.microsoft.com/d381b813-5368-4ffe-a9a1-0f5027ae9d80">IXpsOMGradientBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

