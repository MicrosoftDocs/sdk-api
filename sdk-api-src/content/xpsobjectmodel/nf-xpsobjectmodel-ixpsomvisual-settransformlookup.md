---
UID: NF:xpsobjectmodel.IXpsOMVisual.SetTransformLookup
title: IXpsOMVisual::SetTransformLookup method
author: windows-driver-content
description: Sets the lookup key name of a shared matrix transform in a resource dictionary.
old-location: xps\ixpsomvisual_settransformlookup.htm
old-project: printdocs
ms.assetid: b9066cf8-37b5-4c30-ae41-f92a61aa552c
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IXpsOMVisual, IXpsOMVisual interface [XPS Documents and Packaging], SetTransformLookup method, IXpsOMVisual::SetTransformLookup, SetTransformLookup method [XPS Documents and Packaging], SetTransformLookup method [XPS Documents and Packaging], IXpsOMVisual interface, SetTransformLookup,IXpsOMVisual.SetTransformLookup, xps.ixpsomvisual_settransformlookup, xpsobjectmodel/IXpsOMVisual::SetTransformLookup
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IXpsOMVisual.SetTransformLookup
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMVisual::SetTransformLookup method


## -description


Sets the lookup key name of a shared matrix transform in a resource dictionary.


## -parameters




### -param key [in]

The lookup key name of the matrix transform in the dictionary. 


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



After you call <b>SetTransformLookup</b>, the local transform is released and <a href="https://msdn.microsoft.com/a7152ba0-2b65-4c66-b99b-7450a8cdb6fd">GetTransformLocal</a> returns a <b>NULL</b> pointer in the <i>matrixTransform</i> parameter. The table that follows explains the relationship between the local and lookup values of this property.


<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>transform</i> by <a href="https://msdn.microsoft.com/966916c9-8b63-468b-80fb-0c4863ff893a">GetTransform</a>
</th>
<th>Object that is returned in <i>matrixTransform</i> by <a href="https://msdn.microsoft.com/a7152ba0-2b65-4c66-b99b-7450a8cdb6fd">GetTransformLocal</a>
</th>
<th>Object that is returned in <i>key</i> by <a href="https://msdn.microsoft.com/83d30b9c-4d3d-4fca-8dea-121074642b39">GetTransformLookup</a>
</th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/ac087cb0-dd3c-4f4b-a6e0-6f0f0a219d8a">SetTransformLocal</a>


</td>
<td>
The local transform that is set by <a href="https://msdn.microsoft.com/ac087cb0-dd3c-4f4b-a6e0-6f0f0a219d8a">SetTransformLocal</a>.

</td>
<td>
The local transform that is set by <a href="https://msdn.microsoft.com/ac087cb0-dd3c-4f4b-a6e0-6f0f0a219d8a">SetTransformLocal</a>.

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
The shared transform that gets retrieved—with a lookup key that matches the key that is set by <b>SetTransformLookup</b>—from the resource directory.

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
Neither <a href="https://msdn.microsoft.com/ac087cb0-dd3c-4f4b-a6e0-6f0f0a219d8a">SetTransformLocal</a> nor <b>SetTransformLookup</b> has been called yet.

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




<a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

