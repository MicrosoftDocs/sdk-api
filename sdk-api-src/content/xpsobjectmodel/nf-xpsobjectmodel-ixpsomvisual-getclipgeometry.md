---
UID: NF:xpsobjectmodel.IXpsOMVisual.GetClipGeometry
title: IXpsOMVisual::GetClipGeometry
author: windows-sdk-content
description: Gets a pointer to the IXpsOMGeometry interface that contains the resolved geometry of the visual's clipping region.
old-location: xps\ixpsomvisual_getclipgeometry.htm
tech.root: printdocs
ms.assetid: f56fa077-749c-422b-b82d-161f9e5d4766
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetClipGeometry, GetClipGeometry method [XPS Documents and Packaging], GetClipGeometry method [XPS Documents and Packaging],IXpsOMVisual interface, IXpsOMVisual interface [XPS Documents and Packaging],GetClipGeometry method, IXpsOMVisual.GetClipGeometry, IXpsOMVisual::GetClipGeometry, xps.ixpsomvisual_getclipgeometry, xpsobjectmodel/IXpsOMVisual::GetClipGeometry
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
 - IXpsOMVisual.GetClipGeometry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMVisual::GetClipGeometry


## -description


Gets a pointer to the <a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a> interface that contains the resolved geometry of the visual's clipping region.


## -parameters




### -param clipGeometry [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a> interface that contains the resolved geometry of the visual's clipping region. If  the clip geometry has not been set, a <b>NULL</b> pointer is returned.

The value that is returned in this parameter depends on which method has most recently been called to set the geometry.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>clipGeometry</i></th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/8b703866-9dc0-4327-9988-908f17bd4b21">SetClipGeometryLocal</a>


</td>
<td>
The local clip geometry that is set by <a href="https://msdn.microsoft.com/8b703866-9dc0-4327-9988-908f17bd4b21">SetClipGeometryLocal</a>.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/3f79f1ce-e761-44f7-970c-393c83f8f2fd">SetClipGeometryLookup</a>


</td>
<td>
The shared clip geometry that gets retrieved, with a lookup key that matches the key that is set by <a href="https://msdn.microsoft.com/3f79f1ce-e761-44f7-970c-393c83f8f2fd">SetClipGeometryLookup</a>, from the resource directory.

</td>
</tr>
<tr>
<td>
Neither <a href="https://msdn.microsoft.com/8b703866-9dc0-4327-9988-908f17bd4b21">SetClipGeometryLocal</a> nor <a href="https://msdn.microsoft.com/3f79f1ce-e761-44f7-970c-393c83f8f2fd">SetClipGeometryLookup</a> has been called yet.

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
<i>clipGeometry</i> is <b>NULL</b>.

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




<a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a>



<a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

