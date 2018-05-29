---
UID: NF:xpsobjectmodel.IXpsOMGradientBrush.SetTransformLocal
title: IXpsOMGradientBrush::SetTransformLocal
author: windows-sdk-content
description: Sets the IXpsOMMatrixTransform interface pointer to a local, unshared matrix transform that is to be used for the brush.
old-location: xps\ixpsomgradientbrush_settransformlocal.htm
old-project: printdocs
ms.assetid: aabb0410-bdff-4b6b-8d8a-de1cc6fca68b
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IXpsOMGradientBrush interface [XPS Documents and Packaging],SetTransformLocal method, IXpsOMGradientBrush.SetTransformLocal, IXpsOMGradientBrush::SetTransformLocal, SetTransformLocal, SetTransformLocal method [XPS Documents and Packaging], SetTransformLocal method [XPS Documents and Packaging],IXpsOMGradientBrush interface, xps.ixpsomgradientbrush_settransformlocal, xpsobjectmodel/IXpsOMGradientBrush::SetTransformLocal
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
req.typenames: XPS_INTERLEAVING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsobjectmodel.h
api_name:
-	IXpsOMGradientBrush.SetTransformLocal
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMGradientBrush::SetTransformLocal


## -description


Sets the <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface pointer to a local, unshared matrix transform that is to be used for the brush.


## -parameters




### -param transform [in]

A pointer to the <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface of the local, unshared matrix transform that is to be used for the brush. A <b>NULL</b> pointer releases any previously set interface.


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



After you call <b>SetTransformLocal</b>, the transform lookup key is released and <a href="https://msdn.microsoft.com/dfdd6797-b7e6-46fa-92b1-d9c418e8a510">GetTransformLocal</a> returns a <b>NULL</b> pointer in the <i>transform</i> parameter. The table that follows explains the relationship between the local and lookup values of this property.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>transform</i> by <a href="https://msdn.microsoft.com/6b5474d2-a97e-4446-b4a9-7efb51c31ad3">GetTransform</a>
</th>
<th>Object that is returned in <i>transform</i> by <a href="https://msdn.microsoft.com/dfdd6797-b7e6-46fa-92b1-d9c418e8a510">GetTransformLocal</a>
</th>
<th>Object that is returned in <i>key</i> by <a href="https://msdn.microsoft.com/60a91156-f9c8-4f6b-92b7-21e2fcd337fc">GetTransformLookup</a>
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

<a href="https://msdn.microsoft.com/342434ff-9fdc-43ea-8beb-9d518f7a9454">SetTransformLookup</a>


</td>
<td>
The shared transform retrieved, with a lookup key that matches the key that is set by <a href="https://msdn.microsoft.com/342434ff-9fdc-43ea-8beb-9d518f7a9454">SetTransformLookup</a>, from the resource directory.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
The lookup key that is set by <a href="https://msdn.microsoft.com/342434ff-9fdc-43ea-8beb-9d518f7a9454">SetTransformLookup</a>.

</td>
</tr>
<tr>
<td>
Neither <b>SetTransformLocal</b> nor <a href="https://msdn.microsoft.com/342434ff-9fdc-43ea-8beb-9d518f7a9454">SetTransformLookup</a> has been called yet.

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
 

 The transform passed in <i>transform</i>  determines how the gradient is transformed. The visible part of the gradient that is ultimately rendered in the image is determined by the path, stroke, or glyph that is using the gradient brush.




## -see-also




<a href="https://msdn.microsoft.com/d381b813-5368-4ffe-a9a1-0f5027ae9d80">IXpsOMGradientBrush</a>



<a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

