---
UID: NF:xpsobjectmodel.IXpsOMGradientBrush.GetTransformLookup
title: IXpsOMGradientBrush::GetTransformLookup
author: windows-sdk-content
description: Gets the name of the lookup key of the shared matrix transform interface that is to be used for the brush.
old-location: xps\ixpsomgradientbrush_gettransformlookup.htm
old-project: printdocs
ms.assetid: 60a91156-f9c8-4f6b-92b7-21e2fcd337fc
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: GetTransformLookup, GetTransformLookup method [XPS Documents and Packaging], GetTransformLookup method [XPS Documents and Packaging],IXpsOMGradientBrush interface, IXpsOMGradientBrush interface [XPS Documents and Packaging],GetTransformLookup method, IXpsOMGradientBrush.GetTransformLookup, IXpsOMGradientBrush::GetTransformLookup, xps.ixpsomgradientbrush_gettransformlookup, xpsobjectmodel/IXpsOMGradientBrush::GetTransformLookup
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
 - IXpsOMGradientBrush.GetTransformLookup
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMGradientBrush::GetTransformLookup


## -description


Gets the name of the lookup key  of the shared matrix transform interface that is to be used for the brush.

The key name identifies a shared resource in a resource dictionary.


## -parameters




### -param key [out, retval]

The name of the lookup key  of the shared matrix transform interface that is to be used for the brush. If the lookup key name has not been set or if the local matrix transform has  been set, a <b>NULL</b> pointer is returned.

The value that is returned in this parameter depends on which method has been most recently called to set the lookup key or the transform.

<table>
<tr>
<th>Most recent method called</th>
<th>String that is returned in <i>key</i></th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/aabb0410-bdff-4b6b-8d8a-de1cc6fca68b">SetTransformLocal</a>


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
The key that is set by <a href="https://msdn.microsoft.com/342434ff-9fdc-43ea-8beb-9d518f7a9454">SetTransformLookup</a>.

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
<i>key</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method does not return an <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface pointer; to retrieve this pointer  from the dictionary, call <a href="https://msdn.microsoft.com/6efc2fed-e372-4416-9645-50c1430f0e75">IXpsOMDictionary::GetByKey</a>.

 The transform  determines how the gradient is transformed. The visible part of the gradient that is ultimately rendered in the image is determined by the path, stroke, or glyph that is using the gradient brush.

This method allocates the memory used by the string that is returned in <i>key</i>.  If <i>key</i> is not <b>NULL</b>, use the <a href="https://msdn.microsoft.com/library/ms680722(v=VS.85).aspx">CoTaskMemFree</a> function  to free the memory.




## -see-also




<a href="https://msdn.microsoft.com/f887e3d3-973c-4267-a785-6bc190c13082">IXpsOMDictionary</a>



<a href="https://msdn.microsoft.com/d381b813-5368-4ffe-a9a1-0f5027ae9d80">IXpsOMGradientBrush</a>



<a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

